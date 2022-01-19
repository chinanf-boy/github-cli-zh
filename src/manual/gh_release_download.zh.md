## gh release download

```
gh release download [<tag>] [flags]
```

从 GitHub Release，下载资源。

如果没有显式的 tag 参数，资源将从项目的最新版本下载。在这种情况下，需要`--pattern`。

### Options

<dl class="flags">
	<dt><code>-A</code>, <code>--archive &lt;format&gt;</code></dt>
	<dd>下载的格式 (zip or tar.gz)</dd>

<dt><code>-D</code>, <code>--dir &lt;string&gt;</code></dt>
<dd>下载的位置</dd>

<dt><code>-p</code>, <code>--pattern &lt;stringArray&gt;</code></dt>
<dd>只下载符合 glob 匹配模式的资源</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
# 下载 v1.2.3 的所有资源
$ gh release download v1.2.3

# 仅下载 Debian 包
$ gh release download --pattern '*.deb'

# 下载多文件
$ gh release download -p '*.deb' -p '*.rpm'

# 下载压缩文件
$ gh release download v1.2.3 --archive=zip
```

### See also

- [gh release](./gh_release.zh.md)
