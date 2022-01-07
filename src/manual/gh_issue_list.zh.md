

## gh issue list

列出并筛选此存储库中的问题

```
gh issue list [flags]
```

### Options

<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;string&gt;</code></dt>
	<dd>Filter by assignee</dd>

<dt><code>-A</code>, <code>--author &lt;string&gt;</code></dt>
<dd>Filter by author</dd>

<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
<dd>jq 表达式，过滤 JSON 输出</dd>

<dt><code>--json &lt;fields&gt;</code></dt>
<dd>JSON 输出特殊字段</dd>

<dt><code>-l</code>, <code>--label &lt;strings&gt;</code></dt>
<dd>Filter by labels</dd>

<dt><code>-L</code>, <code>--limit &lt;int&gt;</code></dt>
<dd>Maximum number of issues to fetch</dd>

<dt><code>--mention &lt;string&gt;</code></dt>
<dd>Filter by mention</dd>

<dt><code>-m</code>, <code>--milestone &lt;number&gt;</code></dt>
<dd>Filter by milestone number or `title`</dd>

<dt><code>-S</code>, <code>--search &lt;query&gt;</code></dt>
<dd>Search issues with query</dd>

<dt><code>-s</code>, <code>--state &lt;string&gt;</code></dt>
<dd>Filter by state: {open|closed|all}</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>模板化输出</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open the browser to list the issue(s)</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash
$gh问题列表-l“bug”-l“需要帮助”$gh问题列表-蒙娜丽莎$gh问题列表-A“@me”$gh问题列表-web$gh问题列表-里程碑“大1.0”$gh问题列表-搜索”错误号：受让人排序：已创建asc“
```
”

### See also

-   [gh issue](./gh_issue)
