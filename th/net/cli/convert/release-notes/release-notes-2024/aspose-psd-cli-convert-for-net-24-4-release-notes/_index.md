---
title: บันทึกการอัปเดต Aspose.PSD CLI Convert for .NET 24.4
type: สารบัญ
weight: 90
url: /th/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD CLI Convert for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **คีย์**     | **สรุป**                                              | **หมวดหมู่** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | การเปิดตัวครั้งแรกของ Aspose.PSD CLI Convert Application |  การปรับปรุง |


## **ตัวอย่างการใช้:**

**PSDNET-2023. การเปิดตัวครั้งแรกของ Aspose.PSD CLI Convert Application**

**ใช้ผ่าน command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**ใช้ผ่านโค้ด command:**

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
