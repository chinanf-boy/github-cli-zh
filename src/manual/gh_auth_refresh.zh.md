---
layout: manual
permalink: /:path/:basename
---

## gh auth refresh

```
gh auth refresh [flags]
```

扩展或修复存储凭据的权限范围

\--scopes标志接受以逗号分隔的范围列表，这些范围是您希望gh凭据具有的范围。如果不存在，此命令将确保gh可以访问最小范围集。

### Options

<dl class="flags">
	<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
	<dd>The GitHub host to use for authentication</dd>

```
<dt><code>-s</code>, <code>--scopes &lt;strings&gt;</code></dt>
<dd>Additional authentication scopes for gh to have</dd>
```

</dl>

### Examples

{%highlight bash%}{%raw%}$gh auth refresh--scopes write:org，read:public_key

# => open a browser to add write:org and read:public_key scopes for use with gh api

$gh授权刷新

# => open a browser to ensure your authentication credentials have the correct minimum scopes

{%endraw%}{%endhighlight%}

### See also

-   [gh auth](./gh_auth)
