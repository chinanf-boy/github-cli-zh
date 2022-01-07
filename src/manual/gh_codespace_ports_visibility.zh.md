## gh codespace ports visibility

更改转发端口的可见性

```
gh codespace ports visibility <port>:{public|private|org}...
```

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-c</code>, <code>--codespace &lt;string&gt;</code></dt>
	<dd>名字</dd>
</dl>

### Examples

```bash
gh codespace ports visibility 80:org 3000:private 8000:public
```

### See also

- [gh codespace ports](./gh_codespace_ports.zh.md)
