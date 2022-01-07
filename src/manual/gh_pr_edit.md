---
layout: manual
permalink: /:path/:basename
---

## gh pr edit

```
gh pr edit [<number> | <url> | <branch>] [flags]
```

Edit a pull request.

Without an argument, the pull request that belongs to the current branch
is selected.


### Options


<dl class="flags">
	<dt><code>--add-assignee &lt;login&gt;</code></dt>
	<dd>Add assigned users by their login. Use &#34;@me&#34; to assign yourself.</dd>

	<dt><code>--add-label &lt;name&gt;</code></dt>
	<dd>Add labels by name</dd>

	<dt><code>--add-project &lt;name&gt;</code></dt>
	<dd>Add the pull request to projects by name</dd>

	<dt><code>--add-reviewer &lt;login&gt;</code></dt>
	<dd>Add reviewers by their login.</dd>

	<dt><code>-B</code>, <code>--base &lt;branch&gt;</code></dt>
	<dd>Change the base branch for this pull request</dd>

	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>Set the new body.</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
	<dd>Edit the milestone the pull request belongs to by name</dd>

	<dt><code>--remove-assignee &lt;login&gt;</code></dt>
	<dd>Remove assigned users by their login. Use &#34;@me&#34; to unassign yourself.</dd>

	<dt><code>--remove-label &lt;name&gt;</code></dt>
	<dd>Remove labels by name</dd>

	<dt><code>--remove-project &lt;name&gt;</code></dt>
	<dd>Remove the pull request from projects by name</dd>

	<dt><code>--remove-reviewer &lt;login&gt;</code></dt>
	<dd>Remove reviewers by their login.</dd>

	<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
	<dd>Set the new title.</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh pr edit 23 --title "I found a bug" --body "Nothing works"
$ gh pr edit 23 --add-label "bug,help wanted" --remove-label "core"
$ gh pr edit 23 --add-reviewer monalisa,hubot  --remove-reviewer myorg/team-name
$ gh pr edit 23 --add-assignee "@me" --remove-assignee monalisa,hubot
$ gh pr edit 23 --add-project "Roadmap" --remove-project v1,v2
$ gh pr edit 23 --milestone "Version 1"
{% endraw %}{% endhighlight %}

### See also

* [gh pr](./gh_pr)
