## gh reference

# gh reference

## `gh actions`

了解如何使用GitHub操作

## `gh alias <command>`

创建命令快捷方式

### `gh alias delete <alias>`

删除别名

### `gh alias list`

列出你的别名

### `gh alias set <alias> <expansion> [flags]`

为gh命令创建快捷方式

```
-s, --shell   定义个 alias 传递给 shell 解释器，r
```

## `gh api <endpoint> [flags]`

发出经过身份验证的GitHub API请求

```
    --cache duration        Cache the response, e.g. "3600s", "60m", "1h"
-F, --field key=value       Add a typed parameter in key=value format
-H, --header key:value      Add a HTTP request header 格式是 key=value
    --hostname string       The GitHub hostname for the request (default "github.com")
-i, --include               Include HTTP response headers in the output
    --input file            The file to use as body for the HTTP request (use "-" to read from standard input)
-q, --jq string             Query to select values from the response using jq syntax
-X, --method string         The HTTP method for the request (default "GET")
    --paginate              Make additional HTTP requests to fetch all pages of results
-p, --preview strings       Opt into GitHub API previews
-f, --raw-field key=value   Add a string parameter in key=value format
    --silent                Do not print the response body
-t, --template string       Format the response using a Go template
```

## `gh auth <command>`

登录、注销和刷新您的身份验证

### `gh auth login [flags]`

通过GitHub主机进行身份验证

```
-h, --hostname string   The hostname of the GitHub instance to authenticate with
-s, --scopes strings    Additional authentication scopes for gh to have
-w, --web               Open a browser to authenticate
    --with-token        Read token from standard input
```

### `gh auth logout [flags]`

注销GitHub主机

```
-h, --hostname string   The hostname of the GitHub instance to log out of
```

### `gh auth refresh [flags]`

刷新存储的身份验证凭据

```
-h, --hostname string   The GitHub host to use for authentication
-s, --scopes strings    Additional authentication scopes for gh to have
```

### `gh auth setup-git [flags]`

配置git以将GitHub CLI用作凭据帮助器

```
-h, --hostname string   The hostname to configure git for
```

### `gh auth status [flags]`

查看身份验证状态

```
-h, --hostname string   Check a specific hostname's auth status
-t, --show-token        Display the auth token
```

## `gh browse [<number> | <path>] [flags]`

在浏览器中打开存储库

```
-b, --branch string   Select another branch by passing in the branch name
-c, --commit          Open the last commit
-n, --no-browser      Print destination URL instead of opening the browser
-p, --projects        Open repository projects
-s, --settings        Open repository settings
-w, --wiki            Open repository wiki
```

## `gh codespace`

连接并管理您的代码空间

### `gh codespace code [flags]`

在Visual Studio代码中打开代码空间

```
-c, --codespace string   名字
    --insiders           Use the insiders version of Visual Studio Code
```

### `gh codespace cp [-e] [-r] <sources>... <dest>`

在本地和远程文件系统之间复制文件

```
-c, --codespace string   名字
-e, --expand             Expand remote file names on remote shell
-r, --recursive          Recursively copy directories
```

### `gh codespace create [flags]`

创建一个代码空间

```
-b, --branch string           repository branch
    --idle-timeout duration   allowed inactivity before codespace is stopped, e.g. "10m", "1h"
-m, --machine string          hardware specifications for the VM
-r, --repo string             repository name with owner: user/repo
-s, --status                  show status of post-create command and dotfiles
```

### `gh codespace delete [flags]`

删除代码空间

```
    --all                Delete all codespaces
-c, --codespace string   名字
    --days N             Delete codespaces older than N days
-f, --force              Skip confirmation for codespaces that contain unsaved changes
-r, --repo repository    Delete codespaces for a repository
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

SSH到一个代码空间

```
-c, --codespace string    名字
-d, --debug               Log debug data to a file
    --debug-file string   文件日志的路径
    --profile string      所使用的 SSH profile 名称
    --server-port int     SSH server port number (0 => pick unused)
