---
title: Aspose.PSD CLI Resize cho .NET 24.4 - Ghi chú phát hành
type: docs
weight: 90
url: /vi/net/cli/resize/release-notes/aspose-psd-cli-resize-cho-net-24-4-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD CLI Resize cho .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                          | **Danh mục** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Phát hành ban đầu của Ứng dụng Resize Aspose.PSD CLI | Cải tiến |


## **Ví dụ sử dụng:**

**PSDNET-2026. Phát hành ban đầu của Ứng dụng Resize Aspose.PSD CLI**

**Sử dụng từ dòng lệnh:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Sử dụng từ code:**

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
