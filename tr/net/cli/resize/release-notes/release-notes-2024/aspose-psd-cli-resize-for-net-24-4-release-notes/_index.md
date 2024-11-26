---
title: Aspose.PSD CLI Yeniden Boyutlandırma için .NET 24.4 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD CLI Yeniden Boyutlandırma için .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                     | **Kategori** |
|:------------|:-------------------------------------------------------------|:-------------|
| PSDNET-2026 | Aspose.PSD CLI Yeniden Boyutlandırma Uygulamasının İlk Sürümü | Geliştirme   |


## **Kullanım örnekleri:**

**PSDNET-2026. Aspose.PSD CLI Yeniden Boyutlandırma Uygulamasının İlk Sürümü**

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
