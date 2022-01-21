

## gh pr checkout

Check out a pull request in git

```
gh pr checkout {<number> | <url> | <branch>} [flags]
```

### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>本地分支名 (默认: the name of the head branch)</dd>

	<dt><code>--detach</code></dt>
	<dd> 以一种分离 HEAD 的状态，查看 PR</dd>

	<dt><code>-f</code>, <code>--force</code></dt>
	<dd>重设本地分支为最新的PR</dd>

	<dt><code>--recurse-submodules</code></dt>
	<dd>在 checkout 之后，更新所有的 submodules </dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### See also

* [gh pr](./gh_pr)
