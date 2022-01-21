

## gh reference

# gh reference

## `gh actions`

Learn about working with GitHub Actions

## `gh alias <command>`

Create command shortcuts

### `gh alias delete <alias>`

Delete an alias

### `gh alias list`

List your aliases

### `gh alias set <alias> <expansion> [flags]`

Create a shortcut for a gh command

```
-s, --shell   定义个 alias 传递给 shell 解释器，r
````

## `gh api <endpoint> [flags]`

Make an authenticated GitHub API request

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
````

## `gh auth <command>`

Login, logout, and refresh your authentication

### `gh auth login [flags]`

Authenticate with a GitHub host

```
-h, --hostname string   The hostname of the GitHub instance to authenticate with
-s, --scopes strings    Additional authentication scopes for gh to have
-w, --web               Open a browser to authenticate
    --with-token        Read token from standard input
````

### `gh auth logout [flags]`

Log out of a GitHub host

```
-h, --hostname string   The hostname of the GitHub instance to log out of
````

### `gh auth refresh [flags]`

Refresh stored authentication credentials

```
-h, --hostname string   The GitHub host to use for authentication
-s, --scopes strings    Additional authentication scopes for gh to have
````

### `gh auth setup-git [flags]`

Configure git to use GitHub CLI as a credential helper

```
-h, --hostname string   The hostname to configure git for
````

### `gh auth status [flags]`

View authentication status

```
-h, --hostname string   Check a specific hostname's auth status
-t, --show-token        Display the auth token
````

## `gh browse [<number> | <path>] [flags]`

Open the repository in the browser

```
-b, --branch string   Select another branch by passing in the branch name
-c, --commit          Open the last commit
-n, --no-browser      Print destination URL instead of opening the browser
-p, --projects        Open repository projects
-s, --settings        Open repository settings
-w, --wiki            Open repository wiki
````

## `gh codespace`

Connect to and manage your codespaces

### `gh codespace code [flags]`

Open a codespace in Visual Studio Code

```
-c, --codespace string   名字
    --insiders           Use the insiders version of Visual Studio Code
````

### `gh codespace cp [-e] [-r] <sources>... <dest>`

Copy files between local and remote file systems

```
-c, --codespace string   名字
-e, --expand             Expand remote file names on remote shell
-r, --recursive          Recursively copy directories
````

### `gh codespace create [flags]`

Create a codespace

```
-b, --branch string           repository branch
    --idle-timeout duration   allowed inactivity before codespace is stopped, e.g. "10m", "1h"
-m, --machine string          hardware specifications for the VM
-r, --repo string             repository name with owner: user/repo
-s, --status                  show status of post-create command and dotfiles
````

### `gh codespace delete [flags]`

Delete a codespace

```
    --all                Delete all codespaces
-c, --codespace string   名字
    --days N             Delete codespaces older than N days
-f, --force              Skip confirmation for codespaces that contain unsaved changes
-r, --repo repository    Delete codespaces for a repository
````

### `gh codespace list [flags]`

List your codespaces

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-L, --limit int         Maximum number of codespaces to list (default 30)
-t, --template string   模板化输出
````

### `gh codespace logs [flags]`

Access codespace logs

```
-c, --codespace string   名字
-f, --follow             日志跟随滚动
````

### `gh codespace ports [flags]`

List ports in a codespace

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
````

#### `gh codespace ports forward <remote-port>:<local-port>...`

Forward ports

#### `gh codespace ports visibility <port>:{public|private|org}...`

Change the visibility of the forwarded port

### `gh codespace ssh [<flags>...] [-- <ssh-flags>...] [<command>]`

SSH into a codespace

```
-c, --codespace string    名字
-d, --debug               Log debug data to a file
    --debug-file string   文件日志的路径
    --profile string      所使用的 SSH profile 名称
    --server-port int     SSH server port number (0 => pick unused)
````

### `gh codespace stop [flags]`

Stop a running codespace

```
-c, --codespace string   名字
````

## `gh completion -s <shell>`

