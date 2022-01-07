---
layout: manual
permalink: /:path/:basename
---

## gh pr checks

```
gh pr checks [<number> | <url> | <branch>] [flags]
```

显示单个拉动请求的CI状态。

在没有参数的情况下，将选择属于当前分支的请求。

### Options

<dl class="flags">
	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open the web browser to show details about checks</dd>
</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### See also

-   [gh pr](./gh_pr)
