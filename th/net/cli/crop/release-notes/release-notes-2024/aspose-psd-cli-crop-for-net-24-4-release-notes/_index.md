---
title: บันทึกการออกอากาศ Aspose.PSD CLI Crop for .NET 24.4
type: docs
weight: 90
url: /th/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการออกอากาศสำหรับ [Aspose.PSD CLI Crop for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Key**     | **สรุป**                                        | **หมวดหมู่** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | การเปิดตัว Aspose.PSD CLI Crop Application  |  ปรับปรุง |


## **ตัวอย่างการใช้:**


**PSDNET-2023. การเปิดตัว Aspose.PSD CLI Crop Application**

**การใช้จาก command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}


**การใช้จากโค้ด command:**

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