Generate shell completion scripts

```
-s, --shell string   Shell type: {bash|zsh|fish|powershell}
````

## `gh config <command>`

Manage configuration for gh

### `gh config get <key> [flags]`

Print the value of a given configuration key

```
-h, --host string   Get per-host setting
````

### `gh config list [flags]`

Print a list of configuration keys and values

```
-h, --host string   Get per-host configuration
````

### `gh config set <key> <value> [flags]`

Update configuration with a value for the given key

```
-h, --host string   Set per-host setting
````

## `gh extension`

Manage gh extensions

### `gh extension create [<name>] [flags]`

Create a new extension

```
--precompiled string   Create a precompiled extension. Possible values: go, other
````

### `gh extension install <repository>`

Install a gh extension from a repository

### `gh extension list`

List installed extension commands

### `gh extension remove <name>`

Remove an installed extension

### `gh extension upgrade {<name> | --all} [flags]`

Upgrade installed extensions

```
--all     Upgrade all extensions
--force   Force upgrade extension
````

## `gh gist <command>`

Manage gists

### `gh gist clone <gist> [<directory>] [-- <gitflags>...]`

Clone a gist locally

### `gh gist create [<filename>... | -] [flags]`

Create a new gist

```
-d, --desc string       A description for this gist
-f, --filename string   Provide a filename to be used when reading from standard input
-p, --public            List the gist publicly (default: secret)
-w, --web               Open the web browser with created gist
````

### `gh gist delete {<id> | <url>}`

Delete a gist

### `gh gist edit {<id> | <url>} [flags]`

Edit one of your gists

```
-a, --add string        Add a new file to the gist
-f, --filename string   Select a file to edit
````

### `gh gist list [flags]`

List your gists

```
-L, --limit int   Maximum number of gists to fetch (default 10)
    --public      Show only public gists
    --secret      Show only secret gists
````

### `gh gist view [<id> | <url>] [flags]`

View a gist

```
-f, --filename string   Display a single file from the gist
    --files             List file names from the gist
-r, --raw               Print raw instead of rendered gist contents
-w, --web               Open gist in the browser
````

## `gh gpg-key <command>`

Manage GPG keys

### `gh gpg-key add [<key-file>]`

Add a GPG key to your GitHub account

### `gh gpg-key list`

Lists GPG keys in your GitHub account

## `gh issue <command>`

Manage issues

### `gh issue close {<number> | <url>}`

Close issue

### `gh issue comment {<number> | <url>} [flags]`

Create a new issue comment

```
-b, --body string      Supply a body. Will prompt for one otherwise.
-F, --body-file file   读取文件，输入主体内容 (use "-" to read from standard input)
-e, --editor           Add body using editor
-w, --web              Add body in browser
````

### `gh issue create [flags]`

Create a new issue

```
-a, --assignee login   Assign people by their login. Use "@me" to self-assign.
-b, --body string      Supply a body. Will prompt for one otherwise.
-F, --body-file file   读取文件，输入主体内容 (use "-" to read from standard input)
-l, --label name       添加标签
-m, --milestone name   Add the issue to a milestone by name
-p, --project name     Add the issue to projects by name
    --recover string   Recover input from a failed run of create
-t, --title string     Supply a title. Will prompt for one otherwise.
-w, --web              Open the browser to create an issue
````

### `gh issue delete {<number> | <url>}`

Delete issue

### `gh issue edit {<number> | <url>} [flags]`

Edit an issue

```
    --add-assignee login      Add assigned users by their login. Use "@me" to assign yourself.
    --add-label name          添加标签
    --add-project name        Add the issue to projects by name
-b, --body string             设置新的主体内容.
-F, --body-file file          读取文件，输入主体内容 (use "-" to read from standard input)
-m, --milestone name          Edit the milestone the issue belongs to by name
    --remove-assignee login   Remove assigned users by their login. Use "@me" to unassign yourself.
    --remove-label name       移除 name 标签
    --remove-project name     Remove the issue from projects by name
-t, --title string            设置新的标题.
````

### `gh issue list [flags]`

List and filter issues in this repository

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
````

### `gh issue reopen {<number> | <url>}`

Reopen issue

### `gh issue status [flags]`

Show status of relevant issues

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
````

### `gh issue transfer {<number> | <url>} <destination-repo>`

Transfer issue to another repository

### `gh issue view {<number> | <url>} [flags]`

View an issue

```
-c, --comments          View issue comments
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               Open an issue in the browser
````

