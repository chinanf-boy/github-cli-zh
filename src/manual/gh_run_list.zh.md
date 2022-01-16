

## gh run list

列出最近的工作流运行

```
gh run list [flags]
```

### Options

<dl class="flags">
	<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
	<dd>jq 表达式，过滤 JSON 输出</dd>

<dt><code>--json &lt;fields&gt;</code></dt>
<dd>JSON 输出特殊字段</dd>

<dt><code>-L</code>, <code>--limit &lt;int&gt;</code></dt>
<dd>Maximum number of runs to fetch</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>模板化输出</dd>

<dt><code>-w</code>, <code>--workflow &lt;string&gt;</code></dt>
<dd>Filter runs by workflow</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### See also

-   [gh run](./gh_run.zh.md)
