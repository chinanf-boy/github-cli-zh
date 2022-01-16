## gh formatting

一些 gh 命令支持将数据导出为 JSON，以替代通常的基于行的纯文本输出。这适用于将结构化数据传递给脚本。JSON 输出是通过`--json`选项，后跟要获取的字段列表。使用不带值的标志来获取可用字段的列表。

这个`--jq`选项接受 jq 语法的 查询，并且只打印与查询匹配的结果值。这相当于，将输出管道化到`jq -r`，但不要求在系统上安装 jq 实用程序。要了解有关查询语法的详细信息，请参阅：<https://stedolan.github.io/jq/manual/v1.6/>

而`--template`，作为 Go 模板，自然是程序 JSON 数据。有关 Go 模板的语法，请参见：<https://golang.org/pkg/text/template/>

模板中，提供以下功能：

- `autocolor`：例如`color`，但仅向终端发射颜色
- `color <style> <input>`：使用<https://github.com/mgutz/ansi>，对输入进行颜色化
- `join <sep> <list>`：使用分隔符，连接列表中的值
- `pluck <field> <list>`：从输入中的所有项，收集字段值
- `tablerow <fields>...`：将输出中的字段，作为表格垂直对齐
- `tablerender`：就地呈现由 tablerow 添加的字段
- `timeago <time>`：呈现相对于现在的时间戳
- `timefmt <format> <time>`：使用 Go `Time.Format`函数，格式化时间戳
- `truncate <length> <input>`：确保输入，符合长度

### Examples

```js
$ gh issue list --json number,title --template \
  '{{range .}}{{tablerow (printf "#%v" .number | autocolor "green") .title}}{{end}}'

# format a pull request using multiple tables with headers
$ gh pr view 3519 --json number,title,body,reviews,assignees --template \
  '{{printf "#%v" .number}} {{.title}}

  {{.body}}

  {{tablerow "ASSIGNEE" "NAME"}}{{range .assignees}}{{tablerow .login .name}}{{end}}{{tablerender}}
  {{tablerow "REVIEWER" "STATE" "COMMENT"}}{{range .reviews}}{{tablerow .author.login .state .body}}{{end}}
  '
```

### See also

- [gh](./gh)
