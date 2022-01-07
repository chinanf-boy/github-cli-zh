---
layout: manual
permalink: /:path/:basename
---

## gh gist clone

```
gh gist clone <gist> [<directory>] [-- <gitflags>...]
```

本地克隆GitHub gist。

要点可以以下格式之一作为参数提供：

-   按ID，例如5b0e0062eb8e9654adad7bb1d81cc75f
-   通过URL，例如。“<https://gist.github.com/OWNER/5b0e0062eb8e9654adad7bb1d81cc75f>"

通过在“--”之后列出其他“git clone”标志来传递这些标志。

### See also

-   [gh gist](./gh_gist)
