

## gh release create

```
gh release create [<tag>] [<files>...]
```

Create a new GitHub Release for a repository.

A list of asset files may be given to upload to the new release. To define a
display label for an asset, append text starting with `#` after the file name.

If a matching git tag does not yet exist, one will automatically get created
from the latest state of the default branch. Use `--target` to override this.
To fetch the new tag locally after the release, do `git fetch --tags origin`.

To create a release from an annotated git tag, first create one locally with
git, push the tag to GitHub, then run this command.

When using automatically generated Release 笔记, a Release 标题 will also be automatically
generated unless a title was explicitly passed. Additional Release 笔记 can be prepended to
automatically generated notes by using the notes parameter.


### Options


<dl class="flags">
	<dt><code>--discussion-category &lt;string&gt;</code></dt>
	<dd>开始指定主题分类的讨论</dd>

	<dt><code>-d</code>, <code>--draft</code></dt>
	<dd>一个草稿版本</dd>

	<dt><code>--generate-notes</code></dt>
	<dd>自动生成，release 的 标题与笔记</dd>

	<dt><code>-n</code>, <code>--notes &lt;string&gt;</code></dt>
	<dd>Release 笔记</dd>

	<dt><code>-F</code>, <code>--notes-file &lt;file&gt;</code></dt>
	<dd>用文件，读笔记 (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-p</code>, <code>--prerelease</code></dt>
	<dd>预览版</dd>

	<dt><code>--target &lt;branch&gt;</code></dt>
	<dd>指定的分支或是完整的 commit SHA (default: main branch)</dd>

	<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
	<dd>Release 标题</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
Interactively create a release
$ gh release create

Interactively create a release from specific tag
$ gh release create v1.2.3

Non-interactively create a release
$ gh release create v1.2.3 --notes "bugfix release"

Use automatically generated Release 笔记
$ gh release create v1.2.3 --generate-notes

Use Release 笔记 from a file
$ gh release create v1.2.3 -F changelog.md

Upload all tarballs in a directory as release assets
$ gh release create v1.2.3 ./dist/*.tgz

Upload a release asset with a display label
$ gh release create v1.2.3 '/path/to/asset.zip#My display label'

Create a release and start a discussion
$ gh release create v1.2.3 --discussion-category "General"
{% endraw %}{% endhighlight %}

### See also

* [gh release](./gh_release)
