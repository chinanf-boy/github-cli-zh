---
layout: manual
permalink: /:path/:basename
---

## gh pr

Work with GitHub pull requests

### Commands

* [gh pr checkout](./gh_pr_checkout)
* [gh pr checks](./gh_pr_checks)
* [gh pr close](./gh_pr_close)
* [gh pr comment](./gh_pr_comment)
* [gh pr create](./gh_pr_create)
* [gh pr diff](./gh_pr_diff)
* [gh pr edit](./gh_pr_edit)
* [gh pr list](./gh_pr_list)
* [gh pr merge](./gh_pr_merge)
* [gh pr ready](./gh_pr_ready)
* [gh pr reopen](./gh_pr_reopen)
* [gh pr review](./gh_pr_review)
* [gh pr status](./gh_pr_status)
* [gh pr view](./gh_pr_view)


### Options


<dl class="flags">
	<dt><code>-R</code>, <code>--repo &lt;[HOST/]OWNER/REPO&gt;</code></dt>
	<dd>Select another repository using the [HOST/]OWNER/REPO format</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
$ gh pr checkout 353
$ gh pr create --fill
$ gh pr view --web
{% endraw %}{% endhighlight %}

### See also

* [gh](./gh)
