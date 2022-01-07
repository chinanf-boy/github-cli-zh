

## gh extension

GitHub CLI扩展是提供附加gh命令的存储库。

扩展存储库的名称必须以“gh-”开头，并且必须包含同名的可执行文件。所有参数都传递给`gh <extname>`调用将被转发到`gh-<extname>`扩展的可执行文件。

扩展不能覆盖任何核心gh命令。

请参阅上的可用扩展名列表<https://github.com/topics/gh-extension>

### Commands

-   [gh extension create](./gh_extension_create)
-   [gh extension install](./gh_extension_install)
-   [gh extension list](./gh_extension_list)
-   [gh extension remove](./gh_extension_remove)
-   [gh extension upgrade](./gh_extension_upgrade)

### See also

-   [gh](./gh)
