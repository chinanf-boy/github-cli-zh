---
layout: manual
permalink: /:path/:basename
---

## gh config get

打印给定配置密钥的值

```
gh config get <key> [flags]
```

### Options

<dl class="flags">
	<dt><code>-h</code>, <code>--host &lt;string&gt;</code></dt>
	<dd>Get per-host setting</dd>
</dl>

### Examples

{%highlight bash%}{%raw%}$gh config get git_protocol https{%endraw%}{%endhighlight%}

### See also

-   [gh config](./gh_config)
