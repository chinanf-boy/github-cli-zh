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
	<dd>Clone the new repository to the current directory</dd>

<dt><code>-d</code>, <code>--description &lt;string&gt;</code></dt>
<dd>存储库的描述</dd>

<dt><code>--disable-issues</code></dt>
<dd>Disable issues in the new repository</dd>

<dt><code>--disable-wiki</code></dt>
<dd>Disable wiki in the new repository</dd>

<dt><code>-g</code>, <code>--gitignore &lt;string&gt;</code></dt>
<dd>Specify a gitignore template for the repository</dd>

<dt><code>-h</code>, <code>--homepage &lt;URL&gt;</code></dt>
<dd>主页URL</dd>

<dt><code>--internal</code></dt>
<dd>Make the new repository internal</dd>

<dt><code>-l</code>, <code>--license &lt;string&gt;</code></dt>
<dd>Specify an Open Source License for the repository</dd>

<dt><code>--private</code></dt>
<dd>Make the new repository private</dd>

<dt><code>--public</code></dt>
<dd>Make the new repository public</dd>

<dt><code>--push</code></dt>
<dd>Push local commits to the new repository</dd>

<dt><code>-r</code>, <code>--remote &lt;string&gt;</code></dt>
<dd>Specify remote name for the new repository</dd>

<dt><code>-s</code>, <code>--source &lt;string&gt;</code></dt>
<dd>Specify path to local repository to use as source</dd>

<dt><code>-t</code>, <code>--team &lt;name&gt;</code></dt>
<dd>The name of the organization team to be granted access</dd>

<dt><code>-p</code>, <code>--template &lt;repository&gt;</code></dt>
<dd>Make the new repository based on a template repository</dd>
</dl>

### Examples

```bash

# create a repository interactively 
gh repo create

# create a new remote repository and clone it locally
gh repo create my-project --public --clone

# create a remote repository from the current directory
gh repo create my-project --private --source=. --remote=upstream
```

### See also

- [gh repo](./gh_repo.zh.md)
