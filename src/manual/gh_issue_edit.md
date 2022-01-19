

## gh issue edit

Edit an issue

```
gh issue edit {<number> | <url>} [flags]
```

### Options


<dl class="flags">
	<dt><code>--add-assignee &lt;login&gt;</code></dt>
	<dd>通过 login，添加 关联的用户。使用 &#34;@me&#34; 关联自己.</dd>

	<dt><code>--add-label &lt;name&gt;</code></dt>
	<dd>Add labels by name</dd>

	<dt><code>--add-project &lt;name&gt;</code></dt>
	<dd>Add the issue to projects by name</dd>

	<dt><code>-b</code>, <code>--body &lt;string&gt;</code></dt>
	<dd>设置新的主体内容.</dd>

	<dt><code>-F</code>, <code>--body-file &lt;file&gt;</code></dt>
	<dd>Read body text from file (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-m</code>, <code>--milestone &lt;name&gt;</code></dt>
	<dd>用 name，编辑下里程碑</dd>

	<dt><code>--remove-assignee &lt;login&gt;</code></dt>
	<dd>移除 login 的人员配置. 使用 &#34;@me&#34; 就移除自己</dd>

	<dt><code>--remove-label &lt;name&gt;</code></dt>
	<dd>移除 name 标签</dd>

	<dt><code>--remove-project &lt;name&gt;</code></dt>
	<dd>移除 name 项目</dd>

	<dt><code>-t</code>, <code>--title &lt;string&gt;</code></dt>
	<dd>设置新的标题.</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh issue edit 23 --title "I found a bug" --body "Nothing works"
$ gh issue edit 23 --add-label "bug,help wanted" --remove-label "core"
$ gh issue edit 23 --add-assignee "@me" --remove-assignee monalisa,hubot
$ gh issue edit 23 --add-project "Roadmap" --remove-project v1,v2
$ gh issue edit 23 --milestone "Version 1"
$ gh issue edit 23 --body-file body.txt
{% endraw %}{% endhighlight %}

### See also

* [gh issue](./gh_issue)
