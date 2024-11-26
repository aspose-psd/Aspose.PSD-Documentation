---
title: บันทึกการอัปเดต Aspose.PSD CLI Crop for .NET 24.6
type: docs
weight: 90
url: /th/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}
หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD CLI Crop for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)
{{% /alert %}}

| **Key**     | **สรุป**                                                                                   | **หมวดหมู่** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | การเผยแพร่ครั้งแรกของ Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export และ Aspose.PSD.CLI.NLP.Editor |  ความพัฒนา |

## **ตัวอย่างการใช้:**

**PSDNET-2110. การเผยแพร่ครั้งแรกของแอปพลิเคชัน Aspose.PSD CLI Crop**


**การใช้งานผ่าน command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input รูปภาพ1.jpg --output รูปที่ตัด.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**การใช้งานจากโค้ด command :**

{{< highlight csharp >}}
var options = ตัวเลือก Aspose.PSD.CLI.CommandLineOptions.CropOptions ใหม่
{
    InputPath = "รูปภาพ1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "รูปที่ตัด.png",
    OutputFormat = "png"
};


ถ้า (มีใบอนุญาตแล้ว)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}
