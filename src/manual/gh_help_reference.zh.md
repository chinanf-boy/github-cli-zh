## gh reference

# gh reference

## `gh actions`

了解如何使用 GitHub Actions

## `gh alias <command>`

创建命令快捷方式

### `gh alias delete <alias>`

删除别名

### `gh alias list`

列出你的别名

### `gh alias set <alias> <expansion> [flags]`

为 gh 命令，创建快捷方式

```
-s, --shell   定义个 alias 传递给 shell 解释器，r
```

## `gh api <endpoint> [flags]`

发出，经过身份验证的 GitHub API 请求

```
    --cache duration        缓存一个响应, e.g. "3600s", "60m", "1h"
-F, --field key=value       添加一个类型参数，格式是 key=value
-H, --header key:value      添加一个 HTTP 请求头，格式是 key=value
    --hostname string       请求的 GitHub 主址 (default "github.com")
-i, --include               将 HTTP 响应头也输出
    --input file            file 作为 HTTP 请求的主体 (使用 "-" 可以从标准输入读取)
-q, --jq string             使用 jq 语法，查询响应的值
-X, --method string         HTTP 方法 (默认 "GET")
    --paginate              发出额外的 HTTP 请求，获取所有的结果页
-p, --preview strings       GitHub API 预览版本的功能
-f, --raw-field key=value   添加一个字符串参数，格式是 key=value
    --silent                不打印
-t, --template string       用模板格式化响应
```

## `gh auth <command>`

登录、注销和刷新您的身份验证

### `gh auth login [flags]`

通过 GitHub 主机进行身份验证

```
-h, --hostname string   身份验证的 GitHub 主址
-s, --scopes strings    权限范围
-w, --web               打开浏览器，进行身份验证
    --with-token        从标准输入读取令牌
```

### `gh auth logout [flags]`

注销 GitHub 主机

```
-h, --hostname string   身份登出的 GitHub 主址
```

### `gh auth refresh [flags]`

刷新存储的身份验证凭据

```
-h, --hostname string   身份验证的 GitHub 主址
-s, --scopes strings    权限范围
```

### `gh auth setup-git [flags]`

配置 git，以将 GitHub CLI 用作凭据帮助器

```
-h, --hostname string   配置 git 的 主机网址
```

### `gh auth status [flags]`

查看身份验证状态

```
-h, --hostname string   检查的主机
-t, --show-token        展示 身份令牌
```

## `gh browse [<number> | <path>] [flags]`

在浏览器中，打开存储库

```
-b, --branch string   换分支
-c, --commit          打开最后的 commit
-n, --no-browser      给 URL，不打开浏览器
-p, --projects        打开 projects
-s, --settings        打开 settings
-w, --wiki            打开 wiki
```

## `gh codespace`

连接，并管理您的代码空间

### `gh codespace code [flags]`

在 Visual Studio Code 中打开代码空间

```
-c, --codespace string   名字
    --insiders           Use the insiders version of Visual Studio Code
```

### `gh codespace cp [-e] [-r] <sources>... <dest>`

在本地和远程文件系统之间，复制文件

```
-c, --codespace string   名字
-e, --expand             在远程 shell上，展开远程的（多个）文件名
-r, --recursive          递归复制目录
```

### `gh codespace create [flags]`

创建一个代码空间

```
-b, --branch string           分支
    --idle-timeout duration   在 codespace 停止之前，不活动的时间, e.g. "10m", "1h"
-m, --machine string          VM 硬件规格
-r, --repo string             拥有者的库名: user/repo
-s, --status                  展示 post-create 命令和 dotfiles
```

### `gh codespace delete [flags]`

删除代码空间

```
    --all                删除所有
-c, --codespace string   名字
    --days N             删除过去 N 天
-f, --force              强制删除
-r, --repo repository    删除一个库
```

### `gh codespace list [flags]`

