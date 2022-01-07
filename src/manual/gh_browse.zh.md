## gh browse

```
gh browse [<number> | <path>] [flags]
```

在 web 浏览器中，打开 GitHub 存储库。

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>Select another branch by passing in the branch name</dd>

<dt><code>-c</code>, <code>--commit</code></dt>
<dd>Open the last commit</dd>

<dt><code>-n</code>, <code>--no-browser</code></dt>
<dd>Print destination URL instead of opening the browser</dd>

<dt><code>-p</code>, <code>--projects</code></dt>
<dd>Open repository projects</dd>

<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>

<dt><code>-s</code>, <code>--settings</code></dt>
<dd>Open repository settings</dd>

<dt><code>-w</code>, <code>--wiki</code></dt>
<dd>Open repository wiki</dd>
```

</dl>

### Examples

```bash
$gh browse
#=>打开当前存储库的主页

$gh browse 217
#=>未结问题或拉取请求 217

$gh browse --settings
#=>打开存储库设置

$gh browse main.go:312
#=>打开主管道。到 312 号线

$gh browse main.go --branch main
#=>打开总管。进入主分支
```


### See also

- [gh](./gh.zh.md)