## `gh pr <command>`

Manage pull requests

### `gh pr checkout {<number> | <url> | <branch>} [flags]`

Check out a pull request in git

```
-b, --branch string        Local branch name to use (default: the name of the head branch)
    --detach               Checkout PR with a detached HEAD
-f, --force                Reset the existing local branch to the latest state of the pull request
    --recurse-submodules   Update all submodules after checkout
````

### `gh pr checks [<number> | <url> | <branch>] [flags]`

Show CI status for a single pull request

```
-w, --web   Open the web browser to show details about checks
````

### `gh pr close {<number> | <url> | <branch>} [flags]`

Close a pull request

```
-d, --delete-branch   Delete the local and remote branch after close
````

### `gh pr comment [<number> | <url> | <branch>] [flags]`

Create a new pr comment

```
-b, --body string      Supply a body. Will prompt for one otherwise.
-F, --body-file file   读取文件，输入主体内容 (use "-" to read from standard input)
-e, --editor           Add body using editor
-w, --web              Add body in browser
````

### `gh pr create [flags]`

Create a pull request

```
-a, --assignee login       Assign people by their login. Use "@me" to self-assign.
-B, --base branch          要合并到的分支
-b, --body string          PR 的主体内容
-F, --body-file file       读取文件，输入主体内容
-d, --draft                草稿版
-f, --fill                 不用提示，使用 commit 的信息填入 title/body
-H, --head branch          包含你 commits 的分支 (default: current branch)
-l, --label name           添加标签
-m, --milestone name       Add the pull request to a milestone by name
    --no-maintainer-edit   Disable maintainer's ability to modify pull request
-p, --project name         将 pull request 添加到 name 项目
    --recover string       Recover input from a failed run of create
-r, --reviewer handle      PR 审查人员
-t, --title string         添加 标题
-w, --web                  浏览器打开
````

### `gh pr diff [<number> | <url> | <branch>] [flags]`

View changes in a pull request

```
--color string   在 diff 输出中，使用颜色: {always|never|auto} (default "auto")
--patch          以 patch 格式，展示 diff 
````

### `gh pr edit [<number> | <url> | <branch>] [flags]`

Edit a pull request

```
    --add-assignee login      Add assigned users by their login. Use "@me" to assign yourself.
    --add-label name          添加标签
    --add-project name        将 pull request 添加到 name 项目
    --add-reviewer login      通过 login ，添加审查人员.
-B, --base branch             更改 PR 的基分支
-b, --body string             设置新的主体内容.
-F, --body-file file          读取文件，输入主体内容 (use "-" to read from standard input)
-m, --milestone name          编辑 name 里程牌
    --remove-assignee login   Remove assigned users by their login. Use "@me" to unassign yourself.
    --remove-label name       移除 name 标签
    --remove-project name     移除 name 项目的 PR
    --remove-reviewer login   通过 login ，移除审查人员.
-t, --title string            设置新的标题.
````

### `gh pr list [flags]`

List and filter pull requests in this repository

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
````

### `gh pr merge [<number> | <url> | <branch>] [flags]`

Merge a pull request

```
    --admin            即便条件不达标，用管理员权限合并
    --auto             条件符合，自动合并
-b, --body text        合并的主体内容
-F, --body-file file   读取文件，输入主体内容 (use "-" to read from standard input)
-d, --delete-branch    合并后，删除本地与远程分支
    --disable-auto     禁止自动合并
-m, --merge            合并
-r, --rebase           变基
-s, --squash           将多个提交变成一个，再合并
-t, --subject text     合并提交的主题
````

