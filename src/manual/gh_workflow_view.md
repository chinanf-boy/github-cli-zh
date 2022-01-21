

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
	<dd>浏览器打开</dd>

	<dt><code>-y</code>, <code>--yaml</code></dt>
	<dd>查看工作流的 yaml 文件</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
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
