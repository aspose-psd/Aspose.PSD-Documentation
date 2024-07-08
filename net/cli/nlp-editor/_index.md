---
title: Aspose.PSD CLI NLP Editor Application for .NET
type: docs
weight: 10
url: /net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Natural-Language-Processing PSD Console C# Library PSD API
description: Aspose.PSD-based NLP Editor CLI application for PSD, PSB, and AI File Formats. No-code CI/CD Automation. Supports natural language processing for editing PSD files. Just write your request in natural language to perform various operations like conversion, adjustment, resizing, and more. It does not require Adobe Photoshop or Adobe Illustrator to be installed and can be run from the console without additional code.
---

**![Aspose.PSD for .NET Product Logo](home_1.png)**

**Welcome to Aspose.PSD NLP Editor CLI Application for .NET**

Aspose.PSD CLI NLP Editor Application is a lightweight console utility for editing PSD files using natural language commands. Easy integration into CI/CD Pipelines.

**Disclaimer**

This is an experimental application. Please try it and leave feedback. Any feedback is highly appreciated. We want to take NO-Code application to the next level. Easy integration to any build pipeline or business process is our goal.

**Main functionality of Aspose.PSD NLP Editor CLI Application for .NET**

1. Perform operations on PSD, PSB, AI files using natural language commands.
2. Supports various operations like conversion, adjustment, resizing, and more.
3. No-code CI/CD automation.
4. Supports writing requests in natural language for editing PSD files.

{{% alert color="primary" %}}
We recommend before first use run the following command:
{{< highlight bash >}}
Aspose.PSD.CLI.NLP.Editor --setup nlp.cli
{{< /highlight >}}
After this command you will be able to run this application with short name nlp.cli instead pf Aspose.PSD.CLI.NLP.Editor. You can specify your own short name.
{{% /alert %}}

**Available parameters for Aspose.PSD.CLI.Crop Application**

| **Argument** | **Description**                         |
|:-------------|:----------------------------------------|
| any text     | Required. You command in natural language to update PSD or PSB File      |
| license      | Path to the license.                    |
| verbose      | Display more information on a specific command. |
| setup        | Creates bat file in tools folder for quick call from console. Example: --setup psd.nlp. Then you can call tool with psd.nlp command |

**Examples of usage**

1. This command will convert first found file (That can be opened with aspose.psd) from current folder and will save it png format with transparency. Also, the license will be set up. You need to specify license only once. The next runs the license will be used from the specified path. This command will show the verbose log of NLP processing if it's available. 
{{< highlight bash >}}
  nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. This command find the file with most similar name to "smth.psd". Then it will adjust contrast and will save it to jpeg wiith the best quality. Name of output file will printed. It will be smth.jpg
{{< highlight bash >}}
Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality
{{< /highlight >}}

3. This command will wind file on the specified path, and will reduce its size to 25%. Output file will printed. It will be saved in the current folder of console.
{{< highlight bash >}}
Resize file C:\Users\someuser\Desktop\input.psd to 25%
{{< /highlight >}}

4. This command will find file input.psd in  C:\Users\someuser\Desktop\. Then it will find layer with index 3 and will resize it to width 50px and height 100px. Then this layer will be saved as PDF in C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
 Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. This command will open smth.psd in current folderm but all effects will be disabled. And then this file will be converted to BMP format and as output.bmp in the current folder.
 {{< highlight bash >}}
 Open smth.psd without effects and save it to output.bmp
  {{< /highlight >}}

**Please check other [Aspose.PSD CLI Applications](https://docs.aspose.com/psd/net/cli) for .NET if you need to add support for PSD, PSB, and AI Formats to your workflow**

1. [Aspose.PSD CLI Convert](/psd/net/cli/convert)
2. [Aspose.PSD CLI Crop](/psd/net/cli/crop)
3. [Aspose.PSD CLI Resize](/psd/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/net/cli/nlp-editor)

**Please check Aspose.PSD for .NET or [other platforms]**

Aspose.PSD CLI Applications is a ready-to-use solution for popular operations. If you need a flexible solution, please check the full version of Aspose.PSD

1. [Aspose.PSD for .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD for Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD for Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Aspose.PSD for .NET Resources**

Following are the links to some useful resources you may need to accomplish your tasks.

- [Aspose.PSD CLI Applications for .NET Online Documentation](/psd/net/cli/conversion)
- [Aspose.PSD for CLI Applications for .NET Release Notes](/psd/net/cli/conversion/release-notes/)
- [Aspose.PSD for CLI Applications .NET Product Page](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD for .NET API Reference Guide](https://reference.aspose.com/net/psd)
- [Download Examples at GitHub Repository](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD for .NET Free Support Forum](https://forum.aspose.com/c/psd)
- [Aspose.PSD for .NET Paid Support Helpdesk](https://helpdesk.aspose.com/)