列出你的代码空间

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-L, --limit int         Maximum number of codespaces to list (default 30)
-t, --template string   模板化输出
```

### `gh codespace logs [flags]`

访问代码空间日志

```
-c, --codespace string   名字
-f, --follow             日志跟随滚动
```

### `gh codespace ports [flags]`

列出代码空间中的端口

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
```

#### `gh codespace ports forward <remote-port>:<local-port>...`

转发端口

#### `gh codespace ports visibility <port>:{public|private|org}...`

更改转发端口的可见性

### `gh codespace ssh [<flags>...] [-- <ssh-flags>...] [<command>]`

SSH 到一个代码空间

```
-c, --codespace string    名字
-d, --debug               调试数据装入文件
    --debug-file string   文件日志的路径
    --profile string      所使用的 SSH profile 名称
    --server-port int     SSH 服务器端口号 (0 => pick unused)
```

### `gh codespace stop [flags]`

停止运行代码空间

```
-c, --codespace string   名字
```

## `gh completion -s <shell>`

生成 shell 完成脚本

```
-s, --shell string   Shell type: {bash|zsh|fish|powershell}
```

## `gh config <command>`

管理 gh 的配置

### `gh config get <key> [flags]`

打印给定配置密钥的值

```
-h, --host string   获取每个 host 的 setting
```

### `gh config list [flags]`

打印配置键和值的列表

```
-h, --host string   获取每个 host 的 configuration
```

### `gh config set <key> <value> [flags]`

使用给定密钥的值更新配置

```
-h, --host string   设置每个 host 的 setting
```

## `gh extension`

管理 gh 扩展

### `gh extension create [<name>] [flags]`

创建一个新的扩展名

```
--precompiled string   预编译扩展。可能的值: go, other
```

### `gh extension install <repository>`

从存储库安装 gh 扩展

### `gh extension list`

列出已安装的扩展命令

### `gh extension remove <name>`

删除已安装的扩展

### `gh extension upgrade {<name> | --all} [flags]`

升级已安装的扩展

```
--all     更新所有
--force   强制更新
```

## `gh gist <command>`

与 GitHub gist（要点） 合作

### `gh gist clone <gist> [<directory>] [-- <gitflags>...]`

本地克隆要点

### `gh gist create [<filename>... | -] [flags]`

创造一个新的要点

```
-d, --desc string       描述
-f, --filename string   标准输入，给个文件名
-p, --public            公开 (default: secret)
-w, --web               gist 链接，打开浏览器
```

### `gh gist delete {<id> | <url>}`

删除要点

### `gh gist edit {<id> | <url>} [flags]`

编辑一个要点

```
-a, --add string        新增一个文件
-f, --filename string   选择一个文件编辑
```

### `gh gist list [flags]`

列出你的要点

```
-L, --limit int   Maximum number of gists to fetch (default 10)
    --public      Show only public gists
    --secret      Show only secret gists
```

### `gh gist view [<id> | <url>] [flags]`

要点

```
-f, --filename string   展示单个文件
    --files             列出文件名列表
-r, --raw               原始内容
-w, --web               浏览器打开
```

## `gh gpg-key <command>`

管理 GPG 密钥

### `gh gpg-key add [<key-file>]`

将 GPG 密钥添加到 GitHub 帐户

### `gh gpg-key list`

列出 GitHub 帐户中的 GPG 密钥

## `gh issue <command>`

管理问题

### `gh issue close {<number> | <url>}`

结案

### `gh issue comment {<number> | <url>} [flags]`

创建新的问题注释

```
-b, --body string      提供主体内容。不填，也会提示
-F, --body-file file   读取文件，输入主体内容 (使用 "-" 可以从标准输入读取)
-e, --editor           通过 editor 添加主体
-w, --web              用浏览器打开网络链接，添加主体
```

### `gh issue create [flags]`

创刊

