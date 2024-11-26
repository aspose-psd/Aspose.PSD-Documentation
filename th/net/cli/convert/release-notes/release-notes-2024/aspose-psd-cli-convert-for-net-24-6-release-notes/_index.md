---
title: Aspose.PSD CLI Convert for .NET 24.6 - บันทึกการอัปเดต
type: docs
weight: 90
url: /th/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD CLI Convert for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                                   | **หมวดหมู่** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | การเปิดตัวครั้งแรกของ Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export และ Aspose.PSD.CLI.NLP.Editor |  พัฒนา |


## **ตัวอย่างการใช้งาน:**

**PSDNET-2110. การเปิดตัวครั้งแรกของ Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export และ Aspose.PSD.CLI.NLP.Editor**

**การใช้งานจาก command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**การใช้งานจากโค้ด command:**

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
