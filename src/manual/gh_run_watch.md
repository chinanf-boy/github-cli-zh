---
layout: manual
permalink: /:path/:basename
---

## gh run watch

Watch a run until it completes, showing its progress

```
gh run watch <run-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>--exit-status</code></dt>
	<dd>Exit with non-zero status if run fails</dd>

	<dt><code>-i</code>, <code>--interval &lt;int&gt;</code></dt>
	<dd>Refresh interval in seconds</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# Watch a run until it's done
gh run watch

# Run some other command when the run is finished
gh run watch && notify-send "run is done!"
{% endraw %}{% endhighlight %}

### See also

* [gh run](./gh_run)
