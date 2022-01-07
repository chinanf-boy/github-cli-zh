---
layout: manual
permalink: /:path/:basename
---

## gh workflow view

View the summary of a workflow

```
gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]
```

### Options


<dl class="flags">
	<dt><code>-r</code>, <code>--ref &lt;string&gt;</code></dt>
	<dd>The branch or tag name which contains the version of the workflow file you&#39;d like to view</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open workflow in the browser</dd>

	<dt><code>-y</code>, <code>--yaml</code></dt>
	<dd>View the workflow yaml file</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# Interactively select a workflow to view
$ gh workflow view

# View a specific workflow
$ gh workflow view 0451
{% endraw %}{% endhighlight %}

### See also

* [gh workflow](./gh_workflow)
