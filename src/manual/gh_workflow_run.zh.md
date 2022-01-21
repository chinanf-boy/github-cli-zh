## gh workflow run

```
gh workflow run [<workflow-id> | <workflow-name>] [flags]
```

为给定工作流创建工作流\\u 分派事件。

此命令将触发 GitHub 操作以运行给定的工作流文件。给定的工作流文件必须支持工作流调度“on”触发器才能以这种方式运行。

如果工作流文件支持输入，可以通过以下几种方式指定输入：

- 交互地
- 通过-f 或-f 标志
- 作为 JSON，通过 STDIN

### Options

<dl class="flags">
	<dt><code>-F</code>, <code>--field &lt;key=value&gt;</code></dt>
	<dd>Add a string parameter in key=value format, respecting @ syntax</dd>

```
<dt><code>--json</code></dt>
<dd>Read workflow inputs as JSON via STDIN</dd>

<dt><code>-f</code>, <code>--raw-field &lt;key=value&gt;</code></dt>
<dd>Add a string parameter in key=value format</dd>

<dt><code>-r</code>, <code>--ref &lt;string&gt;</code></dt>
<dd>The branch or tag name which contains the version of the workflow file you&#39;d like to run</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
# Have gh prompt you for what workflow you'd like to run and interactively collect inputs
$ gh workflow run

# Run the workflow file 'triage.yml' at the remote's default branch
$ gh workflow run triage.yml

# Run the workflow file 'triage.yml' at a specified ref
$ gh workflow run triage.yml --ref my-branch

# Run the workflow file 'triage.yml' with command line inputs
$ gh workflow run triage.yml -f name=scully -f greeting=hello

# Run the workflow file 'triage.yml' with JSON via standard input
$ echo '{"name":"scully", "greeting":"hello"}' | gh workflow run triage.yml --json
```

### See also

- [gh workflow](./gh_workflow)
