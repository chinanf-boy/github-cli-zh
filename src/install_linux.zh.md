# Installing gh on Linux and BSD

从下载的软件包<https://cli.github.com>或来自<https://github.com/cli/cli/releases>被认为是官方二进制文件。我们关注流行的Linux发行版和以下CPU体系结构：`i386`, `amd64`, `arm64`, `armhf`.

其他安装源由社区维护，因此可能落后于我们的发布计划。

## Official sources

### Debian, Ubuntu Linux, Raspberry Pi OS (apt)

安装：

```bash
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```

升级：

```bash
sudo apt update
sudo apt install gh
```

### Fedora, CentOS, Red Hat Enterprise Linux (dnf)

安装：

```bash
sudo dnf config-manager --add-repo https://cli.github.com/packages/rpm/gh-cli.repo
sudo dnf install gh
```

升级：

```bash
sudo dnf update gh
```

### openSUSE/SUSE Linux (zypper)

安装：

```bash
sudo zypper addrepo https://cli.github.com/packages/rpm/gh-cli.repo
sudo zypper ref
sudo zypper install gh
```

升级：

```bash
sudo zypper ref
sudo zypper update gh
```

## Manual installation

-   [Download release binaries][releases page]与你的平台相匹配；或
-   [Build from source](./source.md).

## Unofficial, community-supported methods

GitHub CLI团队不维护以下软件包或存储库，因此我们无法提供对这些安装方法的支持。

### Snap (do not use)

有[so many issues with Snap](https://github.com/casperdcl/cli/issues/7)作为我们团队建议的GitHub CLI等应用程序的运行时机制*永远不要安装gh作为一个单元*.

### Arch Linux

Arch Linux用户可以从[community repo][arch linux repo]:

```bash
sudo pacman -S github-cli
```

或者，使用[unofficial AUR package][arch linux aur]从源代码构建GitHub CLI。

### Android

Android 7+用户可以通过[Termux](https://wiki.termux.com/wiki/Main_Page):

```bash
pkg install gh
```

### FreeBSD

FreeBSD用户可以从[ports collection](https://www.freshports.org/devel/gh/):

```bash
cd /usr/ports/devel/gh/ && make install clean
```

或通过[pkg(8)](https://www.freebsd.org/cgi/man.cgi?pkg(8)):

```bash
pkg install gh
```

### NetBSD/pkgsrc

NetBSD用户和网络上的用户[platforms supported by pkgsrc](https://pkgsrc.org/#index4h1)可以安装[gh package](https://pkgsrc.se/net/gh):

```bash
pkgin install gh
```

要从源代码安装，请执行以下操作：

```bash
cd /usr/pkgsrc/net/gh && make package-install
```

### OpenBSD

在最新版本或从7.0开始的版本中，OpenBSD用户可以从以下软件包安装：

```
pkg_add github-cli
```

### Funtoo

Funtoo Linux有一个自动生成的github cli包，位于[dev-kit](https://github.com/funtoo/dev-kit/tree/1.4-release/dev-util/github-cli)，可通过以下方式安装：

```bash
emerge -av github-cli
```

可通过同步回购协议，然后请求升级来完成升级：

```bash
ego sync
emerge -u github-cli
```

### Gentoo

Gentoo Linux用户可以从[main portage tree](https://packages.gentoo.org/packages/dev-util/github-cli):

```bash
emerge -av github-cli
```

升级可以通过更新portage树，然后请求升级来完成：

```bash
emerge --sync
emerge -u github-cli
```

### Kiss Linux

Kiss Linux用户可以从[community repos](https://github.com/kisslinux/community):

```bash
kiss b github-cli && kiss i github-cli
```

### Nix/NixOS

Nix/NixOS用户可以从[nixpkgs](https://search.nixos.org/packages?show=gitAndTools.gh&query=gh&from=0&size=30&sort=relevance&channel=20.03#disabled):

```bash
nix-env -iA nixos.gitAndTools.gh
```

### openSUSE Tumbleweed

openSUSE Tumbleweed用户可以从[official distribution repo](https://software.opensuse.org/package/gh):

```bash
sudo zypper in gh
```

[releases page]: https://github.com/cli/cli/releases/latest

[arch linux repo]: https://www.archlinux.org/packages/community/x86_64/github-cli

[arch linux aur]: https://aur.archlinux.org/packages/github-cli-git
