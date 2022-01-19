## gh pr review

```
gh pr review [<number> | <url> | <branch>] [flags]
```

将一个审阅添加到请求中。

在没有参数的情况下，当前分支的请求被审查。

### Options

<dl class="flags">
	<dt><code>-a</code>, <code>--approve</code></dt>
	<dd>批准 pull request</dd>

<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
<dd>指定一个审查的主体内容</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>文件读取主体内容 (用&#34;-&#34; 的话，就从标准输入读取)</dd>

<dt><code>-c</code>, <code>--comment</code></dt>
<dd>给出评论</dd>

<dt><code>-r</code>, <code>--request-changes</code></dt>
<dd>要求 PR 修改</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
# 批准
$ gh pr review --approve

# 给评论
$ gh pr review --comment -b "interesting"

# 指定 123 PR，添加一个审查
$ gh pr review 123

# 要求 修改
$ gh pr review 123 -r -b "needs more ASCII art"
```

### See also

- [gh pr](./gh_pr.zh.md)
