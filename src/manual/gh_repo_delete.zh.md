## gh repo delete

```
gh repo delete [<repository>] [flags]
```

删除 GitHub 存储库。

在没有参数的情况下，删除当前存储库。或是，删除指定的存储库。

删除需要`delete_repo`范围的授权。要进行授权，请运行`gh auth refresh -s delete_repo`

### Options

<dl class="flags">
	<dt><code>--confirm</code></dt>
	<dd>直接通过提示</dd>
</dl>

### See also

- [gh repo](./gh_repo.zh.md)
