

## gh repo view

```
gh repo view [<repository>] [flags]
```

显示GitHub存储库的描述和自述。

如果没有参数，将显示当前目录的存储库。

使用“--web”，改为在web浏览器中打开存储库。

使用“--branch”，查看存储库的特定分支。

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>View a specific branch of the repository</dd>

```
<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
<dd>Filter JSON output using a jq expression</dd>

<dt><code>--json &lt;fields&gt;</code></dt>
<dd>Output JSON with the specified fields</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>Format JSON output using a Go template</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open a repository in the browser</dd>
```

</dl>

### See also

-   [gh repo](./gh_repo)
