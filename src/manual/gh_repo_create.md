---
layout: manual
permalink: /:path/:basename
---

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
	<dd>Clone the new repository to the current directory</dd>

	<dt><code>-d</code>, <code>--description &lt;string&gt;</code></dt>
	<dd>Description of the repository</dd>

	<dt><code>--disable-issues</code></dt>
	<dd>Disable issues in the new repository</dd>

	<dt><code>--disable-wiki</code></dt>
	<dd>Disable wiki in the new repository</dd>

	<dt><code>-g</code>, <code>--gitignore &lt;string&gt;</code></dt>
	<dd>Specify a gitignore template for the repository</dd>

	<dt><code>-h</code>, <code>--homepage &lt;URL&gt;</code></dt>
	<dd>Repository home page URL</dd>

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
