

## gh issue list

List and filter issues in this repository

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
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh issue list -l "bug" -l "help wanted"
$ gh issue list -A monalisa
$ gh issue list -a "@me"
$ gh issue list --web
$ gh issue list --milestone "The big 1.0"
$ gh issue list --search "error no:assignee sort:created-asc"
{% endraw %}{% endhighlight %}

### See also

* [gh issue](./gh_issue)
