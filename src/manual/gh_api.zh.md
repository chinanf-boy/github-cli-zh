## gh api

```
gh api <endpoint> [flags]
```

向 GitHub API 发出经过身份验证的 HTTP 请求，并打印响应。

endpoint 参数应该是 GitHub API v3 endpoint 的路径，或者是访问 GitHub API v4 的`graphql`。

endpoint 参数中的占位符值`{owner}`、`{repo}`和`{branch}`将替换成当前目录存储库中的值。请注意，在某些 shell（例如 PowerShell）中，可能需要用`{…}`的值，放在引号中，以防止 shell 对花括号应用特殊含义。

默认的 HTTP 请求方法通常为`GET`，如果添加了任何参数，则为`POST`。用`--method`覆盖默认。

`-f/--raw-field`传递`key=value`格式的一个或多个，用于向请求负载，添加静态字符串参数。要添加非字符串或其他动态值，请参见`--field`。请注意，添加请求参数将自动将请求方法切换为 POST。要改 GET，请使用`--method GET`.

这个`-F/--field`标志具有基于值格式的魔法类型转换：

- 文本值`true`、`false`、`null`和整数，被转换为适当的 JSON 类型；
- 占位符值`{owner}`、`{repo}`和`{branch}`由当前目录存储库中的值填充；
- 如果该值以`@`开头，则该值的其余部分将被解释为，读取值的文件名。传递`-`则从标准输入读取。

对于 GraphQL 请求，除`query`和`operationName`之外的所有字段都被解释为 GraphQL 变量。

原始请求主体可以通过`--input`指定的文件，从外部传递。传递`-`则从标准输入读取。在此模式下，通过`--field`指定的参数。被序列化为 URL 查询参数。

在`--paginate`模式下，将按顺序请求所有结果页，直到没有更多结果页为止。对于 GraphQL 请求，这要求原始查询接受一个`$endCursor: String`变量，之后它从一个集合，获取`pageInfo{ hasNextPage, endCursor }`字段集。

### Options

<dl class="flags">
	<dt><code>--cache &lt;duration&gt;</code></dt>
	<dd>缓存一个响应, e.g. &#34;3600s&#34;, &#34;60m&#34;, &#34;1h&#34;</dd>

<dt><code>-F</code>, <code>--field &lt;key=value&gt;</code></dt>
<dd>添加一个类型参数，格式是 key=value</dd>

<dt><code>-H</code>, <code>--header &lt;key:value&gt;</code></dt>
<dd>添加一个 HTTP 请求头，格式是 key=value</dd>

<dt><code>--hostname &lt;string&gt;</code></dt>
<dd>请求的 GitHub 主址 (默认为 &#34;github.com&#34;)</dd>

<dt><code>-i</code>, <code>--include</code></dt>
<dd>将 HTTP 响应头也输出</dd>

<dt><code>--input &lt;file&gt;</code></dt>
<dd>file 作为 HTTP 请求的主体 (使用 &#34;-&#34; 可以从标准输入读取)</dd>

<dt><code>-q</code>, <code>--jq &lt;string&gt;</code></dt>
<dd>使用 jq 语法，查询响应的值</dd>

<dt><code>-X</code>, <code>--method &lt;string&gt;</code></dt>
<dd>HTTP 方法</dd>

<dt><code>--paginate</code></dt>
<dd>发出额外的 HTTP 请求，获取所有的结果页</dd>

<dt><code>-p</code>, <code>--preview &lt;strings&gt;</code></dt>
<dd> GitHub API 预览版本的功能</dd>

<dt><code>-f</code>, <code>--raw-field &lt;key=value&gt;</code></dt>
<dd>添加一个字符串参数，格式是 key=value</dd>

<dt><code>--silent</code></dt>
<dd>不打印</dd>

<dt><code>-t</code>, <code>--template &lt;string&gt;</code></dt>
<dd>用模板格式化响应</dd>

</dl>

### Examples

```bash
# 列出，repo 的 releases 
$ gh api repos/{owner}/{repo}/releases

# 发布一个 issue 评论
$ gh api repos/{owner}/{repo}/issues/123/comments -f body='Hi from CLI'

# 为 GET 请求，添加参数
$ gh api -X GET search/issues -f q='repo:cli/cli is:open remote'

# 自定义 HTTP header
$ gh api -H 'Accept: application/vnd.github.v3.raw+json' ...

# GitHub API 预览版本的功能
$ gh api --preview baptiste,nebula ...

# 打印 response 中特殊字段
$ gh api repos/{owner}/{repo}/issues --jq '.[].title'

# 模板化输出
$ gh api repos/{owner}/{repo}/issues --template \
  '{{range .}}{{.title}} ({{.labels | pluck "name" | join ", " | color "yellow"}}){{"\n"}}{{end}}'

# 列出，releases with GraphQL
$ gh api graphql -F owner='{owner}' -F name='{repo}' -f query='
  query($name: String!, $owner: String!) {
    repository(owner: $owner, name: $name) {
      releases(last: 3) {
        nodes { tagName }
      }
    }
  }
'

# 列出，一个用户所有的存储库
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
```

### See also

- [gh](./gh.zh.md)
