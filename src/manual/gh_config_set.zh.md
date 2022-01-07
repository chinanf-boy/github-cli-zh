## gh config set

使用给定密钥的值更新配置

```
gh config set <key> <value> [flags]
```

### Options

<dl class="flags">
	<dt><code>-h</code>, <code>--host &lt;string&gt;</code></dt>
	<dd>Set per-host setting</dd>
</dl>

### Examples

```bash
$ gh config set editor vim
$ gh config set editor "code --wait"
$ gh config set git_protocol ssh --host github.com
$ gh config set prompt disabled
```

### See also

- [gh config](./gh_config.zh.md)
