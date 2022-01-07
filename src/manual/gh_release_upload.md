---
layout: manual
permalink: /:path/:basename
---

## gh release upload

```
gh release upload <tag> <files>... [flags]
```

Upload asset files to a GitHub Release.

To define a display label for an asset, append text starting with '#' after the
file name.


### Options


<dl class="flags">
	<dt><code>--clobber</code></dt>
	<dd>Overwrite existing assets of the same name</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### See also

* [gh release](./gh_release)