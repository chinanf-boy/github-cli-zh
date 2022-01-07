

## gh release download

```
gh release download [<tag>] [flags]
```

从GitHub发行版下载资产。

如果没有显式的标记名参数，资源将从项目的最新版本下载。在这种情况下，需要“--pattern”。

### Options

<dl class="flags">
	<dt><code>-A</code>, <code>--archive &lt;format&gt;</code></dt>
	<dd>Download the source code archive in the specified format (zip or tar.gz)</dd>

```
<dt><code>-D</code>, <code>--dir &lt;string&gt;</code></dt>
<dd>The directory to download files into</dd>

<dt><code>-p</code>, <code>--pattern &lt;stringArray&gt;</code></dt>
<dd>Download only assets that match a glob pattern</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash


# download all assets from a specific release

$gh发布下载v1。2.3

# download only Debian packages for the latest release

$gh发布下载——模式“\*。黛布

# specify multiple file patterns

$gh发布下载-p'*.deb'-p'*.rpm'

# download the archive of the source code for a release

$gh发布下载v1。2.3--archive=zip
```


### See also

-   [gh release](./gh_release)
