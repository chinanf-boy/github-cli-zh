## gh issue create

创建 issue

```
gh issue create [flags]
```

### Options

<dl class="flags">
	<dt><code>-a</code>, <code>--assignee &lt;login&gt;</code></dt>
	<dd>通过 login 分配人员。使用 &#34;@me&#34; 自我分配。</dd>

<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
<dd>提供主体内容。不填，也会提示</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>文件读取主体内容 (用&#34;-&#34; 的话，就从标准输入读取)</dd>

<dt><code>-l</code>, <code>--label &lt;name&gt;</code></dt>
<dd>通过 name，添加标签</dd>

<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
<dd>通过 name，添加 issue 到 name 里程牌</dd>

<dt><code>-p</code>, <code>--project &lt;name&gt;</code></dt>
<dd>通过 name，添加 issue 到 name 项目</dd>

<dt><code>--recover &lt;string&gt;</code></dt>
<dd>一次失败创建，带来的恢复输入</dd>

<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
<dd>提供一个标题。不填，也会提示</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>浏览器打开，创建 issue</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### Examples

```bash
$ gh issue create --title "I found a bug" --body "Nothing works"
$ gh issue create --label "bug,help wanted"
$ gh issue create --label bug --label "help wanted"
$ gh issue create --assignee monalisa,hubot
$ gh issue create --assignee "@me"
$ gh issue create --project "Roadmap"
```

### See also

- [gh issue](./gh_issue.zh.md)
