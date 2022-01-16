## gh mintty

MinTTY 是 Git for Windows 默认附带的终端仿真器。它在 gh 提示用户输入部分，有些已知的问题。

有一些变通方法可以让 gh 与 MinTTY 合作：

- 重新安装 Git for Windows，选中`启用对伪控制台的实验支持（Enable experimental support for pseudo consoles）`。

- 使用不同的终端仿真器和 Git for Windows，如 Windows 终端。您可以从任何终端仿真器运行`C:\Program Files\Git\bin\bash.exe`，在没有 MinTTY 的情况下，继续使用 Git For Windows 中的所有工具。

- 使用 winpty 作为 gh 调用的前缀，例如：`winpty gh auth login`。注意：这可能会导致一些 UI 错误。

### See also

- [gh](./gh.zh.md)
