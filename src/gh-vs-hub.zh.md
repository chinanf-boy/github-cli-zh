# GitHub CLI & `hub`

[GitHub CLI](https://cli.github.com/) (`gh`)是[announced in early 2020](https://github.blog/2020-02-12-supercharge-your-command-line-experience-github-cli-is-now-in-beta/)并提供了从命令行与GitHub存储库进行交互的更无缝的方式。我们还知道，许多人对非常相似的问题感兴趣[`hub`](https://hub.github.com/)项目，所以我们想澄清一些潜在的混淆点。

## Why didn’t you just build `gh` on top of `hub`?

我们竭力决定是否继续在现有基础上再接再厉`hub`并将其作为正式的GitHub项目采用。在权衡不同的可能性时，我们决定重新开始，不受10年来设计决策的限制，因为`hub`在没有假设的情况下`hub`可以安全地别名为`git`。我们还希望更加固执己见，专注于GitHub工作流，并通过`hub`有疏远许多人的危险`hub`喜欢现有工具并希望它以他们习惯的方式工作的用户。

## What’s next for `hub`?

GitHub CLI团队专注于构建新工具，`gh`.我们不会关机`hub`或者做任何事情来改变它。这是一个开源项目，只要它得到维护并不断收到捐款，它就会继续存在。

## What does it mean that GitHub CLI is official and `hub` is unofficial?

GitHub CLI由一组代表GitHub使用该工具的人员构建和维护。当it出现问题时，人们可以联系GitHub支持部门或在问题跟踪器中创建问题，GitHub的员工将在那里做出响应。

`hub`是一个项目，其维护者恰好也是GitHub的员工。他选择保持`hub`在他的业余时间，就像我们的许多员工做开源项目一样。

## Should I use `gh` or `hub`?

我们无意强迫任何人使用GitHub CLI而不是`hub`.我们认为人们应该使用任何一套工具，让他们在使用GitHub时感到最快乐和最高效。

如果您打算使用一个工具作为Git本身的包装器，`hub`这可能是一个更好的选择`gh`.

如果您想要一个更加固执己见的工具，并希望从命令行帮助简化GitHub工作流，我们希望您使用`gh`.从那时起`gh`由GitHub的一个团队维护，我们打算响应人们的关注和需求，并根据人们随着时间的推移如何使用它来改进该工具。

GitHub CLI并不打算完全取代`hub`而且可能永远不会，但我们希望使用CLI的绝大多数GitHub用户将在使用中发现越来越多的价值`gh`随着我们的不断改进。
