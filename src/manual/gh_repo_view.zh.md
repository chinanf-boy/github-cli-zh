## gh repo view

```
gh repo view [<repository>] [flags]
```

显示 GitHub 存储库的描述和 README。

如果没有参数，将显示当前目录的存储库。

使用`--web`，改为在 web 浏览器中，打开存储库。

使用`--branch`，查看存储库的特定分支。

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>显示特定分支</dd>

<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
<dd>jq 表达式，过滤 JSON 输出</dd>

<dt><code>--json &lt;fields&gt;</code></dt>
<dd>JSON 输出特殊字段</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>模板化输出</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>浏览器打开</dd>

</dl>

### See also

- [gh repo](./gh_repo.zh.md)
