---
layout: manual
permalink: /:path/:basename
---

## gh release view

```
gh release view [<tag>] [flags]
```

View information about a GitHub Release.

Without an explicit tag name argument, the latest release in the project
is shown.


### Options


<dl class="flags">
	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open the release in the browser</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### See also

* [gh release](./gh_release)
