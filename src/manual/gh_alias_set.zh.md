---
layout: manual
permalink: /:path/:basename
---

## gh alias set

```
gh alias set <alias> <expansion> [flags]
```

定义一个在调用时将扩展为完整gh命令的单词。

扩展可以指定其他参数和标志。如果扩展包含位置占位符，如“$1”，则会适当插入别名后面的额外参数。否则，额外的参数将附加到展开的命令中。

使用“-”作为扩展参数从标准输入读取扩展字符串。这有助于在定义扩展时避免引用问题。

如果扩展以“！”开头或者，如果给定“-shell”，则扩展是一个shell表达式，调用别名时将通过“sh”解释器对其求值。这允许通过管道和重定向链接多个命令。

### Options

<dl class="flags">
	<dt><code>-s</code>, <code>--shell</code></dt>
	<dd>Declare an alias to be passed through a shell interpreter</dd>
</dl>

### Examples

{%highlight bash%}{%raw%}

# note: Command Prompt on Windows requires using double quotes for arguments

$gh别名集pv“pr视图”$gh pv-w 123#=>gh pr视图-w 123

$gh alias set bugs'问题列表--label=bugs'$gh bugs

$gh别名设置家庭作业'问题列表--受让人@me'$gh家庭作业

$gh alias set-epicsBy'问题列表--author=“$1”--label=“epic”'$gh-epicsBy-vilmibm#=>gh问题列表--author=“vilmibm”--label=“epic”

$gh别名集--shell igrep'gh问题列表--label=“$1”| grep“$2”$gh igrep epic foo#=>gh问题列表--label=“epic”| grep“foo”{%endraw%}{%endhighlight%}

### See also

-   [gh alias](./gh_alias)
