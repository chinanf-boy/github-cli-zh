## gh secret list

```
gh secret list [flags]
```

列出机密，有下面这几个级别：

- repository（默认）：可用于 存储库
- environment：部署环境的操作
- organization：组织内
- user：代码空间

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

- [gh secret](./gh_secret.zh.md)
