---
title: دستاوردهای انتشار نسخه Aspose.PSD CLI Resize برای .NET 24.6
type: مستندات
weight: 90
url: /fa/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی دستاوردهای انتشاری برای [Aspose.PSD CLI Resize برای .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) می‌باشد.

{{% /alert %}}

| **کلید**    | **خلاصه**                                                                                  | **دسته‌بندی** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | انتشار اولیه برنامه‌های Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor | ارتقاء |


## **نمونه‌های استفاده:**

**PSDNET-2110. انتشار اولیه برنامه Aspose.PSD CLI Resize**

**استفاده از خط فرمان:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**استفاده از کد:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(options);

{{< /highlight >}}
