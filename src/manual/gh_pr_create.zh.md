## gh pr create

```
gh pr create [flags]
```

在 GitHub 上，创建拉取请求(PR)。

当当前分支未完全推送到 git 远程时，将出现一个提示，询问将分支推送到何处，并提供一个**fork 基本存储库**的选项。使用`--head`明确跳过任何 fork 或 push 行为。

提示还将要求 PR 的标题和主体内容。使用`--title`和`--body`可以跳过，或者使用`--fill`从 git commits 中，自动填充这些值。

通过引用 PR 主体内容中的 issue ，将 issue 链接到 PR 。如果主体内容提到`Fixes #123`或`Closes #123`，合并 PR 时，引用的 issue 将自动关闭。

默认情况下，对基本存储库具有写访问权限的用户，可以将新 commit 推送到 PR 的头分支。使用`--no-maintainer-edit`禁用此选项。

### Options

<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;login&gt;</code></dt>
	<dd>通过 login 分配人员。使用 &#34;@me&#34; 自我分配。</dd>

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
<dd>通过 name，添加 issue 到 name 里程牌</dd>

<dt><code>--no-maintainer-edit</code></dt>
<dd>Disable maintainer&#39;s ability to modify pull request</dd>

<dt><code>-p</code>, <code>--project &lt;name&gt;</code></dt>
<dd>将 pull request 添加到 name 项目</dd>

<dt><code>--recover &lt;string&gt;</code></dt>
<dd>一次失败创建，带来的恢复输入</dd>

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

```bash
$ gh pr create --title "The bug is fixed" --body "Everything works again"
$ gh pr create --reviewer monalisa,hubot  --reviewer myorg/team-name
$ gh pr create --project "Roadmap"
$ gh pr create --base develop --head monalisa:feature
```

### See also

- [gh pr](./gh_pr.zh.md)
