# GitHub CLI project layout

在高层次上，这些领域构成了`github.com/cli/cli`项目：

-   [`cmd/`](../cmd) - `main`用于构建二进制文件的包，例如`gh`可执行
-   [`pkg/`](../pkg)-大多数其他软件包，包括单个gh命令的实现
-   [`docs/`](../docs)-维护人员和贡献者的文档
-   [`script/`](../script)-构建和发布脚本
-   [`internal/`](../internal)-Go软件包高度特定于我们的需求，因此是内部的
-   [`go.mod`](../go.mod)-此项目的外部Go依赖项，由Go在生成时自动获取

由于历史原因，一些辅助Go包处于项目的顶层：

-   [`api/`](../api)-向GitHub API发出请求的主要实用程序
-   [`context/`](../context)-不推荐：仅用于引用git远程
-   [`git/`](../git)-从本地git存储库收集信息的实用程序
-   [`test/`](../test)-不推荐：不要使用
-   [`utils/`](../utils)-不推荐：仅用于打印表输出

## Command-line help text

跑步`gh help issue list`显示主题的帮助文本。在本例中，主题是一个特定的命令，每个命令的帮助文本都嵌入到该命令的源代码中。gh命令的命名约定为：

```
pkg/cmd/<command>/<subcommand>/<subcommand>.go
```

在上面的示例之后`gh issue list`命令（包括其帮助文本）位于[pkg/cmd/issue/list/list.go](../pkg/cmd/issue/list/list.go)

其他非特定于任何命令的帮助主题，例如`gh help environment`，在[pkg/cmd/root/help_topic.go](../pkg/cmd/root/help_topic.go).

在我们的发布过程中，这些帮助主题是[automatically converted](../cmd/gen-docs/main.go)到手册页并在下发布<https://cli.github.com/manual/>.

## How GitHub CLI works

为了说明GitHub CLI在其典型操作模式下的工作方式，让我们构建项目，运行命令，然后讨论按顺序运行的代码。

1.  `go run script/build.go`-确保获取所有外部Go依赖项，然后编译`cmd/gh/main.go`归档`bin/gh`二进制的
2.  `bin/gh issue list --limit 5`-运行新建的`bin/gh`二进制（注意：在Windows上必须使用反斜杠，如`bin\gh`)并将以下参数传递给进程：`["issue", "list", "--limit", "5"]`.
3.  `func main()`在…内`cmd/gh/main.go`是运行的第一个Go函数。传递给进程的参数可以通过`os.Args`.
4.  这个`main`包使用以下命令初始化“root”命令`root.NewCmdRoot()`并向其发出执行命令`rootCmd.ExecuteC()`.
5.  这个[root command](../pkg/cmd/root/root.go)表示顶层`gh`命令，并知道如何将执行分派给嵌套在其下的任何其他gh命令。
6.  基于`["issue", "list"]`参数，则执行到达`RunE`街区`cobra.Command`在内部[pkg/cmd/issue/list/list.go](../pkg/cmd/issue/list/list.go).
7.  这个`--limit 5`将自动分析最初作为参数传递的标志，并将其值存储为`opts.LimitResults`.
8.  `func listRun()`调用，它负责实现`gh issue list`命令
9.  该命令从githubapi等源收集信息，然后将最终输出写入标准输出和标准错误[streams](../pkg/iostreams/iostreams.go)可在`opts.IO`.
10. 程序执行现在返回到`func main()`属于`cmd/gh/main.go`。如果处理该命令时出现任何Go错误，则该函数将以非零退出状态中止该过程。否则，进程将以状态0结束，表示成功。

## How to add a new command

1.  首先，检查我们的问题追踪器，确认我们的团队已经批准了新司令部的计划。
2.  为新命令创建包，例如，为新命令创建包`gh boom`创建以下目录结构：`pkg/cmd/boom/`
3.  新包应该公开一个方法，例如。`NewCmdBoom()`，即接受`*cmdutil.Factory`键入并返回一个`*cobra.Command`.
    -   任何特定于此命令的逻辑都应该保存在命令包中，而不是添加到任何“全局”包中，如`api`或`utils`.
4.  使用上一步中的方法生成命令并将其添加到命令树中，通常在`NewCmdRoot()`方法

## How to write tests

这项任务可能很棘手。通常，gh命令执行的操作包括从当前目录的git存储库中查找信息、查询githubapi、扫描用户的`~/.ssh/config`文件、克隆或获取git存储库等。当然，在运行测试时，这些事情都不应该真正发生，除非您确信任何文件系统操作都严格限定在测试本身创建和维护的位置。避免实际运行诸如发出真正的API请求或向`git`命令，我们将它们存根。您应该看看在一些现有测试中是如何做到这一点的。

要使您的代码可测试，请编写设计为组合在一起的小型、独立的功能。在执行单个功能时，更喜欢使用表驱动测试来维护不同测试输入和期望的变化。
