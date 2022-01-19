## gh extension install

```
gh extension install <repository>
```

在本地安装 GitHub 存储库，作为 GitHub CLI 扩展。

存储库参数以`owner/repo`格式以及完整 URL 指定。当存储库未托管在 github 上时，URL 格式非常有用。

要从**当前目录**，安装正在开发中的扩展，请使用`.`作为存储库参数的值。

请参阅上的可用扩展名列表<https://github.com/topics/gh-extension>

### Examples

```bash
$ gh extension install owner/gh-extension
$ gh extension install https://git.example.com/owner/gh-extension
$ gh extension install .
```

### See also

- [gh extension](./gh_extension.zh.md)
