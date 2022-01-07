## gh extension

GitHub CLI 扩展是提供附加 gh 命令的存储库。

扩展存储库的名称必须以`gh-`开头，并且必须包含同名的可执行文件。所有参数都传递给`gh <extname>`，然后转发到`gh-<extname>`扩展的可执行文件。

扩展不能覆盖任何核心 gh 命令。

请参阅上的可用扩展名列表 <https://github.com/topics/gh-extension>

### Commands

- [gh extension create](./gh_extension_create.zh.md)
- [gh extension install](./gh_extension_install.zh.md)
- [gh extension list](./gh_extension_list.zh.md)
- [gh extension remove](./gh_extension_remove.zh.md)
- [gh extension upgrade](./gh_extension_upgrade.zh.md)

### See also

- [gh](./gh.zh.md)
