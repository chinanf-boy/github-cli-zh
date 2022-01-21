

## gh release download

```
gh release download [<tag>] [flags]
```

Download assets from a GitHub release.

Without an explicit tag name argument, assets are downloaded from the
latest release in the project. In this case, '--pattern' is required.


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

{% highlight bash %}{% raw %}
# download all assets from a specific release
$ gh release download v1.2.3

# download only Debian packages for the latest release
$ gh release download --pattern '*.deb'

# specify multiple file patterns
$ gh release download -p '*.deb' -p '*.rpm'

# download the archive of the source code for a release
$ gh release download v1.2.3 --archive=zip
{% endraw %}{% endhighlight %}

### See also

* [gh release](./gh_release)
