

## gh pr list

List and filter pull requests in this repository

```
gh pr list [flags]
```

### Options


<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;string&gt;</code></dt>
	<dd>Filter by assignee</dd>

	<dt><code>-A</code>, <code>--author &lt;string&gt;</code></dt>
	<dd>Filter by author</dd>

	<dt><code>-B</code>, <code>--base &lt;string&gt;</code></dt>
	<dd>Filter by base branch</dd>

	<dt><code>-d</code>, <code>--draft</code></dt>
	<dd>Filter by draft state</dd>

	<dt><code>-H</code>, <code>--head &lt;string&gt;</code></dt>
	<dd>Filter by head branch</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>jq 表达式，过滤 JSON 输出</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>JSON 输出特殊字段</dd>

	<dt><code>-l</code>, <code>--label &lt;strings&gt;</code></dt>
	<dd>Filter by labels</dd>

	<dt><code>-L</code>, <code>--limit &lt;int&gt;</code></dt>
	<dd>Maximum number of items to fetch</dd>

	<dt><code>-S</code>, <code>--search &lt;query&gt;</code></dt>
	<dd>Search pull requests with query</dd>

	<dt><code>-s</code>, <code>--state &lt;string&gt;</code></dt>
	<dd>Filter by state: {open|closed|merged|all}</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>模板化输出</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open the browser to list the pull requests</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
List PRs authored by you
$ gh pr list --author "@me"

List PRs assigned to you
$ gh pr list --assignee "@me"

List PRs by label, combining multiple labels with AND
$ gh pr list --label bug --label "priority 1"

List PRs using search syntax
$ gh pr list --search "status:success review:required"

Open the list of PRs in a web browser
$ gh pr list --web
 	{% endraw %}{% endhighlight %}

### See also

* [gh pr](./gh_pr)
