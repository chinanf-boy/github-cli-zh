

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
	<dd>环境的机密</dd>

	<dt><code>-o</code>, <code>--org &lt;string&gt;</code></dt>
	<dd>组织的机密</dd>

	<dt><code>-u</code>, <code>--user</code></dt>
	<dd>用户的机密</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### See also

* [gh secret](./gh_secret)
