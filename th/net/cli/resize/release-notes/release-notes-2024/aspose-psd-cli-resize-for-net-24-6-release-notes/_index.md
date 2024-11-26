---
title: Aspose.PSD CLI Resize for .NET 24.6 - บันทึกการอัปเดต
type: docs
weight: 90
url: /th/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการอัปเดตสำหรับ [Aspose.PSD CLI Resize for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Key**     | **รายละเอียด**                                                                                  | **หมวดหมู่** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | การอัปเดตแรกของ Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export และ Aspose.PSD.CLI.NLP.Editor |  ปรับปรุง |


## **ตัวอย่างการใช้งาน:**

**PSDNET-2110. การเปิดใช้งานแอปพลิเคชัน Aspose.PSD CLI Resize**


**การใช้งานผ่าน command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**การใช้งานจาก code:**

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
