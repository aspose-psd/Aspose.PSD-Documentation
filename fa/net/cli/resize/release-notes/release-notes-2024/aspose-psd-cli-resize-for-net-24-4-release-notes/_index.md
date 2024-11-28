---
title: یادداشت‌های نسخه Aspose.PSD CLI Resize برای .NET 24.4
type: docs
weight: 90
url: /fa/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD CLI Resize برای .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) می‌باشد.

{{% /alert %}}

| **کلید**    | **خلاصه**                                              | **دسته‌بندی** |
|:------------|:--------------------------------------------------------|:--------------|
| PSDNET-2026 | انتشار اولیه برنامه Aspose.PSD CLI Resize             | بهبودات     |


## **مثال‌های استفاده:**

**PSDNET-2026. انتشار اولیه برنامه Aspose.PSD CLI Resize**

**استفاده از خط فرمان:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**استفاده از کد:**

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
