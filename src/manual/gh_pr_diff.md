

## gh pr diff

```
gh pr diff [<number> | <url> | <branch>] [flags]
```

View changes in a pull request. 

Without an argument, the pull request that belongs to the current branch
is selected.			


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

* [gh pr](./gh_pr)
