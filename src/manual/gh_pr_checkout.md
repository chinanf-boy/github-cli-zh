

## gh pr checkout

Check out a pull request in git

```
gh pr checkout {<number> | <url> | <branch>} [flags]
```

### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>Local branch name to use (default: the name of the head branch)</dd>

	<dt><code>--detach</code></dt>
	<dd>Checkout PR with a detached HEAD</dd>

	<dt><code>-f</code>, <code>--force</code></dt>
	<dd>Reset the existing local branch to the latest state of the pull request</dd>

	<dt><code>--recurse-submodules</code></dt>
	<dd>Update all submodules after checkout</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### See also

* [gh pr](./gh_pr)
