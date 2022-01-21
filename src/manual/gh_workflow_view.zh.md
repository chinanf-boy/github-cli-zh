## gh workflow view

查看工作流摘要

```
gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]
```

### Options

<dl class="flags">
	<dt><code>-r</code>, <code>--ref &lt;string&gt;</code></dt>
	<dd>想要查看的 分支与 tag 下的工作流文件</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>浏览器打开</dd>

<dt><code>-y</code>, <code>--yaml</code></dt>
<dd>查看工作流的 yaml 文件</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
# 交互式选择
$ gh workflow view

# 查看一个特定的工作流
$ gh workflow view 0451
```

### See also

- [gh workflow](./gh_workflow.zh.md)
