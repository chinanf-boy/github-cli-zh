---
layout: manual
permalink: /:path/:basename
---

## gh formatting

Some gh commands support exporting the data as JSON as an alternative to their usual
line-based plain text output. This is suitable for passing structured data to scripts.
The JSON output is enabled with the `--json` option, followed by the list of fields
to fetch. Use the flag without a value to get the list of available fields.

The `--jq` option accepts a query in jq syntax and will print only the resulting
values that match the query. This is equivalent to piping the output to `jq -r`,
but does not require the jq utility to be installed on the system. To learn more
about the query syntax, see: <https://stedolan.github.io/jq/manual/v1.6/>

With `--template`, the provided Go template is rendered using the JSON data as input.
For the syntax of Go templates, see: <https://golang.org/pkg/text/template/>

The following functions are available in templates:
- `autocolor`: like `color`, but only emits color to terminals
- `color <style> <input>`: colorize input using <https://github.com/mgutz/ansi>
- `join <sep> <list>`: joins values in the list using a separator
- `pluck <field> <list>`: collects values of a field from all items in the input
- `tablerow <fields>...`: aligns fields in output vertically as a table
- `tablerender`: renders fields added by tablerow in place
- `timeago <time>`: renders a timestamp as relative to now
- `timefmt <format> <time>`: formats a timestamp using Go's Time.Format function
- `truncate <length> <input>`: ensures input fits within length


### Examples

{% highlight bash %}{% raw %}
# format issues as table
$ gh issue list --json number,title --template \
  '{{range .}}{{tablerow (printf "#%v" .number | autocolor "green") .title}}{{end}}'

# format a pull request using multiple tables with headers
$ gh pr view 3519 --json number,title,body,reviews,assignees --template \
  '{{printf "#%v" .number}} {{.title}}

  {{.body}}

  {{tablerow "ASSIGNEE" "NAME"}}{{range .assignees}}{{tablerow .login .name}}{{end}}{{tablerender}}
  {{tablerow "REVIEWER" "STATE" "COMMENT"}}{{range .reviews}}{{tablerow .author.login .state .body}}{{end}}
  '
{% endraw %}{% endhighlight %}

### See also

* [gh](./gh)
