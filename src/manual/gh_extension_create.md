

## gh extension create

Create a new extension

```
gh extension create [<name>] [flags]
```

### Options


<dl class="flags">
	<dt><code>--precompiled &lt;string&gt;</code></dt>
	<dd>Create a precompiled extension. Possible values: go, other</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# Use interactively
gh extension create

# Create a script-based extension
gh extension create foobar

# Create a Go extension
gh extension create --precompiled=go foobar

# Create a non-Go precompiled extension
gh extension create --precompiled=other foobar
{% endraw %}{% endhighlight %}

### See also

* [gh extension](./gh_extension)
