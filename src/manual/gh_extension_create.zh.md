## gh extension create

创建一个新的扩展名

```
gh extension create [<name>] [flags]
```

### Options

<dl class="flags">
	<dt><code>--precompiled &lt;string&gt;</code></dt>
	<dd>预编译扩展。可能的值: go, other</dd>
</dl>

### Examples

```bash
# 交互式
gh extension create

# 创建一个 script-based 扩展
gh extension create foobar

# 创建一个 Go 扩展
gh extension create --precompiled=go foobar

# 创建一个 non-Go precompiled 扩展
gh extension create --precompiled=other foobar
```

### See also

- [gh extension](./gh_extension.zh.md)