```
-a, --assignee login   通过 login 分配人员。使用 @me 自我分配。
-b, --body string      提供主体内容。不填，也会提示
-F, --body-file file   读取文件，输入主体内容 (使用 "-" 可以从标准输入读取)
-l, --label name       添加标签
-m, --milestone name   通过 name，添加 issue 到 name 里程牌
-p, --project name     通过 name，添加 issue 到 name 项目
    --recover string   一次失败创建，带来的恢复输入
-t, --title string     提供一个标题。不填，也会提示
-w, --web              浏览器打开，创建 issue
```

### `gh issue delete {<number> | <url>}`

删除问题

### `gh issue edit {<number> | <url>} [flags]`

编辑问题

```
    --add-assignee login      通过 login 分配人员。使用 @me 自我分配。
    --add-label name          添加标签
    --add-project name        通过 name，添加 issue 到 name 项目
-b, --body string             设置新的主体内容.
-F, --body-file file          读取文件，输入主体内容 (使用 "-" 可以从标准输入读取)
-m, --milestone name          用 name，编辑下里程碑
    --remove-assignee login   移除 login 的人员配置. 使用 @me 就移除自己
    --remove-label name       移除 name 标签
    --remove-project name     移除 name 项目
-t, --title string            设置新的标题.
```

### `gh issue list [flags]`

列出并筛选此存储库中的问题

```
-a, --assignee string    过滤项：assignee
-A, --author string      过滤项：author
-q, --jq expression      jq 表达式，过滤 JSON 输出
    --json fields        JSON 输出特殊字段
-l, --label strings      过滤项：labels
-L, --limit int          Maximum number of issues to fetch (default 30)
    --mention string     过滤项：mention
-m, --milestone number   过滤项：milestone number or `title`
-S, --search query       query 搜索 issue
-s, --state string       过滤项：state: {open|closed|all} (default "open")
-t, --template string    模板化输出
-w, --web                浏览器打开，列出 issue(s)
```

### `gh issue reopen {<number> | <url>}`

重新发行

### `gh issue status [flags]`

显示相关问题的状态

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
```

### `gh issue transfer {<number> | <url>} <destination-repo>`

将问题转移到另一个存储库

### `gh issue view {<number> | <url>} [flags]`

看问题

```
-c, --comments          View issue comments
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               Open an issue in the browser
```

## `gh pr <command>`

管理拉取请求

### `gh pr checkout {<number> | <url> | <branch>} [flags]`

查看 git 中的 pull 请求

```
-b, --branch string        本地分支名 (default: the name of the head branch)
    --detach               以一种分离 HEAD 的状态，查看 PR
-f, --force                重设本地分支为最新的PR
    --recurse-submodules   在 checkout 之后，更新所有的 submodules
```

### `gh pr checks [<number> | <url> | <branch>] [flags]`

显示单个 PR 的 CI 状态

```
-w, --web   浏览器打开
```

### `gh pr close {<number> | <url> | <branch>} [flags]`

关闭拉取请求

```
-d, --delete-branch   关闭 PR 之后，删除本地与远程的分支
```

### `gh pr comment [<number> | <url> | <branch>] [flags]`

创建新的 PR 评论

```
-b, --body string      提供主体内容。不填，也会提示
-F, --body-file file   读取文件，输入主体内容 (使用 "-" 可以从标准输入读取)
-e, --editor           通过 editor 添加主体
-w, --web              用浏览器打开网络链接，添加主体
```

### `gh pr create [flags]`

创建拉取请求

```
-a, --assignee login       通过 login 分配人员。使用 @me 自我分配。
-B, --base branch          要合并到的分支
-b, --body string          PR 的主体内容
-F, --body-file file       读取文件，输入主体内容
-d, --draft                草稿版
-f, --fill                 不用提示，使用 commit 的信息填入 title/body
-H, --head branch          包含你 commits 的分支 (default: current branch)
-l, --label name           添加标签
-m, --milestone name       通过 name，添加 PR 到 name 里程牌
    --no-maintainer-edit   禁用维护人员修改 PR 
