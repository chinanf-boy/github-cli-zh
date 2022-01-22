## gh auth login

```
gh auth login [flags]
```

通过 GitHub 主机进行身份验证。

默认身份验证模式是基于 web 的浏览器流。

或者，使用`--with-token`传进令牌。而令牌所需的最小范围为：`repo`, `read:org`。

`--scopes` 标志接受以逗号分隔的范围列表，这些范围是您希望 gh 凭据具有的范围。如果不存在，此命令将确保 gh 可以访问最小范围集。

### Options

<dl class="flags">
	<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
	<dd>身份验证的 GitHub 主址</dd>

<dt><code>-s</code>, <code>--scopes &lt;strings&gt;</code></dt>
<dd>权限范围</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>打开浏览器，进行身份验证</dd>

<dt><code>--with-token</code></dt>
<dd>从标准输入读取令牌</dd>

</dl>

### Examples

```bash
# 交互式登录
$ gh auth login

# 直接令牌登录

$ gh auth login --with-token < mytoken.txt

# 企业用户版本

$ gh auth login --hostname enterprise.internal
```

### See also

- [gh auth](./gh_auth.zh.md)
