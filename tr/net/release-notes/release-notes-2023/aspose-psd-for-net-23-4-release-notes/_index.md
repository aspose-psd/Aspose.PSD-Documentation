---
title: Aspose.PSD for .NET 23.4 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/aspose-psd-for-net-23-4-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 23.4 için sürüm notlarını](https://www.nuget.org/packages/Aspose.PSD/) içermektedir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1409|Halka açık API'de PSD API'nin yerine kullanmak için RawColor sınıfını tasarlayın|Geliştirme|
|PSDNET-1332|Probasyondan Gradient Haritası Ayarlama Katmanını Ana Aspose.PSD koduna entegre edin|Özellikler|
|PSDNET-1448|Metin kullanılarak metin düzenleme, doğru sonucu kaydetmez|Hata|
|PSDNET-1449|ITextPortion tarafından Metin Katmanı düzenlenirken stillerin veya paragrafların başlangıcı ve sonu yanlış yerde görünür|Hata|
|PSDNET-1509|Photoshop'ta düzenleme yaparken biçimlendirme hareket eder|Hata|


## **Halka Açık API Değişiklikleri**

# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor


# **Kaldırılan API'ler:**
- Hiçbiri


## **Kullanım Örnekleri:**

**PSDNET-1332. Probasyondan Ana Aspose.PSD Koduna Gradient Haritası Ayarlama Katmanını Entegre Etme**

{{< highlight csharp >}}
string kaynakDosya = "gradient_map_default.psd";
string çıktıDosyası = "gradient_map_res.psd";

using (var görüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions()))
{
    Katman katman = görüntü.Layers[1];
    GrdmResource grdmKaynak = (GrdmResource)katman.Resources[0];

    // mevcut değerleri kontrol et

    grdmKaynak.Reverse = true;
    // ikinci gradyan rengi için Kırmızı renk
    grdmKaynak.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmKaynak.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmKaynak.ColorPoints[1].RawColor.Components[3].Value = 0;

    görüntü.Save(çıktıDosyası, new PsdOptions());
}

using (var görüntü = (PsdImage)Image.Load(çıktıDosyası))
{
    Katman katman = görüntü.Layers[1];
    GrdmResource grdmKaynak = (GrdmResource)katman.Resources[0];

    // değişen değerleri kontrol et
    
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1409. Halka açık API için RawColor sınıfını tasarlayın, eski Color yapısının yerine PSD API'sinde kullanın**

{{< highlight csharp >}}
// örnek geçersiz kılma metodu
void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}

var renk = new RawColor(PixelDataFormat.Rgba32Bpp);
var eskiRenk = Color.FromArgb(5, 1, 2, 3);

var argbDeğeri = eskiRenk.ToArgb();
renk.SetAsInt(argbDeğeri);

AssertAreEqual("ARGB", renk.GetColorModeName());
AssertAreEqual(32, renk.GetBitDepth());
AssertAreEqual("A Alpha", renk.Components[0].FullName);
AssertAreEqual(5, (int)renk.Components[0].Value);
AssertAreEqual("R Red", renk.Components[1].FullName);
AssertAreEqual(1, (int)renk.Components[1].Value);
AssertAreEqual("G Green", renk.Components[2].FullName);
AssertAreEqual(2, (int)renk.Components[2].Value);
AssertAreEqual("B Blue", renk.Components[3].FullName);
AssertAreEqual(3, (int)renk.Components[3].Value);

AssertAreEqual(argbDeğeri, renk.GetAsInt());
{{< /highlight >}}

**PSDNET-1448. Metin Portion'ları kullanılarak metin düzenleme, doğru sonucu kaydetmez**

{{< highlight csharp >}}
// kod parçası
{{< /highlight >}}

**PSDNET-1449. ITextPortion tarafından Metin Katmanı düzenlendiğinde stillerin veya paragrafların başlangıcı ve sonu yanlış yerde görünür**

{{< highlight csharp >}}
// kod parçası
{{< /highlight >}}

**PSDNET-1509. Photoshop'ta düzenleme yaparken biçimlendirme hareket eder**

{{< highlight csharp >}}
// kod parçası
{{< /highlight >}}