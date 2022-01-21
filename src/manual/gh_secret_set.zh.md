## gh secret set

```
gh secret set <secret-name> [flags]
```

在以下级别之一设置机密的值：

- repository（默认）：可用于 存储库
- environment：部署环境的操作
- organization：组织内
- user：代码空间

组织和用户机密可以选择性地限制，仅对特定存储库可用。

机密的值在发送到 GitHub 之前，在本地进行加密。

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

```bash
# 交互式，复制机密到当前存储库
$ gh secret set MYSECRET

# 读取一个环境变量的机密
$ gh secret set MYSECRET --body "$ENV_VALUE"

# 读取一个文件的机密
$ gh secret set MYSECRET < myfile.txt

# 设置发布环境的机密 
$ gh secret set MYSECRET --env myenvironment

# 设置 组织级别的机密，在公开与私有的存储库中，都可以看到
$ gh secret set MYSECRET --org myOrg --visibility all

# 设置 组织级别的机密，特定存储库可以看到
$ gh secret set MYSECRET --org myOrg --repos repo1,repo2,repo3

# 设置 用户级别的机密，到代码空间
$ gh secret set MYSECRET --user

# 用 ".env" 文件，设置多个机密
$ gh secret set -f .env
```

### See also

- [gh secret](./gh_secret.zh.md)
