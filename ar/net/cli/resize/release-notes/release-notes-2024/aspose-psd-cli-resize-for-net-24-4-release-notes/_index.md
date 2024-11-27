---
title: تعليمات الإصدار Aspose.PSD CLI لإعادة تحجيم لـ .NET 24.4
type: docs
weight: 90
url: /ar/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على تعليمات الإصدار لـ [Aspose.PSD CLI إعادة التحجيم لـ .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}


| **المفتاح**    | **الملخص**                                   | **الفئة**       |
|:------------|:-----------------------------------------------|:-------------|
| PSDNET-2026 | الإصدار الأولي لتطبيق Aspose.PSD CLI Resize |  تعزيز |


## **أمثلة الاستخدام:**

**PSDNET-2026. الإصدار الأولي لتطبيق Aspose.PSD CLI Resize**

**الاستخدام من سطر الأوامر:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**الاستخدام من الكود:**

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