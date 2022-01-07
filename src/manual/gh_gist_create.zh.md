---
layout: manual
permalink: /:path/:basename
---

## gh gist create

```
gh gist create [<filename>... | -] [flags]
```

创建具有给定内容的新GitHub gist。

GIST可以从一个或多个文件创建。或者，通过“-”作为文件名从标准输入读取。

默认情况下，GIST是保密的；使用“--public”将其公开列出。

### Options

<dl class="flags">
	<dt><code>-d</code>, <code>--desc &lt;string&gt;</code></dt>
	<dd>A description for this gist</dd>

```
<dt><code>-f</code>, <code>--filename &lt;string&gt;</code></dt>
<dd>Provide a filename to be used when reading from standard input</dd>

<dt><code>-p</code>, <code>--public</code></dt>
<dd>List the gist publicly (default: secret)</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>Open the web browser with created gist</dd>
```

</dl>

### Examples

{%highlight bash%}{%raw%}

# publish file 'hello.py' as a public gist

$gh—公共你好。派克

# create a gist with a description

$gh，你好。py-d“Python中的我的Hello World程序”

# create a gist containing several files

$gh，你好。疯狂的世界。太酷了。文本

# read from standard input to create a gist

$gh创建-

# create a gist from output piped from another command

$cat酷。txt |创建{%endraw%}{%endhighlight%}

### See also

-   [gh gist](./gh_gist)
