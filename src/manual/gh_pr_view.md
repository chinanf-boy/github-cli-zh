---
layout: manual
permalink: /:path/:basename
---

## gh pr view

```
gh pr view [<number> | <url> | <branch>] [flags]
```

Display the title, body, and other information about a pull request.

Without an argument, the pull request that belongs to the current branch
is displayed.

With '--web', open the pull request in a web browser instead.


### Options


<dl class="flags">
	<dt><code>-c</code>, <code>--comments</code></dt>
	<dd>View pull request comments</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open a pull request in the browser</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### See also

* [gh pr](./gh_pr)
