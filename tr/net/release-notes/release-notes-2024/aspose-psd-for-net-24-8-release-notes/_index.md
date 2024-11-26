---
title: Aspose.PSD için .NET 24.8 - Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-24-8-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 24.8](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                                          | **Kategori** |
|:------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2091 | [AI Format] XObject Grupları için işleme ekle                                                    | Geliştirme   |
| PSDNET-1754 | TextLayer ve SmartObjectLayer için Warp dönüşüm yeteneklerini geliştirme                        | Özellik      |
| PSDNET-1836 | [AI Format] İçerik akışı operatörlerinde katmanları işleme ekle                                  | Özellik      |
| PSDNET-2015 | AI dosyasının yineleme sonucu Illustrator sonuçlarıyla çok farklı                                  | Hata         |
| PSDNET-2093 | Smart Objectleri tekrar bağlamak tüm Smart Objectlerde uygulanmaz                           | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-1754. TextLayer ve SmartObjectLayer için WarpSettings ekleyerek Warp dönüşüm yeteneklerini geliştirme**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "smart_without_warp.psd");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

string[] çıktıGörselDosyası = new string[4];
string[] çıktıPsdDosyası = new string[4];

for (int caseIndex = 0; caseIndex < çıktıGörselDosyası.Length; caseIndex++)
{
    çıktıGörselDosyası[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".png");
    çıktıPsdDosyası[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".psd");

    using (PsdImage img = (PsdImage)Image.Load(kaynakDosya, opt))
    {
        foreach (Layer layer in img.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                var smartLayer = (SmartObjectLayer)layer;
                smartLayer.WarpSettings = GetWarpSettingsByIndex(smartLayer.WarpSettings, caseIndex);
            }

            if (layer is TextLayer)
            {
                var textLayer = (TextLayer)layer;

                if (caseIndex != 3)
                {
                    textLayer.WarpSettings = GetWarpSettingsByIndex(textLayer.WarpSettings, caseIndex);
                }
            }
        }

        img.Save(çıktıPsdDosyası[caseIndex], new PsdOptions());
    }

    using (PsdImage img = (PsdImage)Image.Load(çıktıPsdDosyası[caseIndex], opt))
    {
        img.Save(çıktıGörselDosyası[caseIndex],
            new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
    }
}

WarpSettings GetWarpSettingsByIndex(WarpSettings warpParams, int caseIndex)
{
    switch (caseIndex)
    {
        case 0:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 20;
            break;
        case 1:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Vertical;
            warpParams.Value = 10;
            break;
        case 2:
            warpParams.Style = WarpStyles.Flag;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 30;
            break;
        case 3:
            warpParams.Style = WarpStyles.Custom;
            warpParams.MeshPoints[2].Y += 70;
            break;
    }

    return warpParams;
}
{{< /highlight >}}

**PSDNET-1836. [AI Format] İçerik akışı operatörlerinde katmanları işleme ekle**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "Layers-NoPen.ai");
string çıktıDosyası = Path.Combine(outputFolder, "Layers-NoPen.output.png");

using (AiImage image = (AiImage)Image.Load(kaynakDosya))
{
    image.Save(çıktıDosyası, new PngOptions());
}

//// "Kalem" adlı katmandan eğriler gizlenmelidir
{{< /highlight >}}

**PSDNET-2015. AI dosyasının yineleme sonucu Illustrator sonuçlarıyla çok farklı**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "4.ai");
string çıktıDosyaYolu = Path.Combine(outputFolder, "4.png");

using (AiImage image = (AiImage)Image.Load(kaynakDosya))
{
    image.Save(çıktıDosyaYolu, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2093. Smart Objectleri yeniden bağlamak PSD dosyasındaki tüm Smart Objectlere uygulanmaz**

{{< highlight csharp >}}
string[] dosyalar = { "simple_test", "w22" };
string değiştirDosya = Path.Combine(baseFolder, "image(19).png");

string[] kaynakDosya = new string[dosyalar.Length];
string[] çıktıDosyalar = new string[dosyalar.Length];

for (int i = 0; i < dosyalar.Length; i++)
{
    kaynakDosya[i] = Path.Combine(baseFolder, dosyalar[i] + ".psd");
    çıktıDosyalar[i] = Path.Combine(outputFolder, dosyalar[i] + "_output.psd");

    using (var image = (PsdImage)Image.Load(kaynakDosya[i]))
    {
        foreach (Layer layer in image.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                SmartObjectLayer smart = (SmartObjectLayer)layer;

                // İkinci akıllı katmanda burada hata vardı
                smart.ReplaceContents(değiştirDosya);
            }
        }

        image.Save(çıktıDosyalar[i]);
    }
}
{{< /highlight >}}
