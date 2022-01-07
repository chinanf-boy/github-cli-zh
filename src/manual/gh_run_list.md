---
layout: manual
permalink: /:path/:basename
---

## gh run list

List recent workflow runs

```
gh run list [flags]
```

### Options


<dl class="flags">
	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-L</code>, <code>--limit &lt;int&gt;</code></dt>
	<dd>Maximum number of runs to fetch</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template</dd>

	<dt><code>-w</code>, <code>--workflow &lt;string&gt;</code></dt>
	<dd>Filter runs by workflow</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### See also

* [gh run](./gh_run)
