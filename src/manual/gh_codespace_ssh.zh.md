## gh codespace ssh

SSH 到一个代码空间

```
gh codespace ssh [<flags>...] [-- <ssh-flags>...] [<command>]
```

### Options

<dl class="flags">
	<dt><code>-c</code>, <code>--codespace &lt;string&gt;</code></dt>
	<dd>名字</dd>

<dt><code>-d</code>, <code>--debug</code></dt>
<dd>调试数据装入文件</dd>

<dt><code>--debug-file &lt;string&gt;</code></dt>
<dd>文件日志的路径</dd>

<dt><code>--profile &lt;string&gt;</code></dt>
<dd>所使用的 SSH profile 名称</dd>

<dt><code>--server-port &lt;int&gt;</code></dt>
<dd>SSH 服务器端口号 (0 =&gt; pick unused)</dd>

</dl>

### See also

- [gh codespace](./gh_codespace.zh.md)
