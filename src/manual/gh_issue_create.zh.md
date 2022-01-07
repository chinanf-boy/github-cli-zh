

## gh issue create

创刊

```
gh issue create [flags]
```

### Options

<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;login&gt;</code></dt>
	<dd>Assign people by their login. Use &#34;@me&#34; to self-assign.</dd>

```
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
<dd>Supply a title. Will prompt for one otherwise.</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open the browser to create an issue</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash
$gh issue create--title“我发现了一个bug”--body“没什么用”$gh issue create--label“bug，需要帮助”$gh issue create--label“需要帮助”$gh issue create--assignment monalisa，hubot$gh issue create--assignment“@me”$gh issue create--project“路线图”{%endraw%}{%endhighlight

### See also

-   [gh issue](./gh_issue)
