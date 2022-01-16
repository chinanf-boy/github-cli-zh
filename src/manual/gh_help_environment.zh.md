## gh environment

`GH_TOKEN`, `GITHUB_TOKEN`（按优先顺序）：github.com API 请求的身份验证令牌。设置此选项可避免提示进行身份验证，并优先于以前存储的凭据。

`GH_ENTERPRISE_TOKEN`，`GITHUB_ENTERPRISE_TOKEN`（按优先顺序）：用于向 GITHUB ENTERPRISE 发出 API 请求的身份验证令牌。设置此选项时，还要设置 GH_HOST。

`GH_HOST`：为命令指定 GitHub 主机名，不在现有存储库的上下文中时，假定为"github.com"主机。

`GH_REPO`：指定 GitHub 存储库("[HOST/]OWNER/REPO"格式)，用于在本地存储库上运行的命令。

`GH_EDITOR, GIT_EDITOR, VISUAL, EDITOR`（按优先顺序）：用于编写文本的编辑器工具。

`GH_BROWSER, BROWSER`（按优先顺序）：用于打开链接的 web 浏览器。

`DEBUG`：可以设为任何值，以启用标准错误的详细输出。包括值`api`
or `oauth`，以打印有关 HTTP 请求或身份验证流的详细信息。

`GH_PAGER, PAGER`（按优先顺序）：发送标准输出的终端寻呼程序，例如: `less`。

`GLAMOUR_STYLE`：用于渲染 Markdown 的样式。<https://github.com/charmbracelet/glamour#styles>

`NO_COLOR`：可以设为任何值，以避免打印颜色输出的 ANSI 转义序列。

`CLICOLOR`：设置为`0`，以禁用在输出中打印 ANSI 颜色。

`CLICOLOR_FORCE`：设置`0`以外的值，以保持输出中的 ANSI 颜色，即使输出是通过管道传输的。

`GH_FORCE_TTY`：可以设为任何值，以强制终端样式输出，即使输出被重定向。当该值为数字时，它将被解释为 viewport 中可用的列数。当该值为百分比时，将根据当前视口中，可用的列数，来应用该值。

`GH_NO_UPDATE_NOTIFIER`：可以设为任何值，以禁用更新通知。默认情况下，gh 每 24 小时检查一次新版本，如果发现较新版本，则会显示标准错误的升级通知。

`GH_CONFIG_DIR`：GH 将存储配置文件的目录。默认值：`$XDG_CONFIG_HOME/gh` 和 `$HOME/.config/gh`

### See also

- [gh](./gh.zh.md)