-p, --project name         将 pull request 添加到 name 项目
    --recover string       一次失败创建，带来的恢复输入
-r, --reviewer handle      PR 审查人员
-t, --title string         添加 标题
-w, --web                  浏览器打开
```

### `gh pr diff [<number> | <url> | <branch>] [flags]`

查看拉取请求中的更改

```
--color string   在 diff 输出中，使用颜色: {always|never|auto} (default "auto")
--patch          以 patch 格式，展示 diff
```

### `gh pr edit [<number> | <url> | <branch>] [flags]`

编辑拉取请求

```
    --add-assignee login      通过 login 分配人员。使用 @me 自我分配
    --add-label name          添加标签
    --add-project name        将 pull request 添加到 name 项目
    --add-reviewer login      通过 login ，添加审查人员.
-B, --base branch             更改 PR 的基分支
-b, --body string             设置新的主体内容.
-F, --body-file file          读取文件，输入主体内容 (使用 "-" 可以从标准输入读取)
-m, --milestone name          编辑 name 里程牌
    --remove-assignee login   移除 login 的人员配置. 使用 @me 就移除自己
    --remove-label name       移除 name 标签
    --remove-project name     移除 name 项目的 PR
    --remove-reviewer login   通过 login ，移除审查人员.
-t, --title string            设置新的标题.
```

### `gh pr list [flags]`

列出并筛选此存储库中的请求

```
-a, --assignee string   过滤项：assignee
-A, --author string     过滤项：author
-B, --base string       过滤项：base branch
-d, --draft             过滤项：draft state
-H, --head string       过滤项：head branch
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-l, --label strings     过滤项：labels
-L, --limit int         Maximum number of items to fetch (default 30)
-S, --search query      Search pull requests with query
-s, --state string      过滤项：state: {open|closed|merged|all} (default "open")
-t, --template string   模板化输出
-w, --web               Open the browser to list the pull requests
```

### `gh pr merge [<number> | <url> | <branch>] [flags]`

合并拉取请求

```
    --admin            即便条件不达标，用管理员权限合并
    --auto             条件符合，自动合并
-b, --body text        合并的主体内容
-F, --body-file file   读取文件，输入主体内容 (使用 "-" 可以从标准输入读取)
-d, --delete-branch    合并后，删除本地与远程分支
    --disable-auto     禁止自动合并
-m, --merge            合并
-r, --rebase           变基
-s, --squash           将多个提交变成一个，再合并
-t, --subject text     合并提交的主题
```

### `gh pr ready [<number> | <url> | <branch>]`

将 PR 标记为已准备好进行审查

### `gh pr reopen {<number> | <url> | <branch>}`

重新打开拉取请求

### `gh pr review [<number> | <url> | <branch>] [flags]`

向拉取请求添加审阅

```
-a, --approve           批准 pull request
-b, --body string       指定一个审查的主体内容
-F, --body-file file    读取文件，输入主体内容 (使用 "-" 可以从标准输入读取)
-c, --comment           给出评论
-r, --request-changes   要求 PR 修改
```

### `gh pr status [flags]`

显示相关拉取请求的状态

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
```

### `gh pr view [<number> | <url> | <branch>] [flags]`

查看拉取请求

```
-c, --comments          查看 pull request 评论
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               浏览器打开
```

## `gh release <command>`

管理 GitHub 发布

### `gh release create [<tag>] [<files>...]`

创建一个新版本

```
    --discussion-category string   开始指定主题分类的讨论
-d, --draft                        一个草稿版本
    --generate-notes               自动生成，release 的 标题与笔记
-n, --notes string                 Release 笔记
-F, --notes-file file              用文件，读笔记 (使用 "-" 可以从标准输入读取)
-p, --prerelease                   预览版
    --target branch                指定的分支或是完整的 commit SHA (default: main branch)
-t, --title string                 Release 标题
```

