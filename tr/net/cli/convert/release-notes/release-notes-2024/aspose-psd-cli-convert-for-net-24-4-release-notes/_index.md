---
title: Aspose.PSD CLI Dönüştürücü için .NET 24.4 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/cli/donusum/aspose-psd-donusum-cli-uygulamasi-icin-net-24-6-sürüm-notlari/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD CLI Dönüştürücü için .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/) sürümüne ilişkin sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                | **Kategori** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Aspose.PSD CLI Dönüştürücü Uygulamasının İlk Sürümü |  İyileştirme |


## **Kullanım Örnekleri:**

**PSDNET-2023. Aspose.PSD CLI Dönüştürücü Uygulamasının İlk Sürümü**

**Komut satırından kullanım:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Kod üzerinden kullanım:**

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
