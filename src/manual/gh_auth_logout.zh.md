## gh auth logout

```
gh auth logout [flags]
```

删除 GitHub 主机的身份验证。

以交互方式或通过--hostname 指定的方式，此命令删除主机的身份验证配置。

### Options

<dl class="flags">
	<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
	<dd>所要登出的服务主机</dd>
</dl>

### Examples

```bash
$ gh auth logout
# => select what host to log out of via a prompt

$ gh auth logout --hostname enterprise.internal
# => log out of specified host
```

### See also

- [gh auth](./gh_auth.zh.md)