### `gh pr ready [<number> | <url> | <branch>]`

Mark a pull request as ready for review

### `gh pr reopen {<number> | <url> | <branch>}`

Reopen a pull request

### `gh pr review [<number> | <url> | <branch>] [flags]`

Add a review to a pull request

```
-a, --approve           批准 pull request
-b, --body string       指定一个审查的主体内容
-F, --body-file file    读取文件，输入主体内容 (use "-" to read from standard input)
-c, --comment           给出评论
-r, --request-changes   要求 PR 修改
````

### `gh pr status [flags]`

Show status of relevant pull requests

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
````

### `gh pr view [<number> | <url> | <branch>] [flags]`

View a pull request

```
-c, --comments          查看 pull request 评论
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               浏览器打开
````

## `gh release <command>`

Manage GitHub releases

### `gh release create [<tag>] [<files>...]`

Create a new release

```
    --discussion-category string   开始指定主题分类的讨论
-d, --draft                        一个草稿版本
    --generate-notes               自动生成，release 的 标题与笔记
-n, --notes string                 Release 笔记
-F, --notes-file file              用文件，读笔记 (use "-" to read from standard input)
-p, --prerelease                   预览版
    --target branch                指定的分支或是完整的 commit SHA (default: main branch)
-t, --title string                 Release 标题
````

### `gh release delete <tag> [flags]`

Delete a release

```
-y, --yes   跳过提示
````

### `gh release download [<tag>] [flags]`

Download release assets

```
-A, --archive format        下载的格式 (zip or tar.gz)
-D, --dir string            下载的位置 (default ".")
-p, --pattern stringArray   只下载符合 glob 匹配模式的资源
````

### `gh release list [flags]`

List releases in a repository

```
-L, --limit int   Maximum number of items to fetch (default 30)
````

### `gh release upload <tag> <files>... [flags]`

Upload assets to a release

```
--clobber   覆盖同名资源
````

### `gh release view [<tag>] [flags]`

View information about a release

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               浏览器打开
````

## `gh repo <command>`

Create, clone, fork, and view repositories

### `gh repo archive [<repository>] [flags]`

Archive a repository

```
-y, --confirm   跳过提示
````

### `gh repo clone <repository> [<directory>] [-- <gitflags>...]`

Clone a repository locally

### `gh repo create [<name>] [flags]`

Create a new repository

```
-c, --clone                 Clone the new repository to the current directory
-d, --description string    存储库的描述
    --disable-issues        Disable issues in the new repository
    --disable-wiki          Disable wiki in the new repository
-g, --gitignore string      Specify a gitignore template for the repository
-h, --homepage URL          主页URL
    --internal              Make the new repository internal
-l, --license string        Specify an Open Source License for the repository
    --private               Make the new repository private
    --public                Make the new repository public
    --push                  Push local commits to the new repository
-r, --remote string         Specify remote name for the new repository
-s, --source string         Specify path to local repository to use as source
-t, --team name             The name of the organization team to be granted access
-p, --template repository   Make the new repository based on a template repository
````

### `gh repo delete [<repository>] [flags]`

Delete a repository

```
--confirm   直接通过提示
````

### `gh repo edit [<repository>] [flags]`

Edit repository settings

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
````

### `gh repo fork [<repository>] [-- <gitflags>...] [flags]`

Create a fork of a repository

```
--clone                Clone the fork {true|false}
--org string           在一个组织内，创建副本
--remote               要添加远程（上级）存储库吗 {true|false}
--remote-name string   Specify a name for a fork's new remote. (default "origin")
````

### `gh repo list [<owner>] [flags]`

List repositories owned by user or organization

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
````

### `gh repo rename [<new-name>] [flags]`

Rename a repository

```
-y, --confirm   跳过提示，直接确定
````

### `gh repo sync [<destination-repository>] [flags]`

Sync a repository

