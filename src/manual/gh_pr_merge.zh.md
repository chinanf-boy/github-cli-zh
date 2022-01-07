

## gh pr merge

```
gh pr merge [<number> | <url> | <branch>] [flags]
```

在GitHub上合并拉取请求。

在没有参数的情况下，将选择属于当前分支的请求。

### Options

<dl class="flags">
	<dt><code>--admin</code></dt>
	<dd>Use administrator privileges to merge a pull request that does not meet requirements</dd>

<dt><code>--auto</code></dt>
<dd>Automatically merge only after necessary requirements are met</dd>

<dt><code>-b</code>, <code>--body &lt;text&gt;</code></dt>
<dd>Body text for the merge commit</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

<dt><code>-d</code>, <code>--delete-branch</code></dt>
<dd>Delete the local and remote branch after merge</dd>

<dt><code>--disable-auto</code></dt>
<dd>Disable auto-merge for this pull request</dd>

<dt><code>-m</code>, <code>--merge</code></dt>
<dd>Merge the commits with the base branch</dd>

<dt><code>-r</code>, <code>--rebase</code></dt>
<dd>Rebase the commits onto the base branch</dd>

<dt><code>-s</code>, <code>--squash</code></dt>
<dd>Squash the commits into one commit and merge it into the base branch</dd>

<dt><code>-t</code>, <code>--subject &lt;text&gt;</code></dt>
<dd>Subject text for the merge commit</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### See also

-   [gh pr](./gh_pr)
