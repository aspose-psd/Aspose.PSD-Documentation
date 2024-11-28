---
title: راهنماهای انتشار Aspose.PSD CLI Convert برای .NET 24.4
type: docs
weight: 90
url: /fa/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت های انتشار برای [Aspose.PSD CLI Convert برای .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **کلید**     | **خلاصه**                                              | **دسته‌بندی** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | انتشار اولیه برنامه Aspose.PSD CLI Convert |  بهبود |


## **مثال‌های استفاده:**

**PSDNET-2023. انتشار اولیه برنامه Aspose.PSD CLI Convert**

**استفاده از خط فرمان:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**استفاده از کد دستوری:**

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
