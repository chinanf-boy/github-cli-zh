## gh environment

GH\_令牌，GITHUB\_令牌（按优先顺序）：GITHUB的身份验证令牌。com API请求。设置此选项可避免提示进行身份验证，并优先于以前存储的凭据。

GH_ENTERPRISE_TOKEN，GITHUB_ENTERPRISE_TOKEN（按优先顺序）：用于向GITHUB ENTERPRISE发出API请求的身份验证令牌。设置此选项时，还要设置GH\_主机。

GH_HOST：为命令指定GitHub主机名，否则这些命令在不在现有存储库的上下文中时将假定为“GitHub.com”主机。

GH_REPO：在“目录”中指定GitHub存储库[HOST/]所有者/REPO”格式，用于在本地存储库上运行的命令。

GH\_编辑器、GIT\_编辑器、可视编辑器、编辑器（按优先顺序）：用于编写文本的编辑器工具。

GHU浏览器，浏览器（按优先顺序）：用于打开链接的web浏览器。

调试：设置为任何值以启用标准错误的详细输出。包括值“api”或“oauth”，以打印有关HTTP请求或身份验证流的详细信息。

GH\_寻呼机，寻呼机（按优先顺序）：发送标准输出的终端寻呼程序，例如“less”。

GLAMOUR\_样式：用于渲染降价的样式。看见<https://github.com/charmbracelet/glamour#styles>

无颜色：设置为任何值以避免打印颜色输出的ANSI转义序列。

CLICOLOR:设置为“0”以禁用在输出中打印ANSI颜色。

CLICOLOR_FORCE：设置为“0”以外的值，以保持输出中的ANSI颜色，即使输出是通过管道传输的。

GH_FORCE_TTY：设置为任何值，以强制终端样式输出，即使输出被重定向。当该值为数字时，它将被解释为视口中可用的列数。当该值为百分比时，将根据当前视口中可用的列数应用该值。

GH_NO_UPDATE_NOTIFIER：设置为任何值以禁用更新通知。默认情况下，gh每24小时检查一次新版本，如果发现较新版本，则会显示标准错误的升级通知。

GH_CONFIG_DIR：GH将存储配置文件的目录。默认值：“$XDG\\u CONFIG\\u HOME/gh”或“$HOME/.CONFIG/gh”。

### See also

-   [gh](./gh)
