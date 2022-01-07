---
layout: manual
permalink: /:path/:basename
---

## gh extension install

```
gh extension install <repository>
```

Install a GitHub repository locally as a GitHub CLI extension.

The repository argument can be specified in "owner/repo" format as well as a full URL.
The URL format is useful when the repository is not hosted on github.com.

To install an extension in development from the current directory, use "." as the
value of the repository argument.

See the list of available extensions at <https://github.com/topics/gh-extension>


### Examples

{% highlight bash %}{% raw %}
$ gh extension install owner/gh-extension
$ gh extension install https://git.example.com/owner/gh-extension
$ gh extension install .
{% endraw %}{% endhighlight %}

### See also

* [gh extension](./gh_extension)
