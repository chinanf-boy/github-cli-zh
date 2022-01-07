

## gh pr comment

```
gh pr comment [<number> | <url> | <branch>] [flags]
```

Create a new pr comment.

Without an argument, the pull request that belongs to the current branch
is selected.			

With '--web', comment on the pull request in a web browser instead.


### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>Supply a body. Will prompt for one otherwise.</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-e</code>, <code>--editor</code></dt>
	<dd>Add body using editor</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Add body in browser</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh pr comment 22 --body "This looks great, lets get it deployed."
{% endraw %}{% endhighlight %}

### See also

* [gh pr](./gh_pr)
