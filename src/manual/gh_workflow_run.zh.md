## gh workflow run

```
gh workflow run [<workflow-id> | <workflow-name>] [flags]
```

为给定工作流，创建 `workflow_dispatch` 事件。

此命令将触发 GitHub Actions，去运行给定的工作流文件。给定的工作流文件必须支持 `workflow_dispatch`上的（`on`）触发器，才能以这种方式运行。

如果工作流文件支持输入，可以通过以下几种方式指定输入：

- 交互式的
- 通过 `-f` 或 `-F`
- 作为 JSON，通过 STDIN 输入

### Options

<dl class="flags">
	<dt><code>-F</code>, <code>--field &lt;key=value&gt;</code></dt>
	<dd>key=value 模式的字符串参数，遵守 @ 语法</dd>

<dt><code>--json</code></dt>
<dd>通过 STDIN，读取 JSON 格式的工作流输入</dd>

<dt><code>-f</code>, <code>--raw-field &lt;key=value&gt;</code></dt>
<dd>key=value 模式的字符串参数</dd>

<dt><code>-r</code>, <code>--ref &lt;string&gt;</code></dt>
<dd>想要运行的 分支与 tag 下的工作流文件</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
# 交互式
$ gh workflow run

# 运行，默认分支下的 triage 工作流
$ gh workflow run triage.yml

# 运行，ref 分支下的 triage 工作流
$ gh workflow run triage.yml --ref my-branch

# 运行，默认分支下的 triage 工作流，带有参数
$ gh workflow run triage.yml -f name=scully -f greeting=hello

# 运行，默认分支下的 triage 工作流，带有参数（JSON 形式）
$ echo '{"name":"scully", "greeting":"hello"}' | gh workflow run triage.yml --json
```

### See also

- [gh workflow](./gh_workflow.zh.md)
