---
title: Aspose.PSD CLI Convert cho .NET 24.4 - Ghi chú phát hành
type: docs
weight: 90
url: /vi/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD CLI Convert cho .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                              | **Danh mục** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Phiên bản ban đầu của Ứng dụng Chuyển đổi Aspose.PSD CLI |  Nâng cấp |


## **Ví dụ sử dụng:**

**PSDNET-2023. Phiên bản ban đầu của Ứng dụng Chuyển đổi Aspose.PSD CLI**

**Sử dụng từ dòng lệnh:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Sử dụng từ mã lệnh:**

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
