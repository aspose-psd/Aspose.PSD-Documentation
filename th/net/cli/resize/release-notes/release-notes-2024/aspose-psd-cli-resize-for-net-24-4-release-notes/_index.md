---
title: Aspose.PSD CLI Resize for .NET 24.4 - บันทึกการอัปเดต
type: docs
weight: 90
url: /th/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}
หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD CLI Resize for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)
{{% /alert %}}

| **คีย์**     | **สรุป**                                          | **หมวดหมู่** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | การเปิดตัว Aspose.PSD CLI Resize Application |  การปรับปรุง |


## **ตัวอย่างการใช้:**


**PSDNET-2026. การเปิดตัว Aspose.PSD CLI Resize Application**

**การใช้จาก command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**การใช้จาก code:**

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
