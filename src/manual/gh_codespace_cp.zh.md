## gh codespace cp

```
gh codespace cp [-e] [-r] <sources>... <dest>
```

cp 命令在本地和远程文件系统之间，复制文件。

与 UNIX 一样的`cp`命令，第一个参数指定，**源**，最后一个参数指定，**目标**；如果目标是目录，则可以在第一个参数之后，指定其他源。

这个`--recursive`，如果任何源是目录，则需要标记。

任何文件名参数上的`remote:`前缀，表示它引用远程（代码空间）计算机的文件系统。它相对于远程用户的主目录进行解析。

默认情况下，远程文件名按字面解释。若是写有`--expand`标志，则每个此类参数均按`scp`方式处理：作为要在远程计算机上计算的 Bash 表达式，需要对 tildes、大括号、glob、环境变量和 backticks 进行扩展。（译者：看例子）

为了安全起见，不要对不受信任的用户，提供这个标志；具体看见 <https://lwn.net/Articles/835962/> ，讨论讨论。

### Options

<dl class="flags">
	<dt><code>-c</code>, <code>--codespace &lt;string&gt;</code></dt>
	<dd>名字</dd>

<dt><code>-e</code>, <code>--expand</code></dt>
<dd>在远程 shell上，展开远程的（多个）文件名</dd>

<dt><code>-r</code>, <code>--recursive</code></dt>
<dd>递归复制目录</dd>

</dl>

### Examples

```bash
$ gh codespace cp -e README.md 'remote:/workspaces/$RepositoryName/'
$ gh codespace cp -e 'remote:~/\*.go' ./gofiles/
$ gh codespace cp -e 'remote:/workspaces/myproj/go.{mod,sum}' ./gofiles/
```

### See also

- [gh codespace](./gh_codespace.zh.md)
