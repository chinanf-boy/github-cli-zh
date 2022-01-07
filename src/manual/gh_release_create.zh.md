

## gh release create

```
gh release create [<tag>] [<files>...]
```

为存储库创建新的GitHub版本。

可能会提供一个资产文件列表以上载到新版本。要定义资源的显示标签，请附加以开头的文本`#`在文件名之后。

如果匹配的git标记还不存在，那么将从默认分支的最新状态自动创建一个。使用`--target`来覆盖这个。要在发布后在本地获取新标记，请执行以下操作`git fetch --tags origin`.

要从带注释的git标记创建发行版，首先使用git在本地创建一个，将标记推送到GitHub，然后运行此命令。

使用自动生成的发行说明时，也会自动生成发行标题，除非明确传递了标题。通过使用notes参数，可以在自动生成的备注前添加其他发行说明。

### Options

<dl class="flags">
	<dt><code>--discussion-category &lt;string&gt;</code></dt>
	<dd>Start a discussion of the specified category</dd>

```
<dt><code>-d</code>, <code>--draft</code></dt>
<dd>Save the release as a draft instead of publishing it</dd>

<dt><code>--generate-notes</code></dt>
<dd>Automatically generate title and notes for the release</dd>

<dt><code>-n</code>, <code>--notes &lt;string&gt;</code></dt>
<dd>Release notes</dd>

<dt><code>-F</code>, <code>--notes-file &lt;file&gt;</code></dt>
<dd>Read release notes from file (use &#34;-&#34; to read from standard input)</dd>

<dt><code>-p</code>, <code>--prerelease</code></dt>
<dd>Mark the release as a prerelease</dd>

<dt><code>--target &lt;branch&gt;</code></dt>
<dd>Target branch or full commit SHA (default: main branch)</dd>

<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
<dd>Release title</dd>
```

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>

### Examples

```bash
以交互方式创建版本$gh release create

以交互方式从特定标记$gh release create v1创建发布。2.3

以非交互方式创建版本$gh release create v1。2.3--注释“错误修复版本”

使用自动生成的发行说明$gh release create v1。2.3——生成注释

使用文件$gh release create v1中的发行说明。2.3-F变更记录。医学博士

将目录中的所有tarball作为发布资产$gh release create v1上传。2.3 ./dist/\*。tgz

上载带有显示标签$gh release create v1的发布资源。2.3'/path/to/asset。zip#我的显示标签'

创建发布并开始讨论$gh发布创建v1。2.3--讨论类别“一般”
```


### See also

-   [gh release](./gh_release)
