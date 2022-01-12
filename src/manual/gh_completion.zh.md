## gh completion

```
gh completion -s <shell>
```

为GitHub CLI命令生成shell完成脚本。

通过包管理器安装GitHub CLI时，可能不需要额外的shell配置来获得完成支持。有关自制，请参阅<https://docs.brew.sh/Shell-Completion>

如果需要手动设置完井，请按照以下说明操作。具体的配置文件位置可能因您的系统而异。在测试完成是否正常工作之前，请确保重新启动shell。

### bash

首先，确保您安装了`bash-completion`使用包管理器。

之后，将此添加到您的`~/.bash_profile`:

```
eval "$(gh completion -s bash)"
```

### zsh

产生`_gh`完成脚本并将其放在您的`$fpath`:

```
gh completion -s zsh > /usr/local/share/zsh/site-functions/_gh
```

确保您的文档中存在以下内容：`~/.zshrc`:

```
autoload -U compinit
compinit -i
```

建议使用Zsh版本5.7或更高版本。

### fish

产生`gh.fish`完成脚本：

```
gh completion -s fish > ~/.config/fish/completions/gh.fish
```

### PowerShell

使用以下命令打开您的配置文件脚本：

```
mkdir -Path (Split-Path -Parent $profile) -ErrorAction SilentlyContinue
notepad $profile
```

添加行并保存文件：

```
Invoke-Expression -Command $(gh completion -s powershell | Out-String)
```

### Options

<dl class="flags">
	<dt><code>-s</code>, <code>--shell &lt;string&gt;</code></dt>
	<dd>Shell type: {bash|zsh|fish|powershell}</dd>
</dl>

### See also

-   [gh](./gh)
