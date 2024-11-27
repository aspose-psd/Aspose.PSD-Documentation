---
title: اطلاعات انتشار برش Aspose.PSD CLI برای .NET 24.4
type: docs
weight: 90
url: /fa/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل اطلاعات انتشار [Aspose.PSD CLI برش برای .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/) می‌باشد.

{{% /alert %}}

| **کلید**     | **خلاصه**                                        | **دسته بندی** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | انتشار اولیه برنامه Aspose.PSD CLI Crop |  بهبود |


## **مثال‌های استفاده:**

**PSDNET-2023. انتشار اولیه برنامه Aspose.PSD CLI Crop**

**استفاده از خط فرمان:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**استفاده از کد دستوری:**

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
