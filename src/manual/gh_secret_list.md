---
layout: manual
permalink: /:path/:basename
---

## gh secret list

```
gh secret list [flags]
```

List secrets on one of the following levels:
- repository (default): available to Actions runs in a repository
- environment: available to Actions runs for a deployment environment in a repository
- organization: available to Actions runs within an organization
- user: available to Codespaces for your user


### Options


<dl class="flags">
	<dt><code>-e</code>, <code>--env &lt;string&gt;</code></dt>
	<dd>List secrets for an environment</dd>

	<dt><code>-o</code>, <code>--org &lt;string&gt;</code></dt>
	<dd>List secrets for an organization</dd>

	<dt><code>-u</code>, <code>--user</code></dt>
	<dd>List a secret for your user</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### See also

* [gh secret](./gh_secret)
