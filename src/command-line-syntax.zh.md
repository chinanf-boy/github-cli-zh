# How we document our command line syntax

## Literal text

对命令中无法更改的部分使用纯文本。

*例子：*
`gh help`此命令中需要参数帮助。

## Placeholder values

使用尖括号表示用户必须替换的值。尖括号内不能包含其他表达式。

*例子：*
`gh pr view <issue-number>`代替`<issue-number>`有发行号。

## Optional arguments

将可选参数放在方括号中。如果用竖条分隔，则互斥参数可以包含在方括号内。

*例子：*
`gh pr checkout [--web]`争论`--web`是可选的。

`gh pr view [<number> | <url>]`这个`<number>`和`<url>`参数是可选的。

## Required mutually exclusive arguments

将所需的互斥参数放在大括号内，用竖条分隔参数。

*例子：*
`gh pr {view | create}`

## Repeatable arguments

省略号表示可以多次出现的参数。

*例子：*
`gh pr close <pr-number>...`

## Variable naming

对于多字变量，使用破折号大小写（所有小写字母都用破折号分隔）

*例子：*
`gh pr checkout <issue-number>`

## Additional examples

*带占位符的可选参数：*
`command sub-command [<arg>]`

*具有互斥选项的必需参数：*
`command sub-command {<path> | <string> | literal}`

*具有互斥选项的可选参数：*
`command sub-command [<path> | <string>]`
