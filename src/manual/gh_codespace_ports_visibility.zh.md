---
layout: manual
permalink: /:path/:basename
---

## gh codespace ports visibility

更改转发端口的可见性

```
gh codespace ports visibility <port>:{public|private|org}...
```

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-c</code>, <code>--codespace &lt;string&gt;</code></dt>
	<dd>Name of the codespace</dd>
</dl>

### Examples

{%highlight bash%}{%raw%}gh代码空间端口可见性80:org 3000:private 8000:public{%endraw%}{%endhighlight%}

### See also

-   [gh codespace ports](./gh_codespace_ports)
