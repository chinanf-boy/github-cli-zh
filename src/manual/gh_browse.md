---
layout: manual
permalink: /:path/:basename
---

## gh browse

```
gh browse [<number> | <path>] [flags]
```

Open the GitHub repository in the web browser.

### Options


<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>Select another branch by passing in the branch name</dd>

	<dt><code>-c</code>, <code>--commit</code></dt>
	<dd>Open the last commit</dd>

	<dt><code>-n</code>, <code>--no-browser</code></dt>
	<dd>Print destination URL instead of opening the browser</dd>

	<dt><code>-p</code>, <code>--projects</code></dt>
	<dd>Open repository projects</dd>

	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>

	<dt><code>-s</code>, <code>--settings</code></dt>
	<dd>Open repository settings</dd>

	<dt><code>-w</code>, <code>--wiki</code></dt>
	<dd>Open repository wiki</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh browse
#=> Open the home page of the current repository

$ gh browse 217
#=> Open issue or pull request 217

$ gh browse --settings
#=> Open repository settings

$ gh browse main.go:312
#=> Open main.go at line 312

$ gh browse main.go --branch main
#=> Open main.go in the main branch
{% endraw %}{% endhighlight %}

### See also

* [gh](./gh)
