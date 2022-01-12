## gh extension install

```
gh extension install <repository>
```

在本地安装GitHub存储库作为GitHub CLI扩展。

存储库参数可以以“owner/repo”格式以及完整URL指定。当存储库未托管在github上时，URL格式非常有用。通用域名格式。

要从当前目录安装正在开发中的扩展，请使用“”作为存储库参数的值。

请参阅上的可用扩展名列表<https://github.com/topics/gh-extension>

### Examples

{%highlight bash%}{%raw%}$gh扩展安装所有者/gh扩展$gh扩展安装<https://git.example.com/owner/gh-extension>$gh扩展安装。{%endraw%}{%endhighlight%}

### See also

-   [gh extension](./gh_extension)
