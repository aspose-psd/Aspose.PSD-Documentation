---
title: Aspose.PSD for .NET 24.2 - Sürüm Notları
type: docs
weight: 110
url: /tr/net/aspose-psd-for-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                 | **Kategori**     |
|:------------ |:-------------------------------------------------------------------------- |:----------------- |
| PSDNET-1503  | PatternFillSettings için Açı özelliğini işle                                  | Özellik           |
| PSDNET-1719  | Metin Katmanı için dikey ve yatay ölçek desteği                              | Özellik           |
| PSDNET-1783  | [AI Format] PDF tabanlı AI Formatında arka planın doğru şekilde işlenmesi    | Özellik           |
| PSDNET-1611  | Bozulmayı değiştirme mekanizmasını saptayın                                  | Geliştirme        |
| PSDNET-1802  | Bozulmayı hızlandırma                                                       | Geliştirme        |
| PSDNET-995   | Belge açılırken "Resim yüklenemedi." istisnası                               | Hata              |
| PSDNET-1491  | Vuruş Deseni olan psd dosyalarının kaydedilmesini düzeltme                   | Hata              |
| PSDNET-1642  | ReplaceContents kullanıldığında akıllı nesnede metin stili yanlış            | Hata              |
| PSDNET-1884  | [AI Format] AI dosyasında Kübik Bezier çizimini düzeltme                     | Hata              |

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Kaldırılan API'lar:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-1503. PatternFillSettings için Açı özelliğini işle**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string outputFile = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(outputFile, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Metin Katmanı için dikey ve yatay ölçek desteği**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "1719_src.psd");
string output = Path.Combine(outputFolder, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [AI Format] PDF tabanlı AI Formatında arka planın doğru şekilde işlenmesi**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "pineapples.ai");
string outputFilePath = Path.Combine(outputFolder, "pineapples.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. Belge açılırken "Resim yüklenemedi." istisnası**

{{< highlight csharp >}}
// Kod ekleme yapmayın, yalnızca yorumlar varsa çevirin
{{< /highlight >}}

**PSDNET-1491. Vuruş Deseni olan psd dosyalarının kaydedilmesini düzeltme**

{{< highlight csharp >}}
// Kod ekleme yapmayın, yalnızca yorumlar varsa çevirin
{{< /highlight >}}

**PSDNET-1642. ReplaceContents kullanıldığında akıllı nesnede metin stili yanlış**

{{< highlight csharp >}}
// Kod ekleme yapmayın, yalnızca yorumlar varsa çevirin
{{< /highlight >}}

**PSDNET-1884. [AI Format] AI dosyasında Kübik Bezier çizimini düzeltme**

{{< highlight csharp >}}
// Kod ekleme yapmayın, yalnızca yorumlar varsa çevirin
{{< /highlight >}}

**PSDNET-1611. Bozulmayı değiştirme mekanizmasını saptayın**

{{< highlight csharp >}}
// Kod ekleme yapmayın, yalnızca yorumlar varsa çevirin
{{< /highlight >}}

**PSDNET-1802. Bozulmayı hızlandırma**

{{< highlight csharp >}}
// Kod ekleme yapmayın, yalnızca yorumlar varsa çevirin
{{< /highlight >}}
