

## gh pr review

```
gh pr review [<number> | <url> | <branch>] [flags]
```

Add a review to a pull request.

Without an argument, the pull request that belongs to the current branch is reviewed.


### Options


<dl class="flags">
	<dt><code>-a</code>, <code>--approve</code></dt>
	<dd>批准 pull request</dd>

	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>指定一个审查的主体内容</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>读取文件，输入主体内容 (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-c</code>, <code>--comment</code></dt>
	<dd>给出评论</dd>

	<dt><code>-r</code>, <code>--request-changes</code></dt>
	<dd>要求 PR 修改</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# approve the pull request of the current branch
$ gh pr review --approve

# leave a review comment for the current branch
$ gh pr review --comment -b "interesting"

# add a review for a specific pull request
$ gh pr review 123

# request changes on a specific pull request
$ gh pr review 123 -r -b "needs more ASCII art"
{% endraw %}{% endhighlight %}

### See also

* [gh pr](./gh_pr)
