---
layout: manual
permalink: /:path/:basename
---

## gh auth logout

```
gh auth logout [flags]
```

删除GitHub主机的身份验证。

此命令删除以交互方式或通过--hostname指定的主机的身份验证配置。

### Options

<dl class="flags">
	<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
	<dd>The hostname of the GitHub instance to log out of</dd>
</dl>

### Examples

{%highlight bash%}{%raw%}$gh auth注销

# => select what host to log out of via a prompt

$gh auth logout--企业主机名。内部的

# => log out of specified host

{%endraw%}{%endhighlight%}

### See also

-   [gh auth](./gh_auth)
