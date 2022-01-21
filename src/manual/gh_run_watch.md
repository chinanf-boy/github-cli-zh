

## gh run watch

Watch a run until it completes, showing its progress

```
gh run watch <run-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>--exit-status</code></dt>
	<dd>运行失败，退出代码 非零</dd>

	<dt><code>-i</code>, <code>--interval &lt;int&gt;</code></dt>
	<dd>刷新的时间间隙</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
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
