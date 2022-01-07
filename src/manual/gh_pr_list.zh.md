---
layout: manual
permalink: /:path/:basename
---

## gh pr list

列出并筛选此存储库中的请求

```
gh pr list [flags]
```

### Options

<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;string&gt;</code></dt>
	<dd>Filter by assignee</dd>

```
<dt><code>-A</code>, <code>--author &lt;string&gt;</code></dt>
<dd>Filter by author</dd>

<dt><code>-B</code>, <code>--base &lt;string&gt;</code></dt>
<dd>Filter by base branch</dd>

<dt><code>-d</code>, <code>--draft</code></dt>
<dd>Filter by draft state</dd>

<dt><code>-H</code>, <code>--head &lt;string&gt;</code></dt>
<dd>Filter by head branch</dd>

<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
<dd>Filter JSON output using a jq expression</dd>

<dt><code>--json &lt;fields&gt;</code></dt>
<dd>Output JSON with the specified fields</dd>

<dt><code>-l</code>, <code>--label &lt;strings&gt;</code></dt>
<dd>Filter by labels</dd>

<dt><code>-L</code>, <code>--limit &lt;int&gt;</code></dt>
<dd>Maximum number of items to fetch</dd>

<dt><code>-S</code>, <code>--search &lt;query&gt;</code></dt>
<dd>Search pull requests with query</dd>

<dt><code>-s</code>, <code>--state &lt;string&gt;</code></dt>
<dd>Filter by state: {open|closed|merged|all}</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>Format JSON output using a Go template</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open the browser to list the pull requests</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

{%highlight bash%}{%raw%}列表PRs由您编写$gh pr List--作者“@me”

分配给您的列表PRs$gh pr列表--受让人“@me”

按标签列出PRs，将多个标签与$gh pr列表相结合--标签错误--标签“优先级1”

使用搜索语法列出PRs$gh pr List--搜索“状态：成功审核：必需”

在web浏览器中打开PRs列表$gh pr list--web{%endraw%}{%endhighlight%}

### See also

-   [gh pr](./gh_pr)
