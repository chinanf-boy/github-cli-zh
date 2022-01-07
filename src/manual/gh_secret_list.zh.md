---
layout: manual
permalink: /:path/:basename
---

## gh secret list

```
gh secret list [flags]
```

列出以下级别之一的机密：

-   存储库（默认）：可用于存储库中运行的操作
-   环境：可用于存储库中部署环境的操作运行
-   组织：可用于组织内运行的操作
-   用户：可用于您的用户的代码空间

### Options

<dl class="flags">
	<dt><code>-e</code>, <code>--env &lt;string&gt;</code></dt>
	<dd>List secrets for an environment</dd>

```
<dt><code>-o</code>, <code>--org &lt;string&gt;</code></dt>
<dd>List secrets for an organization</dd>

<dt><code>-u</code>, <code>--user</code></dt>
<dd>List a secret for your user</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### See also

-   [gh secret](./gh_secret)
