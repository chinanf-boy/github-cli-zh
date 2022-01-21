## gh repo fork

```
gh repo fork [<repository>] [-- <gitflags>...] [flags]
```

创建存储库的副本。

在没有参数的情况下，创建**当前存储库**的副本。否则，副本化指定的存储库。

默认情况下，新的副本地址会是你的`origin`，以及任何现有的远程 `origin` 都被重命名为`upstream`。要改变这种行为，您可以使用`--remote-name`，自己设一个名字。

其他`git clone`标志可以在`--`之后，传入。

### Options

<dl class="flags">
	<dt><code>--clone</code></dt>
	<dd>Clone the fork {true|false}</dd>

<dt><code>--org &lt;string&gt;</code></dt>
<dd>在一个组织内，创建副本</dd>

<dt><code>--remote</code></dt>
<dd>要添加远程（上级）存储库吗 {true|false}</dd>

<dt><code>--remote-name &lt;string&gt;</code></dt>
<dd>指定一个 fork&#39;s 新名</dd>

</dl>

### See also

- [gh repo](./gh_repo.zh.md)
