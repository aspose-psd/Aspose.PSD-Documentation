---
title: Aspose.PSD CLI Cắt cho .NET 24.6 - Ghi chú về Bản phát hành
type: docs
weight: 90
url: /vi/psd/net/cli/cut/aspose-psd-cut-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú về bản phát hành cho [Aspose.PSD CLI Cắt cho .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Cut/)

{{% /alert %}}

| **Khóa**   | **Tóm tắt**                                                                                  | **Danh mục**  |
|:-----------|:---------------------------------------------------------------------------------------------|:--------------|
| PSDNET-2110| Bản phát hành ban đầu của Ứng dụng Aspose.PSD CLI: Aspose.PSD.CLI.Export và Aspose.PSD.CLI.NLP.Editor | Cải tiến     |


## **Ví dụ về cách sử dụng:**

**PSDNET-2110. Bản phát hành ban đầu của Ứng dụng Cắt Aspose.PSD CLI**

**Sử dụng từ dòng lệnh:**

{{< highlight bash >}}
Aspose.PSD.CLI.Cut --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Sử dụng từ mã code:**

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
