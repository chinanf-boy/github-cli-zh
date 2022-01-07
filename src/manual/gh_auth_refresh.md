---
layout: manual
permalink: /:path/:basename
---

## gh auth refresh

```
gh auth refresh [flags]
```

Expand or fix the permission scopes for stored credentials

The --scopes flag accepts a comma separated list of scopes you want your gh credentials to have. If
absent, this command ensures that gh has access to a minimum set of scopes.


### Options


<dl class="flags">
	<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
	<dd>The GitHub host to use for authentication</dd>

	<dt><code>-s</code>, <code>--scopes &lt;strings&gt;</code></dt>
	<dd>Additional authentication scopes for gh to have</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh auth refresh --scopes write:org,read:public_key
# => open a browser to add write:org and read:public_key scopes for use with gh api

$ gh auth refresh
# => open a browser to ensure your authentication credentials have the correct minimum scopes
{% endraw %}{% endhighlight %}

### See also

* [gh auth](./gh_auth)
