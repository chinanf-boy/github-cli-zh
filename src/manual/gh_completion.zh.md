## gh completion

```
gh completion -s <shell>
```

为 GitHub CLI 命令生成， shell 补全脚本。

通过包管理器安装 GitHub CLI 时，可能不需要额外的 shell 配置，获得补全支持。若是 Homebrew，请参阅<https://docs.brew.sh/Shell-Completion>

如果需要手动设置补全，请按照以下说明操作。具体的配置文件位置可能因您的系统而异。在测试补全是否正常工作之前，请确保重启 shell。

### bash

首先，确保您使用包管理器，安装了`bash-completion`。

之后，将此添加到您的`~/.bash_profile`:

```
eval "$(gh completion -s bash)"
```

### zsh

产生`_gh` 补全脚本，并将其放在您的`$fpath`:

```
gh completion -s zsh > /usr/local/share/zsh/site-functions/_gh
```

确保您的文档`~/.zshrc`中存在以下内容:

```
autoload -U compinit
compinit -i
```

建议使用 Zsh 版本 5.7 或更高版本。

### fish

产生`gh.fish` 补全脚本：

```
gh completion -s fish > ~/.config/fish/completions/gh.fish
```

### PowerShell

使用以下命令，打开您的配置文件脚本：

```
mkdir -Path (Split-Path -Parent $profile) -ErrorAction SilentlyContinue
notepad $profile
```

添加代码行，并保存文件：

```
Invoke-Expression -Command $(gh completion -s powershell | Out-String)
```

### Options

<dl class="flags">
	<dt><code>-s</code>, <code>--shell &lt;string&gt;</code></dt>
	<dd>Shell type: {bash|zsh|fish|powershell}</dd>
</dl>

### See also

- [gh](./gh.zh.md)
