

## gh repo sync

```
gh repo sync [<destination-repository>] [flags]
```

Sync destination repository from source repository. Syncing uses the main branch
of the source repository to update the matching branch on the destination
repository so they are equal. A fast forward update will be used execept when the
`--force` flag is specified, then the two branches will
by synced using a hard reset.

Without an argument, the local repository is selected as the destination repository.

The source repository is the parent of the destination repository by default.
This can be overridden with the `--source` flag.


### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>Branch to sync (default: main branch)</dd>

	<dt><code>--force</code></dt>
	<dd>Hard reset the branch of the destination repository to match the source repository</dd>

	<dt><code>-s</code>, <code>--source &lt;string&gt;</code></dt>
	<dd>Source repository</dd>
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
