## gh alias set

```
gh alias set <alias> <expansion> [flags]
```

定义一个在调用时，将扩展为完整 gh 命令的单词。

扩展可以指定其他参数和标志。如果扩展包含位置占位符，如“$1”，则会适当插入别名后面的额外参数。否则，额外的参数将附加到展开的命令中。

使用 `-` 作为扩展参数，从 standard input 读取扩展字符串。这有助于在定义扩展时，避免引用问题。

如果扩展以 `!` 开头或者，如果给定 `-shell`，则扩展是一个 shell 表达式，调用别名时，将通过“sh”解释器执行。这允许通过 **管道** 和 **重定向链接** 多个命令。

### Options

<dl class="flags">
	<dt><code>-s</code>, <code>--shell</code></dt>
	<dd>定义个 alias 传递给 shell 解释器，r</dd>
</dl>

### Examples

```bash
# note: Command Prompt on Windows 要双引号

$ gh alias set pv 'pr view'
$ gh pv -w 123  #=> gh pr view -w 123

$ gh alias set bugs 'issue list --label=bugs'
$ gh bugs

$ gh alias set homework 'issue list --assignee @me'
$ gh homework

$ gh alias set epicsBy 'issue list --author="$1" --label="epic"'
$ gh epicsBy vilmibm  #=> gh issue list --author="vilmibm" --label="epic"

$ gh alias set --shell igrep 'gh issue list --label="$1" | grep "$2"'
$ gh igrep epic foo  #=> gh issue list --label="epic" | grep "foo"
```

### See also

- [gh alias](./gh_alias.zh.md)