```

### `gh codespace stop [flags]`

停止运行代码空间

```
-c, --codespace string   名字
```

## `gh completion -s <shell>`

生成shell完成脚本

```
-s, --shell string   Shell type: {bash|zsh|fish|powershell}
```

## `gh config <command>`

管理gh的配置

### `gh config get <key> [flags]`

打印给定配置密钥的值

```
-h, --host string   Get per-host setting
```

### `gh config list [flags]`

打印配置键和值的列表

```
-h, --host string   Get per-host configuration
```

### `gh config set <key> <value> [flags]`

使用给定密钥的值更新配置

```
-h, --host string   Set per-host setting
```

## `gh extension`

管理gh扩展

### `gh extension create [<name>] [flags]`

创建一个新的扩展名

```
--precompiled string   Create a precompiled extension. Possible values: go, other
```

### `gh extension install <repository>`

从存储库安装gh扩展

### `gh extension list`

列出已安装的扩展命令

### `gh extension remove <name>`

删除已安装的扩展

### `gh extension upgrade {<name> | --all} [flags]`

升级已安装的扩展

```
--all     Upgrade all extensions
--force   Force upgrade extension
```

## `gh gist <command>`

管理注册会计师

### `gh gist clone <gist> [<directory>] [-- <gitflags>...]`

本地克隆要点

### `gh gist create [<filename>... | -] [flags]`

创造一个新的要点

```
-d, --desc string       A description for this gist
-f, --filename string   Provide a filename to be used when reading from standard input
-p, --public            List the gist publicly (default: secret)
-w, --web               Open the web browser with created gist
```

### `gh gist delete {<id> | <url>}`

删除要点

### `gh gist edit {<id> | <url>} [flags]`

编辑一个GIST

```
-a, --add string        Add a new file to the gist
-f, --filename string   Select a file to edit
```

### `gh gist list [flags]`

列出你的注册医生

```
-L, --limit int   Maximum number of gists to fetch (default 10)
    --public      Show only public gists
    --secret      Show only secret gists
```

### `gh gist view [<id> | <url>] [flags]`

要点

```
-f, --filename string   Display a single file from the gist
    --files             List file names from the gist
-r, --raw               Print raw instead of rendered gist contents
-w, --web               Open gist in the browser
```

## `gh gpg-key <command>`

管理GPG密钥

### `gh gpg-key add [<key-file>]`

将GPG密钥添加到GitHub帐户

### `gh gpg-key list`

列出GitHub帐户中的GPG密钥

## `gh issue <command>`

管理问题

### `gh issue close {<number> | <url>}`

结案

### `gh issue comment {<number> | <url>} [flags]`

创建新的问题注释

```
-b, --body string      Supply a body. Will prompt for one otherwise.
-F, --body-file file   Read body text from file (use "-" to read from standard input)
-e, --editor           Add body using editor
-w, --web              Add body in browser
```

### `gh issue create [flags]`

创刊

```
-a, --assignee login   Assign people by their login. Use "@me" to self-assign.
-b, --body string      Supply a body. Will prompt for one otherwise.
-F, --body-file file   Read body text from file (use "-" to read from standard input)
-l, --label name       Add labels by name
-m, --milestone name   Add the issue to a milestone by name
-p, --project name     Add the issue to projects by name
    --recover string   Recover input from a failed run of create
-t, --title string     Supply a title. Will prompt for one otherwise.
-w, --web              Open the browser to create an issue
```

### `gh issue delete {<number> | <url>}`

删除问题

### `gh issue edit {<number> | <url>} [flags]`

编辑问题

```
    --add-assignee login      Add assigned users by their login. Use "@me" to assign yourself.
    --add-label name          Add labels by name
    --add-project name        Add the issue to projects by name
-b, --body string             Set the new body.
-F, --body-file file          Read body text from file (use "-" to read from standard input)
-m, --milestone name          Edit the milestone the issue belongs to by name
    --remove-assignee login   Remove assigned users by their login. Use "@me" to unassign yourself.
    --remove-label name       Remove labels by name
    --remove-project name     Remove the issue from projects by name
-t, --title string            Set the new title.
```

### `gh issue list [flags]`

列出并筛选此存储库中的问题

```
-a, --assignee string    Filter by assignee
-A, --author string      Filter by author
-q, --jq expression      jq 表达式，过滤 JSON 输出
    --json fields        JSON 输出特殊字段
-l, --label strings      Filter by labels
-L, --limit int          Maximum number of issues to fetch (default 30)
    --mention string     Filter by mention
-m, --milestone number   Filter by milestone number or `title`
-S, --search query       Search issues with query
-s, --state string       Filter by state: {open|closed|all} (default "open")
-t, --template string    模板化输出
-w, --web                Open the browser to list the issue(s)
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

