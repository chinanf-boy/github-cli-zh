---
layout: manual
permalink: /:path/:basename
---

## gh codespace create

创建一个代码空间

```
gh codespace create [flags]
```

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>repository branch</dd>

```
<dt><code>--idle-timeout &lt;duration&gt;</code></dt>
<dd>allowed inactivity before codespace is stopped, e.g. &#34;10m&#34;, &#34;1h&#34;</dd>

<dt><code>-m</code>, <code>--machine &lt;string&gt;</code></dt>
<dd>hardware specifications for the VM</dd>

<dt><code>-r</code>, <code>--repo &lt;string&gt;</code></dt>
<dd>repository name with owner: user/repo</dd>

<dt><code>-s</code>, <code>--status</code></dt>
<dd>show status of post-create command and dotfiles</dd>
```

</dl>

### See also

-   [gh codespace](./gh_codespace)
