

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
	<dd>读取文件，输入主体内容 (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-e</code>, <code>--editor</code></dt>
	<dd>Add body using editor</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Add body in browser</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh pr comment 22 --body "This looks great, lets get it deployed."
{% endraw %}{% endhighlight %}

### See also

* [gh pr](./gh_pr)
