

## gh gist create

```
gh gist create [<filename>... | -] [flags]
```

Create a new GitHub gist with given contents.

Gists can be created from one or multiple files. Alternatively, pass "-" as
file name to read from standard input.

By default, gists are secret; use '--public' to make publicly listed ones.


### Options


<dl class="flags">
	<dt><code>-d</code>, <code>--desc &lt;string&gt;</code></dt>
	<dd>A description for this gist</dd>

	<dt><code>-f</code>, <code>--filename &lt;string&gt;</code></dt>
	<dd>Provide a filename to be used when reading from standard input</dd>

	<dt><code>-p</code>, <code>--public</code></dt>
	<dd>List the gist publicly (default: secret)</dd>

	<dt><code>-w</code>, <code>--web</code></dt>
	<dd>Open the web browser with created gist</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# publish file 'hello.py' as a public gist
$ gh gist create --public hello.py

# create a gist with a description
$ gh gist create hello.py -d "my Hello-World program in Python"

# create a gist containing several files
$ gh gist create hello.py world.py cool.txt

# read from standard input to create a gist
$ gh gist create -

# create a gist from output piped from another command
$ cat cool.txt | gh gist create
{% endraw %}{% endhighlight %}

### See also

* [gh gist](./gh_gist)