### `gh release delete <tag> [flags]`

删除发布

```
-y, --yes   跳过提示
```

### `gh release download [<tag>] [flags]`

下载发布资产

```
-A, --archive format        下载的格式 (zip or tar.gz)
-D, --dir string            下载的位置 (default ".")
-p, --pattern stringArray   只下载符合 glob 匹配模式的资源
```

### `gh release list [flags]`

在存储库中列出发布

```
-L, --limit int   Maximum number of items to fetch (default 30)
```

### `gh release upload <tag> <files>... [flags]`

将资产上载到发布

```
--clobber   覆盖同名资源
```

### `gh release view [<tag>] [flags]`

查看有关发布的信息

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               浏览器打开
```

## `gh repo <command>`

创建、克隆、分叉和查看存储库

### `gh repo archive [<repository>] [flags]`

归档存储库

```
-y, --confirm   跳过提示
```

### `gh repo clone <repository> [<directory>] [-- <gitflags>...]`

在本地克隆存储库

### `gh repo create [<name>] [flags]`

创建一个新的存储库

```
-c, --clone                 Clone 新的存储库到当前目录
-d, --description string    存储库的描述
    --disable-issues        禁用 issues
    --disable-wiki          禁用 wiki
-g, --gitignore string      指定一个 gitignore 的模板
-h, --homepage URL          主页URL
    --internal              内部可见
-l, --license string        指定开源的协议
    --private               私有存储库
    --public                公开存储库
    --push                  推送本地的 commits 到新的存储库
-r, --remote string         指定 remote 名称
-s, --source string         指定存储库的源代码路径e
-t, --team name             可以访问存储库的组织名字
-p, --template repository   让新的存储库，基于 一个模板存储库生成
```

### `gh repo delete [<repository>] [flags]`

删除存储库

```
--confirm   直接通过提示
```

### `gh repo edit [<repository>] [flags]`

编辑存储库设置

```
    --add-topic strings        添加 存储库 标签主题
    --allow-forking            允许被 fork
    --default-branch name      设置默认的分支
    --delete-branch-on-merge   当 pull requests 被合并，删除 HEAD 分支
-d, --description string       存储库的描述
    --enable-auto-merge        启动 auto-merge（自动合并） 功能
    --enable-issues            启用 issues
    --enable-merge-commit      可以用 merge commit，合并 PR
    --enable-projects          启用 projects
    --enable-rebase-merge      可用变基（rebase）的方式合并 PR
    --enable-squash-merge      可用，将多个commit变为一个的方式，合并PR
    --enable-wiki              启用 wiki
-h, --homepage URL             主页URL
    --remove-topic strings     移除存储库的标签主题
    --template                 可将存储库当成，模板存储库
    --visibility string        将存储库的可见性改为 {public,private,internal}
```

### `gh repo fork [<repository>] [-- <gitflags>...] [flags]`

创建存储库的分支

```
--clone                Clone the fork {true|false}
--org string           在一个组织内，创建副本
--remote               要添加远程（上级）存储库吗 {true|false}
--remote-name string   Specify a name for a fork's new remote. (default "origin")
```

### `gh repo list [<owner>] [flags]`

列出用户或组织拥有的存储库

```
    --archived          仅展示存档的存储库
    --fork              仅展示副本存储库
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-l, --language string   主编程语言的过滤
-L, --limit int         Maximum number of repositories to list (default 30)
    --no-archived       不要存档的存储库
    --private           仅展示私有存储库
    --public            仅展示公开的存储库
    --source            仅展示非副本的存储库
-t, --template string   模板化输出
    --topic string      标题主题的过滤
```

### `gh repo rename [<new-name>] [flags]`

重命名存储库

```
-y, --confirm   跳过提示，直接确定
```

### `gh repo sync [<destination-repository>] [flags]`

同步存储库

```
-b, --branch string   同步的分支 (default: main branch)
    --force           强制同步
