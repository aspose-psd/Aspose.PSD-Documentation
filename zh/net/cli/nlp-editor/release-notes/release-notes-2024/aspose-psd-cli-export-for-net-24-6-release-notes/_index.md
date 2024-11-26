---
title: Aspose.PSD CLI NLP 编辑器 for .NET 24.6 - 发布说明
type: docs
weight: 90
url: /zh/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

本页面包含 [Aspose.PSD CLI NLP 编辑器 for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/) 的发布说明。

{{% /alert %}}

| **关键字**  | **摘要**                                                                                       | **类别**     |
|:------------|:----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI 应用的初始版本: Aspose.PSD.CLI.Export 和 Aspose.PSD.CLI.NLP.编辑器              |  改进         |


## **使用示例：**

**PSDNET-2110. Aspose.PSD CLI NLP 编辑器应用的初始版本**

## **从命令行使用：**

{{% alert color="primary" %}}
首先安装此 dotnet 工具:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

我们建议在第一次使用之前运行以下命令:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
运行此命令后，您将能够使用短名称 nlp.cli 运行此应用程序，而不是 Aspose.PSD.CLI.NLP.编辑器。您可以指定自己的短名称。
{{% /alert %}}

**使用示例**

1. 此命令将转换当前文件夹中找到的第一个文件（可使用 aspose.psd 打开），并将其保存为带有透明度的 png 格式。此外，将设置许可证。您只需指定许可证一次。下一次运行时将从指定路径使用许可证。如果可用，此命令将显示 NLP 处理的详细日志。
{{< highlight bash >}}nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. 此命令将查找与"smth.psd"最相似名称的文件。然后将调整对比度并以最佳质量保存为 jpeg。输出文件名将被打印。将是 smth.jpg
{{< highlight bash >}}Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality{{< /highlight >}}

3. 此命令将在指定路径上查找文件，并将其大小减小为 25%。输出文件将被打印。它将保存在控制台当前文件夹中。
{{< highlight bash >}}Resize file C:\Users\someuser\Desktop\input.psd to 25%{{< /highlight >}}

4. 此命令将在 C:\Users\someuser\Desktop\ 中查找 input.psd 文件。然后将找到索引为 3 的图层，并将其调整为宽度 50px 和高度 100px。然后将此图层保存为 PDF 到 C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

 5. 此命令将在当前文件夹中打开 smth.psd，但所有效果将被禁用。然后将此文件转换为 BMP 格式，并保存为 output.bmp 在当前文件夹中。
 {{< highlight bash >}}Open smth.psd without effects and save it to output.bmp{{< /highlight >}}

**免责声明**

这是一个实验性应用程序。请尝试并留下反馈。任何反馈都将不胜感激。我们希望将 NO-Code 应用程序提升到新水平。易于整合到任何构建流程或业务流程是我们的目标。
