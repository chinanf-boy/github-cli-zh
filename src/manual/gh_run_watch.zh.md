## gh run watch

观察 run，直到完成，并显示其进度

```
gh run watch <run-id> [flags]
```

### Options

<dl class="flags">
	<dt><code>--exit-status</code></dt>
	<dd>运行失败，退出代码 非零</dd>

<dt><code>-i</code>, <code>--interval &lt;int&gt;</code></dt>
<dd>刷新的时间间隙</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
# 终端一直观察，直到 run 完成
gh run watch

# 然后，试试运行其他命令
gh run watch && notify-send "run is done!"
```

### See also

- [gh run](./gh_run.zh.md)
