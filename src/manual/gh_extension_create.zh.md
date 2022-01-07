

## gh extension create

创建一个新的扩展名

```
gh extension create [<name>] [flags]
```

### Options

<dl class="flags">
	<dt><code>--precompiled &lt;string&gt;</code></dt>
	<dd>Create a precompiled extension. Possible values: go, other</dd>
</dl>

### Examples

```bash


# Use interactively

gh扩展创建

# Create a script-based extension

gh扩展创建foobar

# Create a Go extension

gh扩展创建--预编译=go foobar

# Create a non-Go precompiled extension

gh扩展创建--precompiled=other foobar
```


### See also

-   [gh extension](./gh_extension)
