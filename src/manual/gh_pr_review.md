---
layout: manual
permalink: /:path/:basename
---

## gh pr review

```
gh pr review [<number> | <url> | <branch>] [flags]
```

Add a review to a pull request.

Without an argument, the pull request that belongs to the current branch is reviewed.


### Options


<dl class="flags">
	<dt><code>-a</code>, <code>--approve</code></dt>
	<dd>Approve pull request</dd>

	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>Specify the body of a review</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-c</code>, <code>--comment</code></dt>
	<dd>Comment on a pull request</dd>

	<dt><code>-r</code>, <code>--request-changes</code></dt>
	<dd>Request changes on a pull request</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
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
