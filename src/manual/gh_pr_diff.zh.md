## gh pr diff

```
gh pr diff [<number> | <url> | <branch>] [flags]
```

查看拉取请求中的更改。

在没有参数的情况下，将选择属于当前分支的请求。

### Options

<dl class="flags">
	<dt><code>--color &lt;string&gt;</code></dt>
	<dd>在 diff 输出中，使用颜色: {always|never|auto}</dd>

<dt><code>--patch</code></dt>
<dd>以 patch 格式，展示 diff </dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### See also

- [gh pr](./gh_pr.zh.md)
