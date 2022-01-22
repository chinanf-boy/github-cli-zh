

## gh api

```
gh api <endpoint> [flags]
```

Makes an authenticated HTTP request to the GitHub API and prints the response.

The endpoint argument should either be a path of a GitHub API v3 endpoint, or
"graphql" to access the GitHub API v4.

Placeholder values "{owner}", "{repo}", and "{branch}" in the endpoint argument will
get replaced with values from the repository of the current directory. Note that in
some shells, for example PowerShell, you may need to enclose any value that contains
"{...}" in quotes to prevent the shell from applying special meaning to curly braces.

The default HTTP request method is "GET" normally and "POST" if any parameters
were added. Override the method with `--method`.

Pass one or more `-f/--raw-field` values in "key=value" format to add static string 
parameters to the request payload. To add non-string or otherwise dynamic values, see
`--field` below. Note that adding request parameters will automatically switch the
request method to POST. To send the parameters as a GET query string instead, use
`--method GET`.

The `-F/--field` flag has magic type conversion based on the format of the value:

- literal values "true", "false", "null", and integer numbers get converted to
  appropriate JSON types;
- placeholder values "{owner}", "{repo}", and "{branch}" get populated with values
  from the repository of the current directory;
- if the value starts with "@", the rest of the value is interpreted as a
  filename to read the value from. Pass "-" to read from standard input.

For GraphQL requests, all fields other than "query" and "operationName" are
interpreted as GraphQL variables.

Raw request body may be passed from the outside via a file specified by `--input`.
Pass "-" to read from standard input. In this mode, parameters specified via
`--field` flags are serialized into URL query parameters.

In `--paginate` mode, all pages of results will sequentially be requested until
there are no more pages of results. For GraphQL requests, this requires that the
original query accepts an `$endCursor: String` variable and that it fetches the
`pageInfo{ hasNextPage, endCursor }` set of fields from a collection.


### Options


<dl class="flags">
	<dt><code>--cache &lt;duration&gt;</code></dt>
	<dd>Cache the response, e.g. &#34;3600s&#34;, &#34;60m&#34;, &#34;1h&#34;</dd>

	<dt><code>-F</code>, <code>--field &lt;key=value&gt;</code></dt>
	<dd>Add a typed parameter in key=value format</dd>

	<dt><code>-H</code>, <code>--header &lt;key:value&gt;</code></dt>
	<dd>Add a HTTP request header 格式是 key=value</dd>

	<dt><code>--hostname &lt;string&gt;</code></dt>
	<dd>The GitHub hostname for the request (default &#34;github.com&#34;)</dd>

	<dt><code>-i</code>, <code>--include</code></dt>
	<dd>Include HTTP response headers in the output</dd>

	<dt><code>--input &lt;file&gt;</code></dt>
	<dd>The file to use as body for the HTTP request (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-q</code>, <code>--jq &lt;string&gt;</code></dt>
	<dd>Query to select values from the response using jq syntax</dd>

	<dt><code>-X</code>, <code>--method &lt;string&gt;</code></dt>
	<dd>The HTTP method for the request</dd>

	<dt><code>--paginate</code></dt>
	<dd>Make additional HTTP requests to fetch all pages of results</dd>

	<dt><code>-p</code>, <code>--preview &lt;strings&gt;</code></dt>
	<dd>Opt into GitHub API previews</dd>

	<dt><code>-f</code>, <code>--raw-field &lt;key=value&gt;</code></dt>
	<dd>key=value 模式的字符串参数</dd>

	<dt><code>--silent</code></dt>
	<dd>Do not print the response body</dd>

	<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
	<dd>Format the response using a Go template</dd>
</dl>


### Examples

{% highlight bash %}{% raw %}
# list releases in the current repository
$ gh api repos/{owner}/{repo}/releases

# post an issue comment
$ gh api repos/{owner}/{repo}/issues/123/comments -f body='Hi from CLI'

# add parameters to a GET request
$ gh api -X GET search/issues -f q='repo:cli/cli is:open remote'

# set a custom HTTP header
$ gh api -H 'Accept: application/vnd.github.v3.raw+json' ...

# opt into GitHub API previews
$ gh api --preview baptiste,nebula ...

# print only specific fields from the response
$ gh api repos/{owner}/{repo}/issues --jq '.[].title'

# use a template for the output
$ gh api repos/{owner}/{repo}/issues --template \
  '{{range .}}{{.title}} ({{.labels | pluck "name" | join ", " | color "yellow"}}){{"\n"}}{{end}}'

# list releases with GraphQL
$ gh api graphql -F owner='{owner}' -F name='{repo}' -f query='
  query($name: String!, $owner: String!) {
    repository(owner: $owner, name: $name) {
      releases(last: 3) {
        nodes { tagName }
      }
    }
  }
'

# list all repositories for a user
$ gh api graphql --paginate -f query='
  query($endCursor: String) {
    viewer {
      repositories(first: 100, after: $endCursor) {
        nodes { nameWithOwner }
        pageInfo {
          hasNextPage
          endCursor
        }
      }
    }
  }
'
{% endraw %}{% endhighlight %}

### See also

* [gh](./gh)
