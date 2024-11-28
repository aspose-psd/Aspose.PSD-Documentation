---
title: دستور Release برای Aspose.PSD CLI Export برای .NET 24.6
type: مستندات
weight: 90
url: /fa/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی یادداشت‌های ورژن برای [Aspose.PSD CLI Export برای .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/) می‌باشد.

{{% /alert %}}

| **کلید**   | **خلاصه**                                                                                   | **دسته بندی** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | نسخه اولیه اپلیکیشن‌های Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor | افزایش ویژگی |


## **مثال‌های استفاده:**

**PSDNET-2110. اولین انتشار اپلیکیشن Aspose.PSD CLI Export**

**استفاده از خط فرمان:**

{{< highlight bash >}}

Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic

{{< /highlight >}}

**استفاده از کد:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "exported.png",
    OutputFormat = "png",
    LayerName = "Layer1"
};

if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Apply(options);

{{< /highlight >}}
