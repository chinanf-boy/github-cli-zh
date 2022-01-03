# Installation from source

1.  验证是否已安装Go 1.16+

    ```sh
    $ go version
    ```

    如果`go`未安装，请按照上的说明操作[the Go website](https://golang.org/doc/install).

2.  克隆此存储库

    ```sh
    $ git clone https://github.com/cli/cli.git gh-cli
    $ cd gh-cli
    ```

3.  构建和安装

    #### Unix-like systems

    ```sh
    # installs to '/usr/local' by default; sudo may be required
    $ make install

    # or, install to a different location
    $ make install prefix=/path/to/gh
    ```

    #### Windows

    ```pwsh
    # build the `bin\gh.exe` binary
    > go run script\build.go
    ```

    Windows上没有可用的安装步骤。

4.  跑`gh version`检查它是否有效。

    #### Windows

    跑`bin\gh version`检查它是否有效。

## Cross-compiling binaries for different platforms

您可以使用安装了Go的任何平台来构建用于其他平台或CPU体系结构的二进制文件。这是通过设置环境变量（如GOOS和GOARCH）实现的。

例如，编译`gh`32位Raspberry Pi操作系统的二进制文件：

```sh
# on a Unix-like system:
$ GOOS=linux GOARCH=arm GOARM=7 CGO_ENABLED=0 make clean bin/gh
```

```pwsh
# on Windows, pass environment variables as arguments to the build script:
> go run script\build.go clean bin\gh GOOS=linux GOARCH=arm GOARM=7 CGO_ENABLED=0
```

跑`go tool dist list`列出所有支持的GOOS/GOARCH值。

提示：要减小生成的二进制文件的大小，可以使用`GO_LDFLAGS="-s -w"`。这将忽略用于调试的符号表。请参阅[supported linker flags](https://golang.org/cmd/link/).
