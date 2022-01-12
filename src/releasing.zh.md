# Releasing

我们的构建系统自动编译跨平台二进制文件并将其附加到任何名为`vX.Y.Z`。更改日志是[generated from git commit log](https://docs.github.com/en/repositories/releasing-projects-on-github/automatically-generated-release-notes).

运行的正式版本的用户`gh`在他们的机器上，将在24小时内收到有关新版本的通知。

要测试生成系统，请发布一个名为`vX.Y.Z-pre.0`或`vX.Y.Z-rc.1`。请注意，这样的版本仍然是公开的，但它将被标记为“预发布”，这意味着它永远不会显示为“最新”版本，也不会触发用户的升级通知。

## General guidelines

-   要发布的功能应在发布前至少一天进行审查和批准。
-   功能发布应该增加次要版本号。

## Tagging a new release

1.  `git tag v1.2.3 && git push origin v1.2.3`
2.  等待几分钟以运行生成：<https://github.com/cli/cli/actions>
3.  验证是否显示了版本并具有正确的资源：<https://github.com/cli/cli/releases>
4.  扫描生成的发行说明，并通过在主题部分下对项目进行分组，选择性地添加人性化体验
5.  验证营销网站是否已更新：<https://cli.github.com>
6.  （可选）删除与此版本相关的任何预发布

成功构建将导致跨多个存储库进行更改：

-   <https://github.com/github/cli.github.com>
-   <https://github.com/Homebrew/homebrew-core/pulls>
-   <https://github.com/cli/scoop-gh>

如果构建失败，没有一种干净的方法可以重新运行它。最简单的方法是重新开始，删除GitHub上的部分发行版并重新发布标记。请注意，这可能会中断已收到升级通知的用户或工具。如果功能发布及其二进制文件已经存在，那么最好尝试手动修复失败的特定工作流任务。根据故障类型做出最佳判断。

## Release locally for debugging

可以创建本地版本进行测试，而无需在发布页面上创建任何官方内容。

1.  确保安装了GoReleaser：`brew install goreleaser`
2.  `goreleaser --skip-validate --skip-publish --rm-dist`
3.  在下面找到构建的产品`dist/`.
