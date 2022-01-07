---
layout: manual
permalink: /:path/:basename
---

## gh api

```
gh api <endpoint> [flags]
```

向GitHub API发出经过身份验证的HTTP请求并打印响应。

endpoint参数应该是GitHub API v3端点的路径，或者是访问GitHub API v4的“graphql”。

端点参数中的占位符值“{owner}”、“{repo}”和“{branch}”将替换为当前目录存储库中的值。请注意，在某些shell（例如PowerShell）中，可能需要包含任何包含“{…}”的值在引号中，以防止壳对花括号应用特殊含义。

默认的HTTP请求方法通常为“GET”，如果添加了任何参数，则为“POST”。用`--method`.

通过一个或多个`-f/--raw-field`“key=value”格式的值，用于向请求负载添加静态字符串参数。要添加非字符串或其他动态值，请参见`--field`在下面请注意，添加请求参数将自动将请求方法切换为POST。要改为将参数作为GET查询字符串发送，请使用`--method GET`.

这个`-F/--field`标志具有基于值格式的魔法类型转换：

-   文本值“true”、“false”、“null”和整数被转换为适当的JSON类型；
-   占位符值“{owner}”、“{repo}”和“{branch}”由当前目录存储库中的值填充；
-   如果该值以“@”开头，则该值的其余部分将被解释为从中读取该值的文件名。通过“-”读取标准输入。

对于GraphQL请求，除“query”和“operationName”之外的所有字段都被解释为GraphQL变量。

原始请求主体可以通过指定的文件从外部传递`--input`.通过“-”读取标准输入。在此模式下，通过以下方式指定参数：`--field`标志被序列化为URL查询参数。

在里面`--paginate`模式下，将按顺序请求所有结果页，直到没有更多结果页为止。对于GraphQL请求，这要求原始查询接受`$endCursor: String`变量，它获取`pageInfo{ hasNextPage, endCursor }`集合中的字段集。

### Options

<dl class="flags">
	<dt><code>--cache &lt;duration&gt;</code></dt>
	<dd>Cache the response, e.g. &#34;3600s&#34;, &#34;60m&#34;, &#34;1h&#34;</dd>

```
<dt><code>-F</code>, <code>--field &lt;key=value&gt;</code></dt>
<dd>Add a typed parameter in key=value format</dd>

<dt><code>-H</code>, <code>--header &lt;key:value&gt;</code></dt>
<dd>Add a HTTP request header in key:value format</dd>

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
<dd>Add a string parameter in key=value format</dd>

<dt><code>--silent</code></dt>
<dd>Do not print the response body</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>Format the response using a Go template</dd>
```

</dl>

### Examples

{%highlight bash%}{%raw%}

# list releases in the current repository

$gh api repos/{owner}/{repo}/releases

# post an issue comment

$gh api repos/{owner}/{repo}/issues/123/comments-f body='Hi from CLI'

# add parameters to a GET request

$gh api-X获取搜索/问题-f q='repo:cli/cli is:open remote'

# set a custom HTTP header

$gh api-H'接受：应用程序/vnd。github。v3。原始+json'。。。

# opt into GitHub API previews

$gh api——预览巴蒂斯特星云。。。

# print only specific fields from the response

$gh api repos/{owner}/{repo}/issues--jq'。\[].标题'

# use a template for the output

$gh api repos/{owner}/{repo}/issues--template\\'{{range.}{{.title}}（{.labels{.labels | pulk“name”| join“，| color“yellow”}}}）{{{\\n}}{{{end}'

# list releases with GraphQL

$gh api graphql-F owner='{owner}'-F name='{repo}'-F query='query（$name:String！，$owner:String！）{repository（owner:$owner，name:$name）{releases（last:3）{nodes{tagName}}}'

# list all repositories for a user

$gh api graphql--paginate-f query='query（$endCursor:String）{viewer{repositories（first:100，after:$endCursor）{nodes{nameWithOwner}pageInfo{hasNextPage endCursor}}}}{%endraw%}{%endhighlight

### See also

-   [gh](./gh)
