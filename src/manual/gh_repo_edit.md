

## gh repo edit

Edit repository settings

```
gh repo edit [<repository>] [flags]
```

### Options


<dl class="flags">
	<dt><code>--add-topic &lt;strings&gt;</code></dt>
	<dd>添加 存储库 标签主题</dd>

	<dt><code>--allow-forking</code></dt>
	<dd>允许被 fork</dd>

	<dt><code>--default-branch &lt;name&gt;</code></dt>
	<dd>设置默认的分支</dd>

	<dt><code>--delete-branch-on-merge</code></dt>
	<dd>当 pull requests 被合并，删除 HEAD 分支</dd>

	<dt><code>-d</code>, <code>--description &lt;string&gt;</code></dt>
	<dd>存储库的描述</dd>

	<dt><code>--enable-auto-merge</code></dt>
	<dd>启动 auto-merge（自动合并） 功能</dd>

	<dt><code>--enable-issues</code></dt>
	<dd>启用 issues</dd>

	<dt><code>--enable-merge-commit</code></dt>
	<dd>可以用 merge commit，合并 PR</dd>

	<dt><code>--enable-projects</code></dt>
	<dd>启用 projects</dd>

	<dt><code>--enable-rebase-merge</code></dt>
	<dd>可用变基（rebase）的方式合并 PR</dd>

	<dt><code>--enable-squash-merge</code></dt>
	<dd>可用，将多个commit变为一个的方式，合并PR</dd>

	<dt><code>--enable-wiki</code></dt>
	<dd>启用 wiki</dd>

	<dt><code>-h</code>, <code>--homepage &lt;URL&gt;</code></dt>
	<dd>主页URL</dd>

	<dt><code>--remove-topic &lt;strings&gt;</code></dt>
	<dd>移除存储库的标签主题</dd>

	<dt><code>--template</code></dt>
	<dd>可将存储库当成，模板存储库</dd>

	<dt><code>--visibility &lt;string&gt;</code></dt>
	<dd>将存储库的可见性改为 {public,private,internal}</dd>
</dl>


### See also

* [gh repo](./gh_repo)
