

## gh repo list

List repositories owned by user or organization

```
gh repo list [<owner>] [flags]
```

### Options


<dl class="flags">
	<dt><code>--archived</code></dt>
	<dd>仅展示存档的存储库</dd>

	<dt><code>--fork</code></dt>
	<dd>仅展示副本存储库</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>jq 表达式，过滤 JSON 输出</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>JSON 输出特殊字段</dd>

	<dt><code>-l</code>, <code>--language &lt;string&gt;</code></dt>
	<dd>主编程语言的过滤</dd>

	<dt><code>-L</code>, <code>--limit &lt;int&gt;</code></dt>
	<dd>Maximum number of repositories to list</dd>

	<dt><code>--no-archived</code></dt>
	<dd>不要存档的存储库</dd>

	<dt><code>--private</code></dt>
	<dd>仅展示私有存储库</dd>

	<dt><code>--public</code></dt>
	<dd>仅展示公开的存储库</dd>

	<dt><code>--source</code></dt>
	<dd>仅展示非副本的存储库</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>模板化输出</dd>

	<dt><code>--topic &lt;string&gt;</code></dt>
	<dd>标题主题的过滤</dd>
</dl>


### See also

* [gh repo](./gh_repo)
