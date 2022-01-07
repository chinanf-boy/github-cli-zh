

## gh release view

```
gh release view [<tag>] [flags]
```

查看有关GitHub发行版的信息。

在没有显式标记名参数的情况下，将显示项目中的最新版本。

### Options

<dl class="flags">
	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

```
<dt><code>--json &lt;fields&gt;</code></dt>
<dd>Output JSON with the specified fields</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>Format JSON output using a Go template</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open the release in the browser</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### See also

-   [gh release](./gh_release)
