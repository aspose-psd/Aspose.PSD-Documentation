---
title: Aspose.PSD for .NET 23.3 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-psd-for-net-23-3-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-146|Posterize Düzenleme Katmanı Desteği|Özellik|
|PSDNET-1366|VscgResource Desteğinin Uygulanması|Özellik|
|PSDNET-1437|Posterize Düzenleme Katmanı Veri İçin PostResource Kaynağının Desteğinin Eklenmesi|Özellik|
|PSDNET-931|Curves ayarlaması ve CMYK renk moduyla katmanın PNG'ye yanlış dışa aktarımı|Hata|
|PSDNET-1403|Dosyanın kaydedilmesinden ve dosyanın PS tarafından güncelleştirilmesinden sonra Paragrafın Stili kayboluyor|Hata|
|PSDNET-1453|Metindeki ışıldama ve gölge efektlerinin bozulmuş render'ı|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **Kaldırılan API'ler:**
- Hiçbiri


## **Kullanım Örnekleri:**

**PSDNET-146. Posterize Düzenleme Katmanı Desteği**

{{< highlight csharp >}}
string kaynakDosya = "zendeya_posterize.psd";
string çıktıDosya = "zendeya_posterize_10.psd";

using (var görüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions()))
{
    foreach (Layer katman in görüntü.Layers)
    {
        if (katman is PosterizeLayer)
        {
            ((PosterizeLayer)katman).Levels = 10;
            görüntü.Save(çıktıDosya);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Curves ayarlaması ve CMYK renk moduyla katmanın PNG'ye yanlış dışa aktarımı**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // the ', new PsdOptions()' provocating a bug.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. VscgResource Desteğinin Uygulanması**

{{< highlight csharp >}}
string kaynakDosya = "StrokeInternalFill_src.psd";
string çıktıDosya = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"Değerler eşit değil.\nBeklenen:{expected}\nSonuç:{current}\nFark:{expected - current}");
    }
}

using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    VscgResource vscgResource = (VscgResource)görüntü.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // Kırmızı
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // Yeşil
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // Mavi

    görüntü.Save(çıktıDosya);
}

