

## gh pr comment

```
gh pr comment [<number> | <url> | <branch>] [flags]
```

创建新的公关评论。

在没有参数的情况下，将选择属于当前分支的请求。			

使用“--web”，在web浏览器中对请求进行注释。

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>Supply a body. Will prompt for one otherwise.</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

<dt><code>-e</code>, <code>--editor</code></dt>
<dd>Add body using editor</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Add body in browser</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash
$gh pr comment 22--body“这看起来很棒，让我们部署它吧。”
```


### See also

-   [gh pr](./gh_pr.zh.md)
