

## gh secret set

```
gh secret set <secret-name> [flags]
```

Set a value for a secret on one of the following levels:
- repository (default): available to Actions runs in a repository
- environment: available to Actions runs for a deployment environment in a repository
- organization: available to Actions runs within an organization
- user: available to Codespaces for your user

Organization and user secrets can optionally be restricted to only be available to
specific repositories.

Secret values are locally encrypted before being sent to GitHub.


### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>机密内容 (reads from standard input if not specified)</dd>

	<dt><code>-e</code>, <code>--env &lt;environment&gt;</code></dt>
	<dd>设置发布环境的机密</dd>

	<dt><code>-f</code>, <code>--env-file &lt;file&gt;</code></dt>
	<dd>加载 secret 名与值 (dotenv 格式文件）</dd>

	<dt><code>--no-store</code></dt>
	<dd>打印 encrypted, base64-encoded 值，而不是在 Github 上存储</dd>

	<dt><code>-o</code>, <code>--org &lt;organization&gt;</code></dt>
	<dd>设置组织的机密</dd>

	<dt><code>-r</code>, <code>--repos &lt;repositories&gt;</code></dt>
	<dd>能访问到一个组织或用户机密，列出这样的存储库</dd>

	<dt><code>-u</code>, <code>--user</code></dt>
	<dd>设置用户的机密</dd>

	<dt><code>-v</code>, <code>--visibility &lt;{all|private|selected}&gt;</code></dt>
	<dd>设置一个组织机密的可见性: {all|private|selected}</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# Paste secret value for the current repository in an interactive prompt
$ gh secret set MYSECRET

# Read secret value from an environment variable
$ gh secret set MYSECRET --body "$ENV_VALUE"

# Read secret value from a file
$ gh secret set MYSECRET < myfile.txt

# Set secret for a deployment environment in the current repository
$ gh secret set MYSECRET --env myenvironment

# Set organization-level secret visible to both public and private repositories
$ gh secret set MYSECRET --org myOrg --visibility all

# Set organization-level secret visible to specific repositories
$ gh secret set MYSECRET --org myOrg --repos repo1,repo2,repo3

# Set user-level secret for Codespaces
$ gh secret set MYSECRET --user

# Set multiple secrets imported from the ".env" file
$ gh secret set -f .env
{% endraw %}{% endhighlight %}

### See also

* [gh secret](./gh_secret)
