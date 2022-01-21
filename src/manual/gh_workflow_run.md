

## gh workflow run

```
gh workflow run [<workflow-id> | <workflow-name>] [flags]
```

Create a workflow_dispatch event for a given workflow.

This command will trigger GitHub Actions to run a given workflow file.  The given workflow file must
support a workflow_dispatch 'on' trigger in order to be run in this way.

If the workflow file supports inputs, they can be specified in a few ways:

- Interactively
- via -f or -F flags
- As JSON, via STDIN
 

### Options


<dl class="flags">
	<dt><code>-F</code>, <code>--field &lt;key=value&gt;</code></dt>
	<dd>Add a string parameter in key=value format, respecting @ syntax</dd>

	<dt><code>--json</code></dt>
	<dd>Read workflow inputs as JSON via STDIN</dd>

	<dt><code>-f</code>, <code>--raw-field &lt;key=value&gt;</code></dt>
	<dd>Add a string parameter in key=value format</dd>

	<dt><code>-r</code>, <code>--ref &lt;string&gt;</code></dt>
	<dd>The branch or tag name which contains the version of the workflow file you&#39;d like to run</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# Have gh prompt you for what workflow you'd like to run and interactively collect inputs
$ gh workflow run

# Run the workflow file 'triage.yml' at the remote's default branch
$ gh workflow run triage.yml

# Run the workflow file 'triage.yml' at a specified ref
$ gh workflow run triage.yml --ref my-branch

# Run the workflow file 'triage.yml' with command line inputs
$ gh workflow run triage.yml -f name=scully -f greeting=hello

# Run the workflow file 'triage.yml' with JSON via standard input
$ echo '{"name":"scully", "greeting":"hello"}' | gh workflow run triage.yml --json
{% endraw %}{% endhighlight %}

### See also

* [gh workflow](./gh_workflow)
