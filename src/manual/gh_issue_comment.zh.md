

## gh issue comment

创建新的问题注释

```
gh issue comment {<number> | <url>} [flags]
```

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>Supply a body. Will prompt for one otherwise.</dd>

```
<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

<dt><code>-e</code>, <code>--editor</code></dt>
<dd>Add body using editor</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Add body in browser</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash
$gh问题注释22--body“我能够重现这个问题，让我们来修复它。”
```


### See also

-   [gh issue](./gh_issue)
