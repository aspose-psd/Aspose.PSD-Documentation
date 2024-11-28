---
title: Aspose.PSD CLI NLP Editor for .NET 24.6 - Release Notes
type: docs
weight: 90
url: /net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD CLI NLP Editor for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Key**     | **Summary**                                                                                 | **Category** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Initial Release of Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export and Aspose.PSD.CLI.NLP.Editor |  Enhancement |


## **Usage examples:**

**PSDNET-2110. Initial release of Aspose.PSD CLI NLP Editor Application**

## **Usage from command line:**

{{% alert color="primary" %}}
Firstly install this dotnet tool:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

We recommend before first use run the following command:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
After this command you will be able to run this application with short name nlp.cli instead pf Aspose.PSD.CLI.NLP.Editor. You can specify your own short name.
{{% /alert %}}

**Examples of usage**

1. This command will convert first found file (That can be opened with aspose.psd) from current folder and will save it png format with transparency. Also, the license will be set up. You need to specify license only once. The next runs the license will be used from the specified path. This command will show the verbose log of NLP processing if it's available. 
{{< highlight bash >}}nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. This command find the file with most similar name to "smth.psd". Then it will adjust contrast and will save it to jpeg wiith the best quality. Name of output file will printed. It will be smth.jpg 
{{< highlight bash >}}Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality{{< /highlight >}}

3. This command will wind file on the specified path, and will reduce its size to 25%. Output file will printed. It will be saved in the current folder of console.
{{< highlight bash >}}Resize file C:\Users\someuser\Desktop\input.psd to 25%{{< /highlight >}}

4. This command will find file input.psd in  C:\Users\someuser\Desktop\. Then it will find layer with index 3 and will resize it to width 50px and height 100px. Then this layer will be saved as PDF in C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

 5. This command will open smth.psd in current folderm but all effects will be disabled. And then this file will be converted to BMP format and as output.bmp in the current folder.
 {{< highlight bash >}}Open smth.psd without effects and save it to output.bmp{{< /highlight >}}

**Disclaimer**

This is an experimental application. Please try it and leave feedback. Any feedback is highly appreciated. We want to take NO-Code application to the next level. Easy integration to any build pipeline or business process is our goal.
