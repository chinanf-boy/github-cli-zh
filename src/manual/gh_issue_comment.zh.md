## gh issue comment

创建新的问题评论

```
gh issue comment {<number> | <url>} [flags]
```

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>提供主体内容。不填，也会提示</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>文件读取主体内容 (用&#34;-&#34; 的话，就从标准输入读取)</dd>

<dt><code>-e</code>, <code>--editor</code></dt>
<dd>通过 editor 添加主体</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>用浏览器打开网络链接，添加主体</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
$ gh issue comment 22 --body "I was able to reproduce this issue, lets fix it."
```

### See also

- [gh issue](./gh_issue.zh.md)
