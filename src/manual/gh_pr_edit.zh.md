## gh pr edit

```
gh pr edit [<number> | <url> | <branch>] [flags]
```

编辑拉取请求。

在没有参数的情况下，将选择属于当前分支的请求。

### Options

<dl class="flags">
	<dt><code>--add-assignee &lt;login&gt;</code></dt>
	<dd>通过 login，添加 关联的用户。使用 &#34;@me&#34; 关联自己.</dd>

<dt><code>--add-label &lt;name&gt;</code></dt>
<dd>通过 name，添加标签</dd>

<dt><code>--add-project &lt;name&gt;</code></dt>
<dd>将 pull request 添加到 name 项目</dd>

<dt><code>--add-reviewer &lt;login&gt;</code></dt>
<dd>通过 login ，添加审查人员.</dd>

<dt><code>-B</code>, <code>--base &lt;branch&gt;</code></dt>
<dd>更改 PR 的基分支</dd>

<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
<dd>设置新的主体内容.</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>文件读取主体内容 (用&#34;-&#34; 的话，就从标准输入读取)</dd>

<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
<dd>编辑 name 里程牌</dd>

<dt><code>--remove-assignee &lt;login&gt;</code></dt>
<dd>移除 login 的人员配置. 使用 &#34;@me&#34; 就移除自己</dd>

<dt><code>--remove-label &lt;name&gt;</code></dt>
<dd>移除 name 标签</dd>

<dt><code>--remove-project &lt;name&gt;</code></dt>
<dd>移除 name 项目的 PR</dd>

<dt><code>--remove-reviewer &lt;login&gt;</code></dt>
<dd>通过 login ，移除审查人员.</dd>

<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
<dd>设置新的标题.</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
$ gh pr edit 23 --title "I found a bug" --body "Nothing works"
$ gh pr edit 23 --add-label "bug,help wanted" --remove-label "core"
$ gh pr edit 23 --add-reviewer monalisa,hubot  --remove-reviewer myorg/team-name
$ gh pr edit 23 --add-assignee "@me" --remove-assignee monalisa,hubot
$ gh pr edit 23 --add-project "Roadmap" --remove-project v1,v2
$ gh pr edit 23 --milestone "Version 1"
```

### See also

- [gh pr](./gh_pr.zh.md)
