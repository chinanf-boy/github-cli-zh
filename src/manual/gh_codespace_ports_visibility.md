

## gh codespace ports visibility

Change the visibility of the forwarded port

```
gh codespace ports visibility <port>:{public|private|org}...
```

### Options inherited from parent commands


<dl class="flags">
	<dt><code>-c</code>, <code>--codespace &lt;string&gt;</code></dt>
	<dd>名字</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
gh codespace ports visibility 80:org 3000:private 8000:public{% endraw %}{% endhighlight %}

### See also

* [gh codespace ports](./gh_codespace_ports)
