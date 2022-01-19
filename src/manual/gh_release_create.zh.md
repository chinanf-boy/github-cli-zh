## gh release create

```
gh release create [<tag>] [<files>...]
```

为存储库创建新的 GitHub 版本(Release)。

新的版本，你可能要上传一系列的资源文件。要定义资源的显示标签，请在文件名之后，附加以`#`开头的文本。

如果匹配的 git tag 还不存在，那么将从默认分支的最新状态自动创建一个。使用`--target`来覆盖这个。要在发布后，在本地获取新 tag ，请执行以下操作`git fetch --tags origin`。

要从带注释的 git tag 创建发行版，首先使用 git 在本地创建一个，然后将 tag 推送到 GitHub，然后运行此命令。

使用自动生成的 release 说明时，也会自动生成 release 标题，除非，明确传递了标题。通过使用 notes 参数，可以在自动生成的备注前，添加其他 release 说明。

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

```bash
# 交互式创建一个 release
$ gh release create

# 交互式创建一个 v1.2.3 release 
$ gh release create v1.2.3

# 非交互式创建一个 release
$ gh release create v1.2.3 --notes "bugfix release"

# 使用自动生成 Release 笔记
$ gh release create v1.2.3 --generate-notes

# 使用文件，给出 Release 笔记
$ gh release create v1.2.3 -F changelog.md

# 上传 dist 目录下，所有的 tgz，作为资源
$ gh release create v1.2.3 ./dist/*.tgz

# 上传一个资源，带标签
$ gh release create v1.2.3 '/path/to/asset.zip#My display label'

# 创建一个 release，并开启讨论
$ gh release create v1.2.3 --discussion-category "General"
```

### See also

- [gh release](./gh_release.zh.md)
