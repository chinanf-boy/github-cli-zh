

## gh pr view

```
gh pr view [<number> | <url> | <branch>] [flags]
```

显示标题、正文和有关拉动请求的其他信息。

在没有参数的情况下，将显示属于当前分支的请求。

使用“--web”，改为在web浏览器中打开拉取请求。

### Options

<dl class="flags">
	<dt><code>-c</code>, <code>--comments</code></dt>
	<dd>View pull request comments</dd>

<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
<dd>jq 表达式，过滤 JSON 输出</dd>

<dt><code>--json &lt;fields&gt;</code></dt>
<dd>JSON 输出特殊字段</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>模板化输出</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open a pull request in the browser</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### See also

-   [gh pr](./gh_pr)
