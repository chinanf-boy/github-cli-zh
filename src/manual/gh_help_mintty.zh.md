

## gh mintty

MinTTY是Git for Windows默认附带的终端仿真器。它已经知道gh提示用户输入的能力存在问题。

有一些变通方法可以让gh与MinTTY合作：

-   重新安装Git for Windows，选中“启用对伪控制台的实验支持”。

-   使用不同的终端仿真器和Git for Windows，如Windows终端。您可以从任何终端仿真器运行“C:\\Program Files\\Git\\bin\\bash.exe”，在没有MinTTY的情况下继续使用Git For Windows中的所有工具。

-   使用winpty作为gh调用的前缀，例如：“winpty gh auth login”。注意：这可能会导致一些UI错误。

### See also

-   [gh](./gh)
