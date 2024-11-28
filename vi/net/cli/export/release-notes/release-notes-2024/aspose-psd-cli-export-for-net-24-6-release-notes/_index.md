---
title: Ghi chú phát hành Aspose.PSD CLI Export cho .NET 24.6
type: docs
weight: 90
url: /vi/net/cli/xuat/aspose-psd-export-cli-app-cho-net-24-6-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa ghi chú phát hành cho [Aspose.PSD CLI Export cho .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                                 | **Danh mục** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Phiên bản Ban đầu của Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export và Aspose.PSD.CLI.NLP.Editor |  Cải tiến |


## **Ví dụ về cách sử dụng:**

**PSDNET-2110. Phiên bản Ban đầu của Ứng dụng Xuất Aspose.PSD CLI**

**Sử dụng từ dòng lệnh:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Sử dụng từ mã nguồn:**

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
