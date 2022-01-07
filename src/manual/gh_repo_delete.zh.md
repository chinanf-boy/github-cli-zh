---
layout: manual
permalink: /:path/:basename
---

## gh repo delete

```
gh repo delete [<repository>] [flags]
```

删除GitHub存储库。

在没有参数的情况下，删除当前存储库。否则，将删除指定的存储库。

删除需要“删除回购”范围的授权。要进行授权，请运行“gh auth refresh-s delete_repo”

### Options

<dl class="flags">
	<dt><code>--confirm</code></dt>
	<dd>confirm deletion without prompting</dd>
</dl>

### See also

-   [gh repo](./gh_repo)
