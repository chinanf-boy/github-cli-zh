

## gh pr create

```
gh pr create [flags]
```

Create a pull request on GitHub.

When the current branch isn't fully pushed to a git remote, a prompt will ask where
to push the branch and offer an option to fork the base repository. Use `--head` to
explicitly skip any forking or pushing behavior.

A prompt will also ask for the title and the body of the pull request. Use `--title`
and `--body` to skip this, or use `--fill` to autofill these values from git commits.

Link an issue to the pull request by referencing the issue in the body of the pull
request. If the body text mentions `Fixes #123` or `Closes #123`, the referenced issue
will automatically get closed when the pull request gets merged.

By default, users with write access to the base repository can push new commits to the
head branch of the pull request. Disable this with `--no-maintainer-edit`.


### Options


<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;login&gt;</code></dt>
	<dd>Assign people by their login. Use &#34;@me&#34; to self-assign.</dd>

	<dt><code>-B</code>, <code>--base &lt;branch&gt;</code></dt>
	<dd>要合并到的分支</dd>

	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>PR 的主体内容</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>读取文件，输入主体内容</dd>

	<dt><code>-d</code>, <code>--draft</code></dt>
	<dd>草稿版</dd>

	<dt><code>-f</code>, <code>--fill</code></dt>
	<dd>不用提示，使用 commit 的信息填入 title/body</dd>

	<dt><code>-H</code>, <code>--head &lt;branch&gt;</code></dt>
	<dd>包含你 commits 的分支 (default: current branch)</dd>

	<dt><code>-l</code>, <code>--label &lt;name&gt;</code></dt>
	<dd>添加标签</dd>

	<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
	<dd>Add the pull request to a milestone by name</dd>

	<dt><code>--no-maintainer-edit</code></dt>
	<dd>Disable maintainer&#39;s ability to modify pull request</dd>

	<dt><code>-p</code>, <code>--project &lt;name&gt;</code></dt>
	<dd>将 pull request 添加到 name 项目</dd>

	<dt><code>--recover &lt;string&gt;</code></dt>
	<dd>Recover input from a failed run of create</dd>

	<dt><code>-r</code>, <code>--reviewer &lt;handle&gt;</code></dt>
	<dd>PR 审查人员</dd>

	<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
	<dd>添加 标题</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>浏览器打开</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh pr create --title "The bug is fixed" --body "Everything works again"
$ gh pr create --reviewer monalisa,hubot  --reviewer myorg/team-name
$ gh pr create --project "Roadmap"
$ gh pr create --base develop --head monalisa:feature
{% endraw %}{% endhighlight %}

### See also

* [gh pr](./gh_pr)
