---
title: اسپوزه.ای.اس.دی. CLI تبدیل برای .نت 24.6 - یادداشت های انتشار
type: docs
weight: 90
url: /fa/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی یادداشت های انتشار برای [اسپوزه.ای.اس.دی. CLI تبدیل برای .نت 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/) می باشد.

{{% /alert %}}

| **کلید**     | **خلاصه**                                                                                 | **دسته‌بندی** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | انتشار اولیه اپ های اسپوزه.ای.اس.دی. CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor | ارتقاء |


## **مثال های استفاده:**

**PSDNET-2110. انتشار اولیه اپ های اسپوزه.ای.اس.دی. CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor**

**استفاده از خط فرمان:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**استفاده از کد خط:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.Convert.CommandLineOptions.ConversionOptions
{
    InputFiles = new List<string> { "photo_1.jpg", "photo_2.jpg", "photo_3.jpg", "photo_4.jpg", "photo_5.jpg", "photo_6.jpg" },
    OutputPath = "result.zip",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Apply(options);
{{< /highlight >}}
