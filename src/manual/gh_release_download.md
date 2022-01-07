

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
	<dd>Download the source code archive in the specified format (zip or tar.gz)</dd>

	<dt><code>-D</code>, <code>--dir &lt;string&gt;</code></dt>
	<dd>The directory to download files into</dd>

	<dt><code>-p</code>, <code>--pattern &lt;stringArray&gt;</code></dt>
	<dd>Download only assets that match a glob pattern</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
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
