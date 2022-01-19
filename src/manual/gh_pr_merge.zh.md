## gh pr merge

```
gh pr merge [<number> | <url> | <branch>] [flags]
```

在 GitHub 上，合并拉取请求。

在没有参数的情况下，将选择属于当前分支的请求。

### Options

<dl class="flags">
	<dt><code>--admin</code></dt>
	<dd>即便条件不达标，用管理员权限合并</dd>

<dt><code>--auto</code></dt>
<dd>条件符合，自动合并</dd>

<dt><code>-b</code>, <code>--body &lt;text&gt;</code></dt>
<dd>合并的主体内容</dd>

<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
<dd>文件读取主体内容 (用&#34;-&#34; 的话，就从标准输入读取)</dd>

<dt><code>-d</code>, <code>--delete-branch</code></dt>
<dd>合并后，删除本地与远程分支</dd>

<dt><code>--disable-auto</code></dt>
<dd>禁止自动合并</dd>

<dt><code>-m</code>, <code>--merge</code></dt>
<dd>合并</dd>

<dt><code>-r</code>, <code>--rebase</code></dt>
<dd>变基</dd>

<dt><code>-s</code>, <code>--squash</code></dt>
<dd>将多个提交变成一个，再合并</dd>

<dt><code>-t</code>, <code>--subject &lt;text&gt;</code></dt>
<dd>合并提交的主题</dd>

</dl>

### Options inherited from parent commands

<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>使用 [HOST/]OWNER/REPO 格式，选择另一存储库</dd>
</dl>

### See also

- [gh pr](./gh_pr.zh.md)
