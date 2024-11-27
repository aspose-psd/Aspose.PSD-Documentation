---
title: ملحق Aspose.PSD CLI لتغيير الحجم لـ .NET 24.6 - ملاحظات الإصدار
type: docs
weight: 90
url: /ar/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD CLI لتغيير الحجم لـ .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Key**     | **Summary**                                                                                 | **Category** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | الإصدار الأولي لتطبيقات Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor |  تحسين |


## **أمثلة الاستخدام:**

**PSDNET-2110. الإصدار الأولي لتطبيق تغيير الحجم لـ Aspose.PSD CLI**

**الاستخدام من خلال سطر الأوامر:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**الاستخدام من خلال الكود:**

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