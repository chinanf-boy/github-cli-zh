

## gh repo view

```
gh repo view [<repository>] [flags]
```

Display the description and the README of a GitHub repository.

With no argument, the repository for the current directory is displayed.

With '--web', open the repository in a web browser instead.

With '--branch', 显示特定分支.

### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>显示特定分支</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>jq 表达式，过滤 JSON 输出</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>JSON 输出特殊字段</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>模板化输出</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>浏览器打开</dd>
</dl>


### See also

* [gh repo](./gh_repo)
