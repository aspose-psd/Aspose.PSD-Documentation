---
title: Aspose.PSD for .NET 23.9 - Sürüm Notları
type: docs
weight: 40
url: /tr/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
|:------------|:----------|:-------------|
| PSDNET-1638 | Yeni ayar katmanları için maske oluşturma uygulaması | Özellik |
| PSDNET-1654 | Grup karıştırma seçeneği olarak Bükülmüş Katmanları Katman ekleme desteği | Özellik |
| PSDNET-1194 | 16 bitlik renk moduna sahip PSD dosyası ayar katmanları için maske uygulamaz | Hata |
| PSDNET-1235 | Metin katmanındaki parantezlerin yanlış render edilmesi | Hata |
| PSDNET-1559 | Metin katmanlarında stilleri güncelleyememe | Hata |
| PSDNET-1583 | CMYK ile dışa aktarılan PSD dosyasında renklerin bozulması | Hata |
| PSDNET-1619 | Belirli PSB dosyası "Dikdörtgenin ortak bir işleme alanı yok" istisnası fırlatıyor | Hata |
| PSDNET-1648 | Görüntü yükleme başarısız. OverflowException: Aritmetik işlem bir taşmayla sonuçlandı | Hata |


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **Kaldırılan API'lar:**
- Hiçbiri


## **Kullanım örnekleri:**

**PSDNET-1638. Yeni ayar katmanları için maske oluşturma uygulaması**

{{< highlight csharp >}}
string srcFile = "zendeya_BW.psd";
string dstFile = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(dstFile);
}

using (var im = (PsdImage)Image.Load(dstFile))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Grup karıştırma seçeneği olarak Bükülmüş Katmanları Katman ekleme desteği**

{{< highlight csharp >}}
string kaynakDosya = "ornek_kaynak.psd";
string ciktiPsd = "ornek_cikti.psd";
string ciktiPng = "ornek_cikti.png";

using (var image = (PsdImage)Image.Load(kaynakDosya))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(ciktiPsd);
    image.Save(ciktiPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. 16 bitlik renk moduna sahip PSD dosyası ayar katmanları için maske uygulamaz**

{{< highlight csharp >}}
string kaynakDosya = "kaynak.psd";
string ciktiPng = "mevcut.png";

using (var image = (PsdImage)Image.Load(kaynakDosya))
{
    image.Save(ciktiPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Metin katmanındaki parantezlerin yanlış render edilmesi**

{{< highlight csharp >}}
string dosya = "dosya1.psd";
string cikti = "cikti_1235.png";

using (var psdImage = (PsdImage)Image.Load(dosya))
{
    foreach (var layer in psdImage.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = new PsdOptions(psdImage);
    psdImage.Save(cikti, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. Metin katmanlarındaki stilleri güncelleyememe**

{{< highlight csharp >}}
string kaynakDosya = "Ornek_FontBuyukluk.psd";
string ciktiDosyasi = "cikti_Ornek_FontBuyukluk.psd";

using (var psdImage = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdImage.Layers[4];
    var l2 = (TextLayer)psdImage.Layers[5];

    var textItems1 = l1.TextData.ProducePortions(new string[] { "metin1", "metin2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var item in textItems1)
    {
        l1.TextData.AddPortion(item);
    }

    var textItems2 = l2.TextData.ProducePortions(new string[] { "metin katmanı 1", "metin katmanı 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(ciktiDosyasi);
}
{{< /highlight >}}

**PSDNET-1583. CMYK ile dışa aktarılan PSD dosyasında renklerin bozulması**

{{< highlight csharp >}}
string kaynakDosya = "kanyon.psd";
string ciktiPngDosyasi = "cikti_kanyon.png";

using (var outputStream = new MemoryStream())
{
    using (var psdImage = (PsdImage)Image.Load(kaynakDosya))
    {
        psdImage.Save(outputStream);
    }

    outputStream.Position = 0;
    using (var psdImage = (PsdImage)Image.Load(outputStream))
    {
        psdImage.Save(ciktiPngDosyasi, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Belirli PSB dosyası "Dikdörtgenin ortak bir işleme alanı yok" istisnası fırlatıyor**

{{< highlight csharp >}}
var girdi = "1619_kaynak.psb";
var cikti = "1619_cikti.png";
using (PsdImage img = (PsdImage)Image.Load(girdi, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(cikti,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Görüntü yükleme başarısız. OverflowException: Aritmetik işlem bir taşmayla sonuçlandı**

{{< highlight csharp >}}
string kaynakDosya = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(kaynakDosya))
{
    Layer layer = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}
