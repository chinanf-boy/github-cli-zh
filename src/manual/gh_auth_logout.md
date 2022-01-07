---
layout: manual
permalink: /:path/:basename
---

## gh auth logout

```
gh auth logout [flags]
```

Remove authentication for a GitHub host.

This command removes the authentication configuration for a host either specified
interactively or via --hostname.


### Options


<dl class="flags">
	<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
	<dd>The hostname of the GitHub instance to log out of</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh auth logout
# => select what host to log out of via a prompt

$ gh auth logout --hostname enterprise.internal
# => log out of specified host
{% endraw %}{% endhighlight %}

### See also

* [gh auth](./gh_auth)
