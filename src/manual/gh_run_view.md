

## gh run view

View a summary of a workflow run

```
gh run view [<run-id>] [flags]
```

### Options


<dl class="flags">
	<dt><code>--exit-status</code></dt>
	<dd>Exit with non-zero status if run failed</dd>

	<dt><code>-j</code>, <code>--job &lt;string&gt;</code></dt>
	<dd>查看一个特定的 job ID</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>jq 表达式，过滤 JSON 输出</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>JSON 输出特殊字段</dd>

	<dt><code>--log</code></dt>
	<dd>查看 完整的日志</dd>

	<dt><code>--log-failed</code></dt>
	<dd>查看运行失败的日志</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>模板化输出</dd>

	<dt><code>-v</code>, <code>--verbose</code></dt>
	<dd>展示 job 步骤</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>浏览器打开</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# Interactively select a run to view, optionally selecting a single job
$ gh run view

# View a specific run
$ gh run view 12345

# View a specific job within a run
$ gh run view --job 456789

# View the full log for a specific job
$ gh run view --log --job 456789

# Exit non-zero if a run failed
$ gh run view 0451 --exit-status && echo "run pending or passed"
{% endraw %}{% endhighlight %}

### See also

* [gh run](./gh_run)
