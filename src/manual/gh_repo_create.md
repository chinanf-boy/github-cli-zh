

## gh repo create

```
gh repo create [<name>] [flags]
```

Create a new GitHub repository.

To create a repository interactively, use `gh repo create` with no arguments.

To create a remote repository non-interactively, supply the repository name and one of `--public`, `--private`, or `--internal`.
Pass `--clone` to clone the new repository locally.

To create a remote repository from an existing local repository, specify the source directory with `--source`. 
By default, the remote repository name will be the name of the source directory. 
Pass `--push` to push any local commits to the new repository.


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

{% highlight bash %}{% raw %}
# create a repository interactively 
gh repo create

# create a new remote repository and clone it locally
gh repo create my-project --public --clone

# create a remote repository from the current directory
gh repo create my-project --private --source=. --remote=upstream
{% endraw %}{% endhighlight %}

### See also

* [gh repo](./gh_repo)
