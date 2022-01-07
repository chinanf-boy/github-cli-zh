

## gh repo fork

```
gh repo fork [<repository>] [-- <gitflags>...] [flags]
```

创建存储库的分支。

在没有参数的情况下，创建当前存储库的分支。否则，分叉指定的存储库。

默认情况下，新的fork被设置为“origin”remote，任何现有的origin remote都被重命名为“upstream”。要改变这种行为，您可以使用--remote name为新fork的remote设置一个名称。

其他“git clone”标志可以通过在“--”之后列出来传入。

### Options

<dl class="flags">
	<dt><code>--clone</code></dt>
	<dd>Clone the fork {true|false}</dd>

<dt><code>--org &lt;string&gt;</code></dt>
<dd>Create the fork in an organization</dd>

<dt><code>--remote</code></dt>
<dd>Add remote for fork {true|false}</dd>

<dt><code>--remote-name &lt;string&gt;</code></dt>
<dd>Specify a name for a fork&#39;s new remote.</dd>

</dl>

### See also

-   [gh repo](./gh_repo)
