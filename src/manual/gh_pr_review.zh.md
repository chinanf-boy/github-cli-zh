

## gh pr review

```
gh pr review [<number> | <url> | <branch>] [flags]
```

将审阅添加到请求中。

在没有参数的情况下，将审查属于当前分支的请求。

### Options

<dl class="flags">
	<dt><code>-a</code>, <code>--approve</code></dt>
	<dd>Approve pull request</dd>

<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
<dd>Specify the body of a review</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>文件读取主体内容 (用&#34;-&#34; 的话，就从标准输入读取)</dd>

<dt><code>-c</code>, <code>--comment</code></dt>
<dd>Comment on a pull request</dd>

<dt><code>-r</code>, <code>--request-changes</code></dt>
<dd>Request changes on a pull request</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash


# approve the pull request of the current branch

$gh公关审查——批准

# leave a review comment for the current branch

$gh公关评论——评论-b“有趣”

# add a review for a specific pull request

$gh公共关系审查123

# request changes on a specific pull request

$gh pr review 123-r-b“需要更多ASCII艺术”
```


### See also

-   [gh pr](./gh_pr.zh.md)
