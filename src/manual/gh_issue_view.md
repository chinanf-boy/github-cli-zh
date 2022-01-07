---
layout: manual
permalink: /:path/:basename
---

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
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open an issue in the browser</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### See also

* [gh issue](./gh_issue)
