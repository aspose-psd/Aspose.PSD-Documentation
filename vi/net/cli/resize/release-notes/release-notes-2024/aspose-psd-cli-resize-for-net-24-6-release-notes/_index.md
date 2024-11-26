---
title: Aspose.PSD CLI Resize cho .NET 24.6 - Ghi chú phát hành
type: docs
weight: 90
url: /vi/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD CLI Resize cho .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Khóa**    | **Tóm tắt**                                                                                    | **Danh mục** |
|:------------|:----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Phiên bản Ban đầu của Ứng dụng Aspose.PSD CLI: Aspose.PSD.CLI.Xuất và Aspose.PSD.CLI.NLP.Chỉnh sửa | Cải tiến    |


## **Ví dụ về cách sử dụng:**

**PSDNET-2110. Ban đầu phát hành Ứng dụng Aspose.PSD CLI Resize**

**Sử dụng từ dòng lệnh:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Sử dụng từ mã nguồn:**

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