查看git中的pull请求

```
-b, --branch string        Local branch name to use (default: the name of the head branch)
    --detach               Checkout PR with a detached HEAD
-f, --force                Reset the existing local branch to the latest state of the pull request
    --recurse-submodules   Update all submodules after checkout
```

### `gh pr checks [<number> | <url> | <branch>] [flags]`

显示单个拉动请求的CI状态

```
-w, --web   Open the web browser to show details about checks
```

### `gh pr close {<number> | <url> | <branch>} [flags]`

关闭拉取请求

```
-d, --delete-branch   Delete the local and remote branch after close
```

### `gh pr comment [<number> | <url> | <branch>] [flags]`

创建新的公关评论

```
-b, --body string      Supply a body. Will prompt for one otherwise.
-F, --body-file file   Read body text from file (use "-" to read from standard input)
-e, --editor           Add body using editor
-w, --web              Add body in browser
```

### `gh pr create [flags]`

创建拉取请求

```
-a, --assignee login       Assign people by their login. Use "@me" to self-assign.
-B, --base branch          The branch into which you want your code merged
-b, --body string          Body for the pull request
-F, --body-file file       Read body text from file
-d, --draft                Mark pull request as a draft
-f, --fill                 Do not prompt for title/body and just use commit info
-H, --head branch          The branch that contains commits for your pull request (default: current branch)
-l, --label name           Add labels by name
-m, --milestone name       Add the pull request to a milestone by name
    --no-maintainer-edit   Disable maintainer's ability to modify pull request
-p, --project name         Add the pull request to projects by name
    --recover string       Recover input from a failed run of create
-r, --reviewer handle      Request reviews from people or teams by their handle
-t, --title string         Title for the pull request
-w, --web                  Open the web browser to create a pull request
```

### `gh pr diff [<number> | <url> | <branch>] [flags]`

查看拉取请求中的更改

```
--color string   Use color in diff output: {always|never|auto} (default "auto")
--patch          Display diff in patch format
```

### `gh pr edit [<number> | <url> | <branch>] [flags]`

编辑拉取请求

```
    --add-assignee login      Add assigned users by their login. Use "@me" to assign yourself.
    --add-label name          Add labels by name
    --add-project name        Add the pull request to projects by name
    --add-reviewer login      Add reviewers by their login.
-B, --base branch             Change the base branch for this pull request
-b, --body string             Set the new body.
-F, --body-file file          Read body text from file (use "-" to read from standard input)
-m, --milestone name          Edit the milestone the pull request belongs to by name
    --remove-assignee login   Remove assigned users by their login. Use "@me" to unassign yourself.
    --remove-label name       Remove labels by name
    --remove-project name     Remove the pull request from projects by name
    --remove-reviewer login   Remove reviewers by their login.
-t, --title string            Set the new title.
```

### `gh pr list [flags]`

列出并筛选此存储库中的请求

```
-a, --assignee string   Filter by assignee
-A, --author string     Filter by author
-B, --base string       Filter by base branch
-d, --draft             Filter by draft state
-H, --head string       Filter by head branch
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-l, --label strings     Filter by labels
-L, --limit int         Maximum number of items to fetch (default 30)
-S, --search query      Search pull requests with query
-s, --state string      Filter by state: {open|closed|merged|all} (default "open")
-t, --template string   模板化输出
-w, --web               Open the browser to list the pull requests
```

### `gh pr merge [<number> | <url> | <branch>] [flags]`

合并拉取请求

```
    --admin            Use administrator privileges to merge a pull request that does not meet requirements
    --auto             Automatically merge only after necessary requirements are met
-b, --body text        Body text for the merge commit
-F, --body-file file   Read body text from file (use "-" to read from standard input)
-d, --delete-branch    Delete the local and remote branch after merge
    --disable-auto     Disable auto-merge for this pull request
-m, --merge            Merge the commits with the base branch
-r, --rebase           Rebase the commits onto the base branch
-s, --squash           Squash the commits into one commit and merge it into the base branch
-t, --subject text     Subject text for the merge commit
```

### `gh pr ready [<number> | <url> | <branch>]`

将拉动请求标记为已准备好进行审查

### `gh pr reopen {<number> | <url> | <branch>}`

重新打开拉取请求

### `gh pr review [<number> | <url> | <branch>] [flags]`

