---
title: 如何运行示例
type: docs
weight: 90
url: /zh/net/how-to-run-the-examples/
description: 学习如何运行关于托管在 GitHub 上的 PSD 文件格式库示例。
---

## **软件需求**
请确保在下载和运行示例之前满足以下要求。

1. Visual Studio 2010 或更高版本
1. 在 Visual Studio 中安装 NuGet 包管理器。确保在 Visual Studio 中安装了最新的 NuGet API 版本。有关如何安装 NuGet 包管理器的详细信息，请查看[这里](http://docs.nuget.org/ndocs/guides/install-nuget)。
1. 转到工具-> 选项-> NuGet 包管理器-> 包源，并确保选中 **nuget.org** 选项
1. 示例项目使用 NuGet 自动包恢复功能，因此您应该具有有效的互联网连接。如果在要执行示例的计算机上没有有效的互联网连接，请查看[安装](/psd/zh/net/installation/)来在示例项目中添加对 Aspose.Imaging.dll 的引用。

## **从 GitHub 下载**
所有 Aspose.PSD for .NET 的示例都托管在[GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET)上。

- 您可以使用您喜欢的 GitHub 客户端克隆存储库，也可以从[这里](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip)下载 ZIP 文件。
- 将 ZIP 文件内容提取到计算机上的任何文件夹中。所有示例位于 **Examples** 文件夹中。
- 这里有一个用于 C# 的 Visual Studio 解决方案文件。
- 这些项目是在 Visual Studio 2013 中创建的，但解决方案文件与 Visual Studio 2010 SP1 及更高版本兼容。
- 在 Visual Studio 中打开解决方案文件并构建项目。
- 首次运行时，依赖项将通过 NuGet 自动下载。
- **Examples** 根文件夹中的 **Data** 文件夹包含 C# 示例使用的输入文件。务必将 **Data** 文件夹与示例项目一起下载。
- 打开 RunExamples.cs 文件，在这里调用所有示例。
- 从项目内取消注释您想要运行的示例。

如有任何设置或运行示例时遇到任何问题，请随时使用我们的论坛联系我们。

## **贡献**
如果您希望添加或改进示例，我们鼓励您为该项目做出贡献。此存储库中的所有示例和展示项目均为开源项目，可以自由在您自己的应用程序中使用。

要做出贡献，您可以 fork 该存储库，编辑源代码并创建拉取请求。我们将审查更改并在发现有帮助时将其包含在存储库中。