// Değişiklikleri kontrol etme
using (PsdImage görüntü = (PsdImage)Image.Load(çıktıDosya))
{
    VscgResource vscgResource = (VscgResource)görüntü.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Dosyanın kaydedilmesinden ve dosyanın PS tarafından güncelleştirilmesinden sonra Paragrafın Stili kayboluyor**

{{< highlight csharp >}}
string kaynakDosya = "PSDTest3.psd";
string çıktıDosya = "output.psd";

string[] yeniMetin = new string[]
{
    "Başlık \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage görüntü = (PsdImage)Aspose.PSD.Image.Load(kaynakDosya))
{
    TextLayer katman2 = görüntü.AddTextLayer("Yeni katman", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var metinVerisiTL = katman2.TextData;

    ITextStyle varsayılanStilTL = metinVerisiTL.ProducePortion().Style;

    ITextParagraph varsayılanParagrafTL = metinVerisiTL.ProducePortion().Paragraph;
    ITextPortion[] yeniParçalarTL = metinVerisiTL.ProducePortions(yeniMetin, varsayılanStilTL, varsayılanParagrafTL);

    yeniParçalarTL[0].Style.FontSize = 14;
    yeniParçalarTL[0].Style.FontName = "TwCenMT-Bold";

    yeniParçalarTL[1].Style.Leading = 20;
    yeniParçalarTL[1].Style.FontSize = 10;
    yeniParçalarTL[1].Style.FontName = "TwCenMT-Bold";

    // Eski metni kaldırma
    metinVerisiTL.RemovePortion(0);

    // Yeni metin parçalarını ekleme
    foreach (var yeniParça in yeniParçalarTL)
    {
        metinVerisiTL.AddPortion(yeniParça);
    }

    metinVerisiTL.UpdateLayerData();

    görüntü.Save(çıktıDosya);
}

using (PsdImage psdGörüntü = (PsdImage)Aspose.PSD.Image.Load(çıktıDosya))
{
    Txt2Resource txt2ÇıktıKaynak = (Txt2Resource)psdGörüntü.GlobalLayerResources[1];
    byte[] baytlar = txt2ÇıktıKaynak.Data;
    string txt2Veri = "";
    for (int i = 18900; i < baytlar.Length; i++)
    {
        txt2Veri += (char)baytlar[i];
    }

    string anahtar0 = @" >> /6 0 >> >> /1 "; // paragraf 0'ın uzunluğuna ön ek
    string anahtar1 = @" >> /6 1 >> >> /1 "; // paragraf 1'in uzunluğuna ön ek
    int indeks0 = txt2Veri.IndexOf(anahtar0);
    int indeks1 = txt2Veri.IndexOf(anahtar1);

    string par0Uzunluk = txt2Veri.Substring(indeks0 + anahtar0.Length, 1);
    string par1Uzunluk = txt2Veri.Substring(indeks1 + anahtar1.Length, 3);

    string beklenen0 = yeniMetin[0].Length.ToString();
    string beklenen1 = (yeniMetin[1].Length + 1).ToString();

    if (par0Uzunluk != beklenen0 || par1Uzunluk != beklenen1)
    {
        throw new Exception(
            $"Paragraf uzunlukları yanlış.\nBeklenen: {beklenen0} ve {beklenen1}\nSonuç: {par0Uzunluk} ve {par1Uzunluk}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Posterize Düzenleme Katmanı Veri İçin PostResource Kaynağının Desteğinin Eklenmesi**

{{< highlight csharp >}}
string kaynakDosya = "zendeya_posterize.psd";
string çıktıDosya = "zendeya_posterize_10.psd";

using (var görüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions()))
{
    Layer katman = görüntü.Layers[1];

    foreach (LayerResource kaynak in katman.Resources)
    {
        if (kaynak is PostResource)
        {
            ((PostResource)kaynak).Levels = 10;
            görüntü.Save(çıktıDosya);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Metindeki ışıldama ve gölge efektlerinin bozulmuş render'ı**

{{< highlight csharp >}}
string çıktıPsd = "effect_bug.psd";
string çıktıPng = "effect_bug.png";

using (var psdGörüntü = new PsdImage(500, 500))
{
    // Metin katmanları ekleyin
    Aspose.PSD.Rectangle metinAlan1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle metinAlan2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle metinAlan3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer metinKatmanı1 = psdGörüntü.AddTextLayer("Efektli Metin", metinAlan1);
    TextLayer metinKatmanı2 = psdGörüntü.AddTextLayer("Efektli Metin", metinAlan2);
    TextLayer metinKatmanı3 = psdGörüntü.AddTextLayer("Efektli Metin", metinAlan3);

    // Metin katmanlarını değiştirin
    metinKatmanı1.TextData.Items[0].Style.FontSize = 150;
    metinKatmanı1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    metinKatmanı1.TextData.UpdateLayerData();

    metinKatmanı2.TextData.Items[0].Style.FontSize = 150;
    metinKatmanı2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    metinKatmanı2.TextData.UpdateLayerData();

    metinKatmanı3.TextData.Items[0].Style.FontSize = 150;
    metinKatmanı3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    metinKatmanı3.TextData.UpdateLayerData();

    // Efektler ekleyin
    OuterGlowEffect ışıltı = metinKatmanı1.BlendingOptions.AddOuterGlow(); // kırılma
    ışıltı.Spread = 15;
    ((ColorFillSettings)ışıltı.FillColor).Color = Color.Red;

    var gölge = metinKatmanı2.BlendingOptions.AddDropShadow(); // uzun metin ile kırılır
    gölge.Distance = 25;
    gölge.Color = Color.DarkBlue;

    var içGölge = metinKatmanı3.BlendingOptions.AddInnerShadow(); // uzun metin ile kırılır
    içGölge.UseGlobalLight = false;
    içGölge.Angle = -179;
    içGölge.Distance = 10;
    içGölge.Size = 8;
    içGölge.Color = Color.HotPink;

    // dışa aktar
    psdGörüntü.Save(çıktıPsd);
    psdGörüntü.Save(çıktıPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}