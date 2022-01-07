

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
	<dd>View a specific job ID from a run</dd>

	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>--log</code></dt>
	<dd>View full log for either a run or specific job</dd>

	<dt><code>--log-failed</code></dt>
	<dd>View the log for any failed steps in a run or specific job</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template</dd>

	<dt><code>-v</code>, <code>--verbose</code></dt>
	<dd>Show job steps</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open run in the browser</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
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
