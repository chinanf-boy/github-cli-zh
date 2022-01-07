---
layout: manual
permalink: /:path/:basename
---

## gh issue

Work with GitHub issues

### Commands

* [gh issue close](./gh_issue_close)
* [gh issue comment](./gh_issue_comment)
* [gh issue create](./gh_issue_create)
* [gh issue delete](./gh_issue_delete)
* [gh issue edit](./gh_issue_edit)
* [gh issue list](./gh_issue_list)
* [gh issue reopen](./gh_issue_reopen)
* [gh issue status](./gh_issue_status)
* [gh issue transfer](./gh_issue_transfer)
* [gh issue view](./gh_issue_view)


### Options


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh issue list
$ gh issue create --label bug
$ gh issue view --web
{% endraw %}{% endhighlight %}

### See also

* [gh](./gh)
