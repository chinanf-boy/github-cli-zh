

## gh run watch

观察跑步直到完成，并显示其进度

```
gh run watch <run-id> [flags]
```

### Options

<dl class="flags">
	<dt><code>--exit-status</code></dt>
	<dd>Exit with non-zero status if run fails</dd>

<dt><code>-i</code>, <code>--interval &lt;int&gt;</code></dt>
<dd>Refresh interval in seconds</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash


# Watch a run until it's done

长跑表

# Run some other command when the run is finished

gh运行监视和通知发送“运行完成！”
```


### See also

-   [gh run](./gh_run)
