---
layout: manual
permalink: /:path/:basename
---

## gh auth login

```
gh auth login [flags]
```

Authenticate with a GitHub host.

The default authentication mode is a web-based browser flow.

Alternatively, pass in a token on standard input by using `--with-token`.
The minimum required scopes for the token are: "repo", "read:org".

The --scopes flag accepts a comma separated list of scopes you want your gh credentials to have. If
absent, this command ensures that gh has access to a minimum set of scopes.


### Options


<dl class="flags">
	<dt><code>-h</code>, <code>--hostname &lt;string&gt;</code></dt>
	<dd>The hostname of the GitHub instance to authenticate with</dd>

	<dt><code>-s</code>, <code>--scopes &lt;strings&gt;</code></dt>
	<dd>Additional authentication scopes for gh to have</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open a browser to authenticate</dd>

	<dt><code>--with-token</code></dt>
	<dd>Read token from standard input</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# start interactive setup
$ gh auth login

# authenticate against github.com by reading the token from a file
$ gh auth login --with-token < mytoken.txt

# authenticate with a specific GitHub Enterprise Server instance
$ gh auth login --hostname enterprise.internal
{% endraw %}{% endhighlight %}

### See also

* [gh auth](./gh_auth)
