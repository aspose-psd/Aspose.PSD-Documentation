---
title: Aspose.PSD CLI Resize için .NET 24.6 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD CLI Resize için .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) sürümü hakkındaki sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI Uygulamalarının İlk Sürümü: Aspose.PSD.CLI.Export ve Aspose.PSD.CLI.NLP.Editor | Geliştirme |

## **Kullanım Örnekleri:**

**PSDNET-2110. Aspose.PSD CLI Resize Uygulamasının İlk Sürümü**

**Komut satırından kullanım:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Koddan kullanım:**

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
