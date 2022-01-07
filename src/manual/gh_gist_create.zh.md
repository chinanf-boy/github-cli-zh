## gh gist create

```
gh gist create [<filename>... | -] [flags]
```

创建具有给定内容的新 GitHub gist。

GIST 可以从一个或多个文件创建。或者，传递`-`作为文件名，从标准输入读取。

默认情况下，GIST 是保密的；使用`--public`将其公开列出。

### Options

<dl class="flags">
	<dt><code>-d</code>, <code>--desc &lt;string&gt;</code></dt>
	<dd>描述</dd>

<dt><code>-f</code>, <code>--filename &lt;string&gt;</code></dt>
<dd>标准输入，给个文件名</dd>

<dt><code>-p</code>, <code>--public</code></dt>
<dd>公开 (default: secret)</dd>

<dt><code>-w</code>, <code>--web</code></dt>
<dd>gist 链接，打开浏览器</dd>

</dl>

### Examples

```bash
# 上传 'hello.py' 作为公开的 gist
$ gh gist create --public hello.py

# 带描述
$ gh gist create hello.py -d "my Hello-World program in Python"

# 带多个文件
$ gh gist create hello.py world.py cool.txt

# 要标准输入
$ gh gist create -

# 管道输入
$ cat cool.txt | gh gist create
```

### See also

- [gh gist](./gh_gist.zh.md)