-s, --source string   源存储库
```

### `gh repo view [<repository>] [flags]`

查看存储库

```
-b, --branch string     显示特定分支
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               浏览器打开
```

## `gh run <command>`

查看有关工作流运行的详细信息

### `gh run cancel [<run-id>]`

取消工作流运行

### `gh run download [<run-id>] [flags]`

下载工作流运行生成的工件

```
-D, --dir string         下载的目录 (default ".")
-n, --name stringArray   仅下载匹配文件名的工件
```

### `gh run list [flags]`

列出最近的工作流运行

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-L, --limit int         Maximum number of runs to fetch (default 20)
-t, --template string   模板化输出
-w, --workflow string   工作流的过滤
```

### `gh run rerun [<run-id>]`

重新运行失败的运行

### `gh run view [<run-id>] [flags]`

查看工作流运行的摘要

```
    --exit-status       Exit with non-zero status if run failed
-j, --job string        查看一个特定的 job ID
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
    --log               查看 完整的日志
    --log-failed        查看运行失败的日志
-t, --template string   模板化输出
-v, --verbose           展示 job 步骤
-w, --web               浏览器打开
```

### `gh run watch <run-id> [flags]`

观察跑步直到完成，并显示其进度

```
    --exit-status    运行失败，退出代码 非零
-i, --interval int   刷新的时间间隙 (default 3)
```

## `gh secret <command>`

管理 GitHub 机密

### `gh secret list [flags]`

列出秘密

```
-e, --env string   环境的机密
-o, --org string   组织的机密
-u, --user         用户的机密
```

### `gh secret remove <secret-name> [flags]`

揭秘

```
-e, --env string   移除环境的机密
-o, --org string   移除组织的机密
-u, --user         移除用户的机密
```

### `gh secret set <secret-name> [flags]`

创建或更新机密

```
-b, --body string                         机密内容 (reads from standard input if not specified)
-e, --env environment                     设置发布环境的机密
-f, --env-file file                       加载 secret 名与值 (dotenv 格式文件）
    --no-store                            打印 encrypted, base64-encoded 值，而不是在 Github 上存储
-o, --org organization                    设置组织的机密
-r, --repos repositories                  能访问到一个组织或用户机密，列出这样的存储库
-u, --user                                设置用户的机密
-v, --visibility {all|private|selected}   设置一个组织机密的可见性: {all|private|selected} (default "private")
```

## `gh ssh-key <command>`

管理 SSH 密钥

### `gh ssh-key add [<key-file>] [flags]`

向 GitHub 帐户添加 SSH 密钥

```
-t, --title string   密钥的 标题
```

### `gh ssh-key list`

列出 GitHub 帐户中的 SSH 密钥

## `gh workflow <command>`

查看有关 GitHub Actions 工作流的详细信息

### `gh workflow disable [<workflow-id> | <workflow-name>]`

禁用工作流

### `gh workflow enable [<workflow-id> | <workflow-name>]`

启用工作流

### `gh workflow list [flags]`

列出工作流

```
-a, --all         展示所有，即便是禁用的工作流
-L, --limit int   Maximum number of workflows to fetch (default 50)
```

### `gh workflow run [<workflow-id> | <workflow-name>] [flags]`

为给定工作流，创建 `workflow_dispatch` 事件。

```
-F, --field key=value       key=value 模式的字符串参数，遵守 @ 语法
    --json                  通过 STDIN，读取 JSON 格式的工作流输入
-f, --raw-field key=value   key=value 模式的字符串参数
-r, --ref string            想要运行的 分支与 tag 下的工作流文件
```

### `gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]`

查看工作流摘要

```
-r, --ref string   The branch or tag name which contains the version of the workflow file you'd like to view
-w, --web          浏览器打开
-y, --yaml         查看工作流的 yaml 文件
```

### See also

- [gh](./gh.zh.md)
