## gh issue edit

编辑问题

```
gh issue edit {<number> | <url>} [flags]
```

### Options

<dl class="flags">
	<dt><code>--add-assignee &lt;login&gt;</code></dt>
	<dd>Add assigned users by their login. Use &#34;@me&#34; to assign yourself.</dd>

<dt><code>--add-label &lt;name&gt;</code></dt>
<dd>通过 name，添加标签</dd>

<dt><code>--add-project &lt;name&gt;</code></dt>
<dd>通过 name，添加 issue 到 name 项目</dd>

<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
<dd>Set the new body.</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>文件读取主体内容 (用&#34;-&#34; 的话，就从标准输入读取)</dd>

<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
<dd>用 name，编辑下里程碑</dd>

<dt><code>--remove-assignee &lt;login&gt;</code></dt>
<dd>移除 login 的人员配置. 使用 &#34;@me&#34; 就移除自己</dd>

<dt><code>--remove-label &lt;name&gt;</code></dt>
<dd>Remove labels by name</dd>

<dt><code>--remove-project &lt;name&gt;</code></dt>
<dd>移除 name 项目</dd>

<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
<dd>Set the new title.</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
$ gh issue edit 23 --title "I found a bug" --body "Nothing works"
$ gh issue edit 23 --add-label "bug,help wanted" --remove-label "core"
$ gh issue edit 23 --add-assignee "@me" --remove-assignee monalisa,hubot
$ gh issue edit 23 --add-project "Roadmap" --remove-project v1,v2
$ gh issue edit 23 --milestone "Version 1"
$ gh issue edit 23 --body-file body.txt
```

### See also

- [gh issue](./gh_issue.zh.md)
