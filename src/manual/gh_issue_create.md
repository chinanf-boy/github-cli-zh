

## gh issue create

Create a new issue

```
gh issue create [flags]
```

### Options


<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;login&gt;</code></dt>
	<dd>Assign people by their login. Use &#34;@me&#34; to self-assign.</dd>

	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>Supply a body. Will prompt for one otherwise.</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-l</code>, <code>--label &lt;name&gt;</code></dt>
	<dd>Add labels by name</dd>

	<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
	<dd>Add the issue to a milestone by name</dd>

	<dt><code>-p</code>, <code>--project &lt;name&gt;</code></dt>
	<dd>Add the issue to projects by name</dd>

	<dt><code>--recover &lt;string&gt;</code></dt>
	<dd>Recover input from a failed run of create</dd>

	<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
	<dd>提供一个标题。不填，也会提示</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open the browser to create an issue</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh issue create --title "I found a bug" --body "Nothing works"
$ gh issue create --label "bug,help wanted"
$ gh issue create --label bug --label "help wanted"
$ gh issue create --assignee monalisa,hubot
$ gh issue create --assignee "@me"
$ gh issue create --project "Roadmap"
{% endraw %}{% endhighlight %}

### See also

* [gh issue](./gh_issue)
