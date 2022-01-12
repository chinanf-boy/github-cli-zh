## gh formatting

一些gh命令支持将数据导出为JSON，以替代通常的基于行的纯文本输出。这适用于将结构化数据传递给脚本。JSON输出是通过`--json`选项，后跟要获取的字段列表。使用不带值的标志来获取可用字段的列表。

这个`--jq`选项接受jq语法的查询，并且只打印与查询匹配的结果值。这相当于将输出管道化到`jq -r`，但不要求在系统上安装jq实用程序。要了解有关查询语法的详细信息，请参阅：<https://stedolan.github.io/jq/manual/v1.6/>

具有`--template`，使用JSON数据作为输入呈现提供的Go模板。有关Go模板的语法，请参见：<https://golang.org/pkg/text/template/>

模板中提供以下功能：

-   `autocolor`例如`color`，但仅向端子发射颜色
-   `color <style> <input>`：使用<https://github.com/mgutz/ansi>
-   `join <sep> <list>`：使用分隔符连接列表中的值
-   `pluck <field> <list>`：从输入中的所有项收集字段值
-   `tablerow <fields>...`：将输出中的字段作为表格垂直对齐
-   `tablerender`：就地呈现由tablerow添加的字段
-   `timeago <time>`：呈现相对于现在的时间戳
-   `timefmt <format> <time>`：使用Go的时间格式化时间戳。格式函数
-   `truncate <length> <input>`：确保输入符合长度

### Examples

{%highlight bash%}{%raw%}

# format issues as table

$gh问题列表--json编号，标题--模板\\'{range.}{{tablerow（printf“#%v”.number | autocolor“green”）.title}{{end}'

# format a pull request using multiple tables with headers

$gh pr view 3519--json编号、标题、正文、评论、受让人--模板\\'{{printf“#%v”.number}{{.title}

{{.body}

{{tablerow“受让人”“名称”}{{range.assignees}{{tablerow.login.NAME}{{end}}{{tablerender}{{{tablerow“审阅者”“状态”“注释”}{{range.reviews}{{tablerow.author.login.STATE.body}{{end}{end}{end}{endraw%}{%endhighlight

### See also

-   [gh](./gh)
