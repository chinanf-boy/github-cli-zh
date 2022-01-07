

## gh workflow view

查看工作流摘要

```
gh workflow view [<workflow-id> | <workflow-name> | <filename>] [flags]
```

### Options

<dl class="flags">
	<dt><code>-r</code>, <code>--ref &lt;string&gt;</code></dt>
	<dd>The branch or tag name which contains the version of the workflow file you&#39;d like to view</dd>

```
<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open workflow in the browser</dd>

<dt><code>-y</code>, <code>--yaml</code></dt>
<dd>View the workflow yaml file</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash


# Interactively select a workflow to view

$gh工作流视图

# View a specific workflow

$gh工作流视图0451
```


### See also

-   [gh workflow](./gh_workflow)