向拉取请求添加审阅

```
-a, --approve           Approve pull request
-b, --body string       Specify the body of a review
-F, --body-file file    Read body text from file (use "-" to read from standard input)
-c, --comment           Comment on a pull request
-r, --request-changes   Request changes on a pull request
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
-c, --comments          View pull request comments
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               Open a pull request in the browser
```

## `gh release <command>`

管理GitHub发布

### `gh release create [<tag>] [<files>...]`

创建一个新版本

```
    --discussion-category string   Start a discussion of the specified category
-d, --draft                        Save the release as a draft instead of publishing it
    --generate-notes               Automatically generate title and notes for the release
-n, --notes string                 Release notes
-F, --notes-file file              Read release notes from file (use "-" to read from standard input)
-p, --prerelease                   Mark the release as a prerelease
    --target branch                Target branch or full commit SHA (default: main branch)
-t, --title string                 Release title
```

### `gh release delete <tag> [flags]`

删除发布

```
-y, --yes   Skip the confirmation prompt
```

### `gh release download [<tag>] [flags]`

下载发布资产

```
-A, --archive format        Download the source code archive in the specified format (zip or tar.gz)
-D, --dir string            The directory to download files into (default ".")
-p, --pattern stringArray   Download only assets that match a glob pattern
```

### `gh release list [flags]`

在存储库中列出发布

```
-L, --limit int   Maximum number of items to fetch (default 30)
```

### `gh release upload <tag> <files>... [flags]`

将资产上载到发布

```
--clobber   Overwrite existing assets of the same name
```

### `gh release view [<tag>] [flags]`

查看有关发布的信息

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               Open the release in the browser
```

## `gh repo <command>`

创建、克隆、分叉和查看存储库

### `gh repo archive [<repository>] [flags]`

归档存储库

```
-y, --confirm   Skip the confirmation prompt
```

### `gh repo clone <repository> [<directory>] [-- <gitflags>...]`

在本地克隆存储库

### `gh repo create [<name>] [flags]`

创建一个新的存储库

```
-c, --clone                 Clone the new repository to the current directory
-d, --description string    Description of the repository
    --disable-issues        Disable issues in the new repository
    --disable-wiki          Disable wiki in the new repository
-g, --gitignore string      Specify a gitignore template for the repository
-h, --homepage URL          Repository home page URL
    --internal              Make the new repository internal
-l, --license string        Specify an Open Source License for the repository
    --private               Make the new repository private
    --public                Make the new repository public
    --push                  Push local commits to the new repository
-r, --remote string         Specify remote name for the new repository
-s, --source string         Specify path to local repository to use as source
-t, --team name             The name of the organization team to be granted access
-p, --template repository   Make the new repository based on a template repository
```

### `gh repo delete [<repository>] [flags]`

删除存储库

```
--confirm   confirm deletion without prompting
```

### `gh repo edit [<repository>] [flags]`

编辑存储库设置

```
    --add-topic strings        Add repository topic
    --allow-forking            Allow forking of an organization repository
    --default-branch name      Set the default branch name for the repository
    --delete-branch-on-merge   Delete head branch when pull requests are merged
-d, --description string       Description of the repository
    --enable-auto-merge        Enable auto-merge functionality
    --enable-issues            Enable issues in the repository
    --enable-merge-commit      Enable merging pull requests via merge commit
    --enable-projects          Enable projects in the repository
    --enable-rebase-merge      Enable merging pull requests via rebase
    --enable-squash-merge      Enable merging pull requests via squashed commit
    --enable-wiki              Enable wiki in the repository
-h, --homepage URL             Repository home page URL
    --remove-topic strings     Remove repository topic
    --template                 Make the repository available as a template repository
    --visibility string        Change the visibility of the repository to {public,private,internal}
```

### `gh repo fork [<repository>] [-- <gitflags>...] [flags]`

创建存储库的分支

```
--clone                Clone the fork {true|false}
--org string           Create the fork in an organization
--remote               Add remote for fork {true|false}
--remote-name string   Specify a name for a fork's new remote. (default "origin")
```

### `gh repo list [<owner>] [flags]`

列出用户或组织拥有的存储库

```
    --archived          Show only archived repositories
    --fork              Show only forks
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-l, --language string   Filter by primary coding language
-L, --limit int         Maximum number of repositories to list (default 30)
    --no-archived       Omit archived repositories
    --private           Show only private repositories
    --public            Show only public repositories
    --source            Show only non-forks