```
-b, --branch string   Branch to sync (default: main branch)
    --force           Hard reset the branch of the destination repository to match the source repository
-s, --source string   Source repository
````

### `gh repo view [<repository>] [flags]`

View a repository

```
-b, --branch string     显示特定分支
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-t, --template string   模板化输出
-w, --web               浏览器打开
````

## `gh run <command>`

View details about workflow runs

### `gh run cancel [<run-id>]`

Cancel a workflow run

### `gh run download [<run-id>] [flags]`

Download artifacts generated by a workflow run

```
-D, --dir string         下载的目录 (default ".")
-n, --name stringArray   仅下载匹配文件名的工件
````

### `gh run list [flags]`

List recent workflow runs

```
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
-L, --limit int         Maximum number of runs to fetch (default 20)
-t, --template string   模板化输出
-w, --workflow string   工作流的过滤
````

### `gh run rerun [<run-id>]`

Rerun a failed run

### `gh run view [<run-id>] [flags]`

View a summary of a workflow run

```
    --exit-status       Exit with non-zero status if run failed
-j, --job string        查看一个特定的 job ID
-q, --jq expression     jq 表达式，过滤 JSON 输出
    --json fields       JSON 输出特殊字段
    --log               查看 完整的日志
    --log-failed        View the log for any failed steps in a run or specific job
-t, --template string   模板化输出
-v, --verbose           展示 job 步骤
-w, --web               浏览器打开
````

### `gh run watch <run-id> [flags]`

Watch a run until it completes, showing its progress

```
    --exit-status    运行失败，退出代码 非零
-i, --interval int   刷新的时间间隙 (default 3)
````

## `gh secret <command>`

Manage GitHub secrets

### `gh secret list [flags]`

List secrets

```
-e, --env string   环境的机密
-o, --org string   组织的机密
-u, --user         用户的机密
````

### `gh secret remove <secret-name> [flags]`

Remove secrets

```
-e, --env string   移除环境的机密
-o, --org string   移除组织的机密
-u, --user         移除用户的机密
````

### `gh secret set <secret-name> [flags]`

Create or update secrets

```
-b, --body string                         机密内容 (reads from standard input if not specified)
-e, --env environment                     设置发布环境的机密
-f, --env-file file                       加载 secret 名与值 (dotenv 格式文件）
    --no-store                            打印 encrypted, base64-encoded 值，而不是在 Github 上存储
-o, --org organization                    设置组织的机密
-r, --repos repositories                  能访问到一个组织或用户机密，列出这样的存储库
-u, --user                                设置用户的机密
-v, --visibility {all|private|selected}   设置一个组织机密的可见性: {all|private|selected} (default "private")
````

## `gh ssh-key <command>`

Manage SSH keys

### `gh ssh-key add [<key-file>] [flags]`

Add an SSH key to your GitHub account

```
-t, --title string   密钥的 标题
````

### `gh ssh-key list`

Lists SSH keys in your GitHub account

## `gh workflow <command>`

View details about GitHub Actions workflows

### `gh workflow disable [<workflow-id> | <workflow-name>]`

Disable a workflow

### `gh workflow enable [<workflow-id> | <workflow-name>]`

Enable a workflow

### `gh workflow list [flags]`

List workflows

```
-a, --all         展示所有，即便是禁用的工作流
-L, --limit int   Maximum number of workflows to fetch (default 50)
````

### `gh workflow run [<workflow-id> | <workflow-name>] [flags]`

Run a workflow by creating a workflow_dispatch event

```
-F, --field key=value       Add a string parameter in key=value format, respecting @ syntax
    --json                  Read workflow inputs as JSON via STDIN
-f, --raw-field key=value   Add a string parameter in key=value format
-r, --ref string            The branch or tag name which contains the version of the workflow file you'd like to run
````

### `gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]`

View the summary of a workflow

```
-r, --ref string   The branch or tag name which contains the version of the workflow file you'd like to view
-w, --web          浏览器打开
-y, --yaml         查看工作流的 yaml 文件
````



### See also

* [gh](./gh)
