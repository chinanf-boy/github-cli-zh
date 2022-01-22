## gh run download

```
gh run download [<run-id>] [flags]
```

下载 GitHub Actions工作流运行生成的工件。

每个工件的内容将根据工件名称，提取到单独的目录。如果只指定了一个工件，它将被提取到当前目录中。

### Options

<dl class="flags">
	<dt><code>-D</code>, <code>--dir &lt;string&gt;</code></dt>
	<dd>下载的目录</dd>

<dt><code>-n</code>, <code>--name &lt;stringArray&gt;</code></dt>
<dd>仅下载匹配文件名的工件</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
# 下载 run-id 的所有工件
$ gh run download <run-id>

# 下载 run-id 的 name 工件
$ gh run download <run-id> -n <name>

# 下载 run-id 的 name1， name2 工件
$ gh run download -n <name1> -n <name2>

# 交互式下载
$ gh run download
```

### See also

- [gh run](./gh_run.zh.md)
