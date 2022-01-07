---
layout: manual
permalink: /:path/:basename
---

## gh issue comment

Create a new issue comment

```
gh issue comment {<number> | <url>} [flags]
```

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
$ gh issue comment 22 --body "I was able to reproduce this issue, lets fix it."
{% endraw %}{% endhighlight %}

### See also

* [gh issue](./gh_issue)
