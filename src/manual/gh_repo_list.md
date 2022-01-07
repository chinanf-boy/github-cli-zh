---
layout: manual
permalink: /:path/:basename
---

## gh repo list

List repositories owned by user or organization

```
gh repo list [<owner>] [flags]
```

### Options


<dl class="flags">
	<dt><code>--archived</code></dt>
	<dd>Show only archived repositories</dd>

	<dt><code>--fork</code></dt>
	<dd>Show only forks</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-l</code>, <code>--language &lt;string&gt;</code></dt>
	<dd>Filter by primary coding language</dd>

	<dt><code>-L</code>, <code>--limit &lt;int&gt;</code></dt>
	<dd>Maximum number of repositories to list</dd>

	<dt><code>--no-archived</code></dt>
	<dd>Omit archived repositories</dd>

	<dt><code>--private</code></dt>
	<dd>Show only private repositories</dd>

	<dt><code>--public</code></dt>
	<dd>Show only public repositories</dd>

	<dt><code>--source</code></dt>
	<dd>Show only non-forks</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template</dd>

	<dt><code>--topic &lt;string&gt;</code></dt>
	<dd>Filter by topic</dd>
</dl>


### See also

* [gh repo](./gh_repo)
