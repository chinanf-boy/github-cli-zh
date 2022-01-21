## gh repo sync

```
gh repo sync [<destination-repository>] [flags]
```

从源存储库同步目标存储库。同步使用源存储库的主分支更新目标存储库上的匹配分支，使它们相等。当`--force`如果指定了标志，则将使用硬重置同步两个分支。

如果没有参数，则选择本地存储库作为目标存储库。

默认情况下，源存储库是目标存储库的父存储库。可以使用`--source`旗帜

### Options

<dl class="flags">
	<dt><code>-b</code>, <code>--branch &lt;string&gt;</code></dt>
	<dd>Branch to sync (default: main branch)</dd>

```
<dt><code>--force</code></dt>
<dd>Hard reset the branch of the destination repository to match the source repository</dd>

<dt><code>-s</code>, <code>--source &lt;string&gt;</code></dt>
<dd>Source repository</dd>
```

</dl>

### Examples

```bash
# Sync local repository from remote parent
$ gh repo sync

# Sync local repository from remote parent on specific branch
$ gh repo sync --branch v1

# Sync remote fork from its parent
$ gh repo sync owner/cli-fork

# Sync remote repository from another remote repository
$ gh repo sync owner/repo --source owner2/repo2
```
### See also

-   [gh repo](./gh_repo.zh.md)
