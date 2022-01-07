

## gh config set

Update configuration with a value for the given key

```
gh config set <key> <value> [flags]
```

### Options


<dl class="flags">
	<dt><code>-h</code>, <code>--host &lt;string&gt;</code></dt>
	<dd>Set per-host setting</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh config set editor vim
$ gh config set editor "code --wait"
$ gh config set git_protocol ssh --host github.com
$ gh config set prompt disabled
{% endraw %}{% endhighlight %}

### See also

* [gh config](./gh_config)
