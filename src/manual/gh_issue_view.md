

## gh issue view

```
gh issue view {<number> | <url>} [flags]
```

Display the title, body, and other information about an issue.

With '--web', open the issue in a web browser instead.


### Options


<dl class="flags">
	<dt><code>-c</code>, <code>--comments</code></dt>
	<dd>View issue comments</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>jq 表达式，过滤 JSON 输出</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>JSON 输出特殊字段</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>模板化输出</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open an issue in the browser</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### See also

* [gh issue](./gh_issue)
