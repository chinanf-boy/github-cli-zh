---
layout: manual
permalink: /:path/:basename
---

## gh secret set

```
gh secret set <secret-name> [flags]
```

在以下级别之一设置机密的值：

-   存储库（默认）：可用于存储库中运行的操作
-   环境：可用于存储库中部署环境的操作运行
-   组织：可用于组织内运行的操作
-   用户：可用于您的用户的代码空间

组织和用户机密可以选择性地限制为仅对特定存储库可用。

秘密值在发送到GitHub之前在本地进行加密。

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>The value for the secret (reads from standard input if not specified)</dd>

```
<dt><code>-e</code>, <code>--env &lt;environment&gt;</code></dt>
<dd>Set deployment environment secret</dd>

<dt><code>-f</code>, <code>--env-file &lt;file&gt;</code></dt>
<dd>Load secret names and values from a dotenv-formatted file</dd>

<dt><code>--no-store</code></dt>
<dd>Print the encrypted, base64-encoded value instead of storing it on Github</dd>

<dt><code>-o</code>, <code>--org &lt;organization&gt;</code></dt>
<dd>Set organization secret</dd>

<dt><code>-r</code>, <code>--repos &lt;repositories&gt;</code></dt>
<dd>List of repositories that can access an organization or user secret</dd>

<dt><code>-u</code>, <code>--user</code></dt>
<dd>Set a secret for your user</dd>

<dt><code>-v</code>, <code>--visibility &lt;{all|private|selected}&gt;</code></dt>
<dd>Set visibility for an organization secret: {all|private|selected}</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

{%highlight bash%}{%raw%}

# Paste secret value for the current repository in an interactive prompt

$gh秘密集我的秘密

# Read secret value from an environment variable

$gh秘密集MYSECRET--正文“$ENV\_值”

# Read secret value from a file

$gh秘密集MYSECRET\<myfile。文本

# Set secret for a deployment environment in the current repository

$gh秘密集我的秘密--环境我的环境

# Set organization-level secret visible to both public and private repositories

$gh秘密集MYSECRET--org myOrg--visibility all

# Set organization-level secret visible to specific repositories

$gh秘密集MYSECRET--org myOrg--repos repo1，repo2，repo3

# Set user-level secret for Codespaces

$gh秘密集MYSECRET--用户

# Set multiple secrets imported from the ".env" file

$gh秘密集-f。环境{%endraw%}{%endhighlight%}

### See also

-   [gh secret](./gh_secret)
