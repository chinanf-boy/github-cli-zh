## gh repo create

```
gh repo create [<name>] [flags]
```

创建一个新的 GitHub 存储库。

要以交互方式创建存储库，请使用`gh repo create`，不带参数。

要以非交互方式创建远程存储库，请提供存储库名称和`--public`, `--private`或`--internal`，通过`--clone`在本地克隆新存储库。

要从现有本地存储库创建远程存储库，请使用`--source`。默认情况下，远程存储库名称将是源目录的名称。通过`--push`将任何本地提交推送到新存储库。

### Options

<dl class="flags">
	<dt><code>-c</code>, <code>--clone</code></dt>
	<dd>Clone 新的存储库到当前目录</dd>

<dt><code>-d</code>, <code>--description &lt;string&gt;</code></dt>
<dd>存储库的描述</dd>

<dt><code>--disable-issues</code></dt>
<dd>禁用 issues</dd>

<dt><code>--disable-wiki</code></dt>
<dd>禁用 wiki</dd>

<dt><code>-g</code>, <code>--gitignore &lt;string&gt;</code></dt>
<dd>指定一个 gitignore 的模板</dd>

<dt><code>-h</code>, <code>--homepage &lt;URL&gt;</code></dt>
<dd>主页URL</dd>

<dt><code>--internal</code></dt>
<dd>内部可见</dd>

<dt><code>-l</code>, <code>--license &lt;string&gt;</code></dt>
<dd>指定开源的协议</dd>

<dt><code>--private</code></dt>
<dd>私有存储库</dd>

<dt><code>--public</code></dt>
<dd>公开存储库</dd>

<dt><code>--push</code></dt>
<dd>推送本地的 commits 到新的存储库</dd>

<dt><code>-r</code>, <code>--remote &lt;string&gt;</code></dt>
<dd>指定 remote 名称</dd>

<dt><code>-s</code>, <code>--source &lt;string&gt;</code></dt>
<dd>指定存储库的源代码路径e</dd>

<dt><code>-t</code>, <code>--team &lt;name&gt;</code></dt>
<dd>可以访问存储库的组织名字</dd>

<dt><code>-p</code>, <code>--template &lt;repository&gt;</code></dt>
<dd>让新的存储库，基于 一个模板存储库生成</dd>
</dl>

### Examples

```bash
# 交互式创建一个 存储库
gh repo create

# 创建一个新的远程存储库，并将它 clone 到本地
gh repo create my-project --public --clone

# 以本地目录为基础，创建一个新的远程存储库
gh repo create my-project --private --source=. --remote=upstream
```

### See also

- [gh repo](./gh_repo.zh.md)
