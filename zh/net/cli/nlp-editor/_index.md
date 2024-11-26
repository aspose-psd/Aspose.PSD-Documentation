---
title: Aspose.PSD CLI NLP Editor Application for .NET
type: docs
weight: 10
url: /zh/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Natural-Language-Processing PSD Console C# Library PSD API
description: 基于 Aspose.PSD 的 NLP 编辑器 CLI 应用程序，用于 PSD、PSB 和 AI 文件格式。 无代码 CI/CD 自动化。 支持通过自然语言处理编辑 PSD 文件。 只需用自然语言编写您的请求，即可执行各种操作，如转换、调整大小等。 无需安装 Adobe Photoshop 或 Adobe Illustrator，可在控制台中运行而无需额外代码。
---

**![Aspose.PSD for .NET 产品标识](home_1.png)**

**欢迎使用 Aspose.PSD NLP 编辑器 CLI 应用程序 .NET**

Aspose.PSD CLI NLP 编辑器应用程序是一个轻量级控制台实用程序，用于使用自然语言命令编辑 PSD 文件。 轻松集成到 CI/CD 管道中。

**免责声明**

这是一个实验性应用程序。 请尝试并留下反馈。 我们非常感谢任何反馈。 我们希望将无代码应用程序提升到一个新水平。 将其轻松集成到任何构建管道或业务流程中是我们的目标。

**Aspose.PSD NLP 编辑器 CLI 应用程序 .NET 的主要功能**

1. 使用自然语言命令在 PSD、PSB、AI 文件上执行操作。
2. 支持各种操作，如转换、调整大小等。
3. 无代码 CI/CD 自动化。
4. 支持使用自然语言编写请求以编辑 PSD 文件。

## **从命令行中使用：**

{{% alert color="primary" %}}
首先安装此 dotnet 工具：
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

我们建议在首次使用前运行以下命令：
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
运行此命令后，您可以使用缩写 nlp.cli 而不是 Aspose.PSD.CLI.NLP.Editor 来运行该应用程序。 您可以指定自己的缩写。
{{% /alert %}}

**Aspose.PSD.CLI.Crop 应用程序的可用参数**

| **参数** | **描述**                         |
|:-------------|:----------------------------------------|
| 任何文本     | 必需。您的自然语言命令，以更新 PSD 或 PSB 文件      |
| 许可证      | 许可证的路径。                    |
| 详细      | 显示特定命令的更多信息。 |
| 设置        | 在工具文件夹中创建批处理文件以便从控制台快速调用。 示例：--setup psd.nlp。然后您可以使用 psd.nlp 命令调用工具。 |

**使用示例**

1. 此命令将转换当前文件夹中第一个找到的文件（可使用 Aspose.PSD 打开）并以带透明度的 png 格式保存。 还将设置许可证。 您只需要在第一次指定许可证。 接下来的运行将使用指定路径的许可证。 如果有的话，此命令将显示 NLP 处理的详细日志。
{{< highlight bash >}}
  nlp.cli 将此文件夹中的文件转换为带有 alpha 的 png 格式 --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. 此命令将查找与“smth.psd”名称最相似的文件。 然后会调整对比度，并以最佳质量将其保存为 jpeg。 输出文件的名称将被打印。 将会是 smth.jpg
{{< highlight bash >}}
调整图层中名称为椭圆的第 10 到文件 smth.psd 的对比度，并保存为 output.jpg，具有最佳质量。
{{< /highlight >}}

3. 此命令将在指定路径上打开文件，并将其大小减小 25%。 输出文件的名称将被打印。它将保存在控制台当前文件夹中。
{{< highlight bash >}}
将文件 C:\Users\someuser\Desktop\input.psd 的大小缩小 25%
{{< /highlight >}}

4. 此命令将在 C:\Users\someuser\Desktop\ 中查找文件 input.psd。 然后将查找索引为 3 的图层，并将其调整为宽度 50px 和高度 100px。 然后将该图层保存为 PDF，保存在 C:\Users\someuser\Desktop\output.pdf 中。
{{< highlight bash >}}
将 C:\Users\someuser\Desktop\input.psd 的索引 3 的图层调整为宽度 50 和高度 100，并保存为 C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. 此命令将在当前文件夹中打开 smth.psd，但将禁用所有效果。 然后将该文件转换为 BMP 格式，并作为 output.bmp 保存在当前文件夹中。
 {{< highlight bash >}}
 在不使用效果的情况下打开 smth.psd，保存为 output.bmp
  {{< /highlight >}}

**如果需要在工作流程中为 PSD、PSB 和 AI 格式添加支持，请查看其他的 [Aspose.PSD CLI 应用程序](https://docs.aspose.com/psd/net/cli) .NET**

1. [Aspose.PSD CLI 转换](/psd/zh/net/cli/convert)
2. [Aspose.PSD CLI 剪裁](/psd/zh/net/cli/crop)
3. [Aspose.PSD CLI 调整大小](/psd/zh/net/cli/resize)
4. [Aspose.PSD CLI 导出](/psd/zh/net/cli/export)
5. [Aspose.PSD CLI NLP 编辑器](/psd/zh/net/cli/nlp-editor)

**请查看 Aspose.PSD for .NET 或 [其他平台]**

Aspose.PSD CLI 应用程序是常见操作的即用解决方案。 如果需要灵活的解决方案，请查看完整版本的 Aspose.PSD

1. [Aspose.PSD for .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD for Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD for Python 通过 .NET](https://releases.aspose.com/psd/python-net/)

## **Aspose.PSD for .NET 资源**

以下链接是您可能需要完成任务所需的一些有用资源。

- [Aspose.PSD CLI 应用程序 .NET 在线文档](/psd/zh/net/cli/conversion)
- [Aspose.PSD CLI 应用程序 .NET 发布说明](/psd/zh/net/cli/conversion/release-notes/)
- [Aspose.PSD CLI 应用程序 .NET 产品页面](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD for .NET API 参考指南](https://reference.aspose.com/net/psd)
- [在 GitHub 存储库中下载示例](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD for .NET 免费支持论坛](https://forum.aspose.com/c/psd)
- [Aspose.PSD for .NET 付费支持帮助台](https://helpdesk.aspose.com/)

