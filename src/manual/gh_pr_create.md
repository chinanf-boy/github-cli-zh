---
layout: manual
permalink: /:path/:basename
---

## gh pr create

```
gh pr create [flags]
```

Create a pull request on GitHub.

When the current branch isn't fully pushed to a git remote, a prompt will ask where
to push the branch and offer an option to fork the base repository. Use `--head` to
explicitly skip any forking or pushing behavior.

A prompt will also ask for the title and the body of the pull request. Use `--title`
and `--body` to skip this, or use `--fill` to autofill these values from git commits.

Link an issue to the pull request by referencing the issue in the body of the pull
request. If the body text mentions `Fixes #123` or `Closes #123`, the referenced issue
will automatically get closed when the pull request gets merged.

By default, users with write access to the base repository can push new commits to the
head branch of the pull request. Disable this with `--no-maintainer-edit`.


### Options


<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;login&gt;</code></dt>
	<dd>Assign people by their login. Use &#34;@me&#34; to self-assign.</dd>

	<dt><code>-B</code>, <code>--base &lt;branch&gt;</code></dt>
	<dd>The branch into which you want your code merged</dd>

	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>Body for the pull request</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>Read body text from file</dd>

	<dt><code>-d</code>, <code>--draft</code></dt>
	<dd>Mark pull request as a draft</dd>

	<dt><code>-f</code>, <code>--fill</code></dt>
	<dd>Do not prompt for title/body and just use commit info</dd>

	<dt><code>-H</code>, <code>--head &lt;branch&gt;</code></dt>
	<dd>The branch that contains commits for your pull request (default: current branch)</dd>

	<dt><code>-l</code>, <code>--label &lt;name&gt;</code></dt>
	<dd>Add labels by name</dd>

	<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
	<dd>Add the pull request to a milestone by name</dd>

	<dt><code>--no-maintainer-edit</code></dt>
	<dd>Disable maintainer&#39;s ability to modify pull request</dd>

	<dt><code>-p</code>, <code>--project &lt;name&gt;</code></dt>
	<dd>Add the pull request to projects by name</dd>

	<dt><code>--recover &lt;string&gt;</code></dt>
	<dd>Recover input from a failed run of create</dd>

	<dt><code>-r</code>, <code>--reviewer &lt;handle&gt;</code></dt>
	<dd>Request reviews from people or teams by their handle</dd>

	<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
	<dd>Title for the pull request</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open the web browser to create a pull request</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh pr create --title "The bug is fixed" --body "Everything works again"
$ gh pr create --reviewer monalisa,hubot  --reviewer myorg/team-name
$ gh pr create --project "Roadmap"
$ gh pr create --base develop --head monalisa:feature
{% endraw %}{% endhighlight %}

### See also

* [gh pr](./gh_pr)
