

## gh alias set

```
gh alias set <alias> <expansion> [flags]
```

Define a word that will expand to a full gh command when invoked.

The expansion may specify additional arguments and flags. If the expansion includes
positional placeholders such as "$1", extra arguments that follow the alias will be
inserted appropriately. Otherwise, extra arguments will be appended to the expanded
command.

Use "-" as expansion argument to read the expansion string from standard input. This
is useful to avoid quoting issues when defining expansions.

If the expansion starts with "!" or if "--shell" was given, the expansion is a shell
expression that will be evaluated through the "sh" interpreter when the alias is
invoked. This allows for chaining multiple commands via piping and redirection.


### Options


<dl class="flags">
	<dt><code>-s</code>, <code>--shell</code></dt>
	<dd>定义个 alias 传递给 shell 解释器，r</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# note: Command Prompt on Windows 要双引号
$ gh alias set pv 'pr view'
$ gh pv -w 123  #=> gh pr view -w 123

$ gh alias set bugs 'issue list --label=bugs'
$ gh bugs

$ gh alias set homework 'issue list --assignee @me'
$ gh homework

$ gh alias set epicsBy 'issue list --author="$1" --label="epic"'
$ gh epicsBy vilmibm  #=> gh issue list --author="vilmibm" --label="epic"

$ gh alias set --shell igrep 'gh issue list --label="$1" | grep "$2"'
$ gh igrep epic foo  #=> gh issue list --label="epic" | grep "foo"
{% endraw %}{% endhighlight %}

### See also

* [gh alias](./gh_alias)
