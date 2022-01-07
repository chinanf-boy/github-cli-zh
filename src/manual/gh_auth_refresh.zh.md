## gh auth refresh

```
gh auth refresh [flags]
```

扩展或修复,存储凭据的权限范围

`--scopes` 标志接受以逗号分隔的范围列表，这些范围是您希望 gh 凭据具有的范围。如果不存在，此命令将确保 gh 可以访问最小范围集。

### Options

<dl class="flags">
<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
<dd>The GitHub 主机</dd>

<dt><code>-s</code>, <code>--scopes &lt;strings&gt;</code></dt>
<dd>权限范围</dd>

</dl>

### Examples

```bash
$ gh auth refresh --scopes write:org,read:public_key
# => 打开浏览器，添加 write:org 和 read:public_key 权限

$ gh auth refresh
# => 打开浏览器，确保具有最小权限
```

### See also

- [gh auth](./gh_auth.zh.md)
