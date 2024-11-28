---
title: یادداشت‌های نسخه Aspose.PSD CLI Crop برای .NET 24.6
type: docs
weight: 90
url: /fa/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD CLI Crop for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **کلید**    | **خلاصه**                                                                   | **دسته‌بندی** |
|:------------|:-----------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | انتشار اولیه برنامه‌های Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor |  بهبود  |


## **مثال‌های استفاده:**

**PSDNET-2110. انتشار اولیه برنامه Aspose.PSD CLI Crop**

**استفاده از خط فرمان:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --ورودی photo1.jpg --خروجی cropped_photo.png --فرمت png --چپ 10 --بالا 35 --عرض 250 --ارتفاع 300 --cropType مستطیل --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**استفاده از کد خط:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}
