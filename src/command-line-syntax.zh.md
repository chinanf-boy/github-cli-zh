# 我们是如何对命令行语法进行文档化的

## 字面文字

对命令中无法更改的部分，使用纯文本。

*例子：*
`gh help`此命令中需要参数帮助。

## 替换值

使用尖括号表示用户必须替换的值。尖括号内，不能包含其他表达式。

*例子：*
- `gh pr view <issue-number>`

将`<issue-number>`替换成发行号。

## 可选参数

将可选参数放在方括号中。如果用竖条分隔，可选的互斥参数。

*例子：*

- `gh pr checkout [--web]`

参数`--web`是可选的。

- `gh pr view [<number> | <url>]`

这个`<number>`和`<url>`参数是可选的。

## 所需的互斥参数

将所需的互斥参数放在大括号内，用竖条分隔参数。

*例子：*
- `gh pr {view | create}`

## 重复性的参数

省略号表示可以多次出现的参数。

*例子：*
- `gh pr close <pr-number>...`

## Variable naming

对于多字变量，使用破折号（所有小写字母，都用破折号分隔）

*例子：*
- `gh pr checkout <issue-number>`

## 其他示例

*带占位符的可选参数：*
- `command sub-command [<arg>]`

*具有互斥选项的必需参数：*
- `command sub-command {<path> | <string> | literal}`

*具有互斥选项的可选参数：*
- `command sub-command [<path> | <string>]`
