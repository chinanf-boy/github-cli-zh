

## gh repo sync

```
gh repo sync [<destination-repository>] [flags]
```

Sync destination repository from 源存储库. Syncing uses the main branch
of the 源存储库 to update the matching branch on the destination
repository so they are equal. A fast forward update will be used execept when the
`--force` flag is specified, then the two branches will
by synced using a hard reset.

Without an argument, the local repository is selected as the destination repository.

The 源存储库 is the parent of the destination repository by default.
This can be overridden with the `--source` flag.


### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>同步的分支 (default: main branch)</dd>

	<dt><code>--force</code></dt>
	<dd>强制同步</dd>

	<dt><code>-s</code>, <code>--source &lt;string&gt;</code></dt>
	<dd>源存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# Sync local repository from remote parent
$ gh repo sync

# Sync local repository from remote parent on specific branch
$ gh repo sync --branch v1

# Sync remote fork from its parent
$ gh repo sync owner/cli-fork

# Sync remote repository from another remote repository
$ gh repo sync owner/repo --source owner2/repo2
{% endraw %}{% endhighlight %}

### See also

* [gh repo](./gh_repo)
