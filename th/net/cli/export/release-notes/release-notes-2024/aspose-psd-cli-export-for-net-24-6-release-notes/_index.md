---
title: Aspose.PSD CLI สำหรับ .NET 24.6 - บันทึกการปล่อย
type: docs
weight: 90
url: /th/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการปล่อยสำหรับ [Aspose.PSD CLI สำหรับ .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                                 | **หมวดหมู่** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | การปล่อยเวอร์ชันแรกของ Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export และ Aspose.PSD.CLI.NLP.Editor |  การปรับปรุง |

## **ตัวอย่างการใช้:**

**PSDNET-2110. การปล่อยเวอร์ชันแรกของแอปพลิเคชัน Aspose.PSD CLI Export**

**การใช้จาก command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**การใช้จากโค้ด:**

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
