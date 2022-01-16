# Triage role

当我们在GitHub CLI上打开更多问题和请求时，我们决定每周轮换一次。最初的期望是，本周担任该职位的人员每天在这项工作上的时间不超过2小时；我们可以根据需要改进它。

## Expectations for incoming issues

所有传入问题都需要**增强**, **缺陷**或**文件**标签

被认为是被分流的，**增强**问题至少需要以下一个附加标签：

-   **果心**：保留给核心CLI团队的工作
-   **需要帮助**：我们将接受捐款的工作
-   **需要设计**：需要用户体验设计师输入才能继续进行的工作
-   **需要调查**：需要核心团队解开谜团才能继续进行的工作
-   **需要用户输入**：需要记者提供更多信息才能继续进行的工作

被认为是被分流的，**缺陷**问题需要一个严重性标签：以下之一**p1**, **p2**或**p3**

如需了解更详细的**怎样**要对问题进行分类，请参阅*问题分类流程图*在下面

## Expectations for community pull requests

要被视为分流，传入的拉取请求应：

-   检查是否有相应的错误**需要帮助**问题
-   检查基本质量：构建是否通过？是否增加了测试？
-   检查冗余：是否已经有一个PR处理此问题？

一旦对PR进行了分类，应将其移动到**需要审查**项目委员会的专栏。

如需了解更详细的**怎样**要对问题进行分类，请参阅*PR分流流程图*在下面

## Issue triage flowchart

-   这个可以直接关闭吗？
    -   e、 g.垃圾邮件/垃圾
    -   闭嘴
-   我们不想这样做吗？
    -   e、 g.已经讨论过不想做或重复的问题
    -   点评结束
-   我们可以接受外部捐款吗？
    -   e、 g.这项任务相对简单，但我们团队中没有人有足够的带宽来承担这项任务
    -   确保线程包含新用户获取此消息所需的所有上下文
    -   添加`help wanted`标签
    -   考虑加入`good first issue`标签
-   我们想这样做吗？
    -   评论承认它
    -   添加`core`标签
    -   如果这是应该很快发布的内容，请添加到“项目待办事项”列
-   这很有趣，但需要讨论吗？
    -   标签`needs-design`如果需要设计输入，ping
    -   标签`needs-investigation`如果在采取行动之前需要进行工程研究
-   是否需要问题作者提供更多信息？
    -   向用户询问详细信息
    -   添加`needs-user-input`标签
-   这是一个使用/支持问题吗？
    -   提供一些说明/解决方法并关闭

## Pull request triage flowchart

-   可以直接关闭吗？
    -   e、 g.垃圾邮件/垃圾
    -   关
-   我们不想这样做吗？
    -   点评结束
-   这是否有趣，但需要讨论，并且没有参考问题？
    -   提出问题
    -   关
-   这是我们想要包括的东西吗？
    -   加上`needs review`柱

## Weekly PR audit

为了不让我们的公开公关名单失控（20+总公关*或*几个月前有多个PRs），每周尝试审核打开的PRs，目的是将其合并和/或关闭。处理每一次公关可能需要做太多的工作，但即使是接近完成一些也很有帮助。

对于每个PR，请询问：

-   这是否太陈旧（超过两个月还是冲突太多）？以评论结束
-   这真的很接近但作者缺席吗？推送提交完成，请求审阅
-   这是在等待分流吗？通过PR分类流程

## Useful aliases

本要点为第一响应者提供了一些有用的别名：

<https://gist.github.com/vilmibm/ee6ed8a783e4fef5b69b2ed42d743b1a>

## Examples

我们希望我们的项目是一个安全且令人鼓舞的开源环境。以下是一些如何以同理心回应或结束问题/PR的示例：

-   [Closing a quality PR its scope is too large](https://github.com/cli/cli/pull/1161)
-   [Closing a stale PR](https://github.com/cli/cli/pull/557#issuecomment-639077269)
-   [Closing a PR that doesn't follow our CONTRIBUTING policy](https://github.com/cli/cli/pull/864)
-   [Responding to a bug report](https://github.com/desktop/desktop/issues/9195#issuecomment-592243129)
-   [Closing an issue that out of scope](https://github.com/cli/cli/issues/777#issuecomment-612926229)
-   [Closing an issue with a feature request](https://github.com/desktop/desktop/issues/9722#issuecomment-625461766)