-t, --template string   模板化输出
    --topic string      Filter by topic
```

### `gh repo rename [<new-name>] [flags]`

重命名存储库

```
-y, --confirm   skip confirmation prompt
```

### `gh repo sync [<destination-repository>] [flags]`

同步存储库

```
-b, --branch string   Branch to sync (default: main branch)
    --force           Hard reset the branch of the destination repository to match the source repository
-s, --source string   Source repository
```

### `gh repo view [<repository>] [flags]`

查看存储库

```
-b, --branch string     View a specific branch of the repository
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               Open a repository in the browser
```

## `gh run <command>`

查看有关工作流运行的详细信息

### `gh run cancel [<run-id>]`

取消工作流运行

### `gh run download [<run-id>] [flags]`

下载工作流运行生成的工件

```
-D, --dir string         The directory to download artifacts into (default ".")
-n, --name stringArray   Only download artifacts that match any of the given names
```

### `gh run list [flags]`

列出最近的工作流运行

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-L, --limit int         Maximum number of runs to fetch (default 20)
-t, --template string   模板化输出
-w, --workflow string   Filter runs by workflow
```

### `gh run rerun [<run-id>]`

重新运行失败的运行

### `gh run view [<run-id>] [flags]`

查看工作流运行的摘要

```
    --exit-status       Exit with non-zero status if run failed
-j, --job string        View a specific job ID from a run
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
    --log               View full log for either a run or specific job
    --log-failed        View the log for any failed steps in a run or specific job
-t, --template string   模板化输出
-v, --verbose           Show job steps
-w, --web               Open run in the browser
```

### `gh run watch <run-id> [flags]`

观察跑步直到完成，并显示其进度

```
    --exit-status    Exit with non-zero status if run fails
-i, --interval int   Refresh interval in seconds (default 3)
```

## `gh secret <command>`

管理GitHub机密

### `gh secret list [flags]`

列出秘密

```
-e, --env string   List secrets for an environment
-o, --org string   List secrets for an organization
-u, --user         List a secret for your user
```

### `gh secret remove <secret-name> [flags]`

揭秘

```
-e, --env string   Remove a secret for an environment
-o, --org string   Remove a secret for an organization
-u, --user         Remove a secret for your user
```

### `gh secret set <secret-name> [flags]`

创建或更新机密

```
-b, --body string                         The value for the secret (reads from standard input if not specified)
-e, --env environment                     Set deployment environment secret
-f, --env-file file                       Load secret names and values from a dotenv-formatted file
    --no-store                            Print the encrypted, base64-encoded value instead of storing it on Github
-o, --org organization                    Set organization secret
-r, --repos repositories                  List of repositories that can access an organization or user secret
-u, --user                                Set a secret for your user
-v, --visibility {all|private|selected}   Set visibility for an organization secret: {all|private|selected} (default "private")
```

## `gh ssh-key <command>`

管理SSH密钥

### `gh ssh-key add [<key-file>] [flags]`

向GitHub帐户添加SSH密钥

```
-t, --title string   Title for the new key
```

### `gh ssh-key list`

列出GitHub帐户中的SSH密钥

## `gh workflow <command>`

查看有关GitHub操作工作流的详细信息

### `gh workflow disable [<workflow-id> | <workflow-name>]`

禁用工作流

### `gh workflow enable [<workflow-id> | <workflow-name>]`

启用工作流

### `gh workflow list [flags]`

列出工作流

```
-a, --all         Show all workflows, including disabled workflows
-L, --limit int   Maximum number of workflows to fetch (default 50)
```

### `gh workflow run [<workflow-id> | <workflow-name>] [flags]`

通过创建工作流\\u分派事件来运行工作流

```
-F, --field key=value       Add a string parameter in key=value format, respecting @ syntax
    --json                  Read workflow inputs as JSON via STDIN
-f, --raw-field key=value   Add a string parameter in key=value format
-r, --ref string            The branch or tag name which contains the version of the workflow file you'd like to run
```

### `gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]`

查看工作流摘要

```
-r, --ref string   The branch or tag name which contains the version of the workflow file you'd like to view
-w, --web          Open workflow in the browser
-y, --yaml         View the workflow yaml file
```

### See also

-   [gh](./gh)
