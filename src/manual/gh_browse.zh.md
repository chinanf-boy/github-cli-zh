## gh browse

```
gh browse [<number> | <path>] [flags]
```

在 web 浏览器中，打开 GitHub 存储库。

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>换分支</dd>

<dt><code>-c</code>, <code>--commit</code></dt>
<dd>打开最后的 commit </dd>

<dt><code>-n</code>, <code>--no-browser</code></dt>
<dd>给 URL，不打开浏览器</dd>

<dt><code>-p</code>, <code>--projects</code></dt>
<dd>打开，库项目</dd>

<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
<dd> [HOST/]OWNER/REPO 格式的库</dd>

<dt><code>-s</code>, <code>--settings</code></dt>
<dd>打开，repository settings</dd>

<dt><code>-w</code>, <code>--wiki</code></dt>
<dd>打开，repository wiki</dd>

</dl>

### Examples

```bash
$gh browse
#=>打开当前存储库的主页

$gh browse 217
#=>打开未结问题或拉取请求 217

$gh browse --settings
#=>打开存储库设置

$gh browse main.go:312
#=>打开 main.go 第 312 行

$gh browse main.go --branch main
#=>打开 main.go 进入 main 分支
```

### See also

- [gh](./gh.zh.md)
