## gh repo sync

```
gh repo sync [<destination-repository>] [flags]
```

从源存储库**同步(sync)**到目标存储库。同步使用源存储库的 mian 分支，来更新目标存储库上的匹配分支，使它们相等。如果指定了`--force`标志，则强制同步两个分支。

如果没有参数，则选择本地存储库作为目标存储库。

默认情况下，源存储库是目标存储库的父存储库。可以使用`--source`更改

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>同步的分支 (default: main branch)</dd>

<dt><code>--force</code></dt>
<dd>强制同步</dd>

<dt><code>-s</code>, <code>--source &lt;string&gt;</code></dt>
<dd>源存储库</dd>

</dl>

### Examples

```bash
# 同步
$ gh repo sync

# v1 分支同步
$ gh repo sync --branch v1

# 同步 owner/cli-fork
$ gh repo sync owner/cli-fork

# owner2/repo2 的内容，同步进 owner/repo
$ gh repo sync owner/repo --source owner2/repo2
```

### See also

- [gh repo](./gh_repo.zh.md)
