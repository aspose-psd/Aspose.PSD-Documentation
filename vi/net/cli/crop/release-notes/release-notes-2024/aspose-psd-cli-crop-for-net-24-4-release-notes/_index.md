---
title: Aspose.PSD CLI Cắt cho .NET 24.4 - Thông tin Phát hành
type: docs
weight: 90
url: /vi/net/cli/cut/aspose-psd-cli-cut-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa thông tin phát hành cho [Aspose.PSD CLI Cắt cho .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Cut/)

{{% /alert %}}

| **Key**     | **Tóm tắt**                                        | **Thể loại** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Bản phát hành ban đầu của Ứng dụng Cắt Aspose.PSD CLI | Cải Tiến |


## **Ví dụ sử dụng:**

**PSDNET-2023. Bản phát hành ban đầu của Ứng dụng Cắt Aspose.PSD CLI**

**Sử dụng từ dòng lệnh:**

{{< highlight bash >}}
Aspose.PSD.CLI.Cut --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Sử dụng từ mã lệnh:**

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

Aspose.PSD.CLI.Cut.Apply(options);
{{< /highlight >}}
