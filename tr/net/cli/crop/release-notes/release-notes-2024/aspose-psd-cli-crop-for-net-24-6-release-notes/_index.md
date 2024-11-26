---
title: Aspose.PSD CLI Kırpma için .NET 24.6 - Sürüm Notları
type: docs
weight: 90
url: /tr/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD CLI Kırpma için .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                                                   | **Kategori**  |
|:------------|:------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI Uygulamalarının İlk Sürümü: Aspose.PSD.CLI.Export ve Aspose.PSD.CLI.NLP.Editor | Geliştirme |


## **Kullanım örnekleri:**

**PSDNET-2110. Aspose.PSD CLI Kırpma Uygulamasının İlk Sürümü**

**Komut satırından kullanım:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Koddan kullanım:**

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

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}
