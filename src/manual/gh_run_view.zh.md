

## gh run view

查看工作流运行的摘要

```
gh run view [<run-id>] [flags]
```

### Options

<dl class="flags">
	<dt><code>--exit-status</code></dt>
	<dd>Exit with non-zero status if run failed</dd>

```
<dt><code>-j</code>, <code>--job &lt;string&gt;</code></dt>
<dd>View a specific job ID from a run</dd>

<dt><code>-q</code>, <code>--jq &lt;expression&gt;</code></dt>
<dd>Filter JSON output using a jq expression</dd>

<dt><code>--json &lt;fields&gt;</code></dt>
<dd>Output JSON with the specified fields</dd>

<dt><code>--log</code></dt>
<dd>View full log for either a run or specific job</dd>

<dt><code>--log-failed</code></dt>
<dd>View the log for any failed steps in a run or specific job</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>Format JSON output using a Go template</dd>

<dt><code>-v</code>, <code>--verbose</code></dt>
<dd>Show job steps</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open run in the browser</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash


# Interactively select a run to view, optionally selecting a single job

$gh运行视图

# View a specific run

$gh运行视图12345

# View a specific job within a run

$gh运行视图--作业456789

# View the full log for a specific job

$gh运行视图--日志--作业456789

# Exit non-zero if a run failed

$gh run view 0451--退出状态&&echo“运行挂起或通过”
```


### See also

-   [gh run](./gh_run)
