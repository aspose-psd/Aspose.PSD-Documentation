---
title: Aspose.PSD için .NET 23.2 - Sürüm Notları
type: docs
weight: 110
url: /tr/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1359|Metin konumlandırma, rendering ve destek iyileştirmeleri için metin renderlama yeniden yapıldı|Geliştirme|
|PSDNET-1270|Warp Effect işleme yeteneği ekleyin|Özellik|
|PSDNET-1391|Paragraf ayarlarından Bottom-to-Bottom ve Top-to-Top liderlik modlarını destekleme|Özellik|
|PSDNET-912|TextLayer PSD için Yazı Tipi ve Renk Değiştirme|Hata|
|PSDNET-1022|Test TextUpdateTests'te metnin yanlış dışa aktarımı, metin eksik|Hata|
|PSDNET-1221|Daha büyük PSD görüntüsünün yeniden boyutlandırılmasından sonra ekstra küçük metin eksik|Hata|
|PSDNET-1301|Aspose.Psd için .NET textLayer.UpdateText(), farklı veri kümeleri için '-' (tire) karakterini rastgele alt çizgi olarak yazdırıyor|Hata|
|PSDNET-1379|ResolutionSettings, PSD'den PDF'e dışa aktarımda uygulanmaz|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **Kaldırılan API'lar:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Kullanım örnekleri:**

**PSDNET-912. TextLayer PSD için Font ve Renk Değiştirme**

{{< highlight csharp >}}
string fontsFolder = "Fontlar";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "sonuç.psd";
string outputPng = "sonuç.png";

FontSettings.SetFontsFolder(fontsFolder);

using (var image = (PsdImage)Image.Load(srcFile))
{
    TextLayer nameLayer = (TextLayer)image.Layers[9];
    var textPortion = nameLayer.TextData.Items[0];

    textPortion.Text = "MODESTO SR";
    textPortion.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textPortion.Style.FillColor = Color.Red;

    nameLayer.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Test TextUpdateTests'te metnin yanlış dışa aktarımı, metin eksik**

{{< highlight csharp >}}
string srcFile = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var image = (PsdImage)Image.Load(srcFile))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var layer = image.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("Text is updated");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Daha büyük PSD görüntüsünün yeniden boyutlandırılmasından sonra ekstra küçük metin eksik**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Warp Effect işleme yeteneği ekleyin**

{{< highlight csharp >}}
string sourceFile = "kaynak.psd";
string pngWarpedExport = "kıvrılmış.png";
string psdWarpedExport = "warpDosyası.psd";

var warpLoadOptions = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(sourceFile, warpLoadOptions))
{
    image.Save(pngWarpedExport, new PngOptions());
    image.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd için .NET textLayer.UpdateText(), farklı veri kümeleri için '-' (tire) karakterini rastgele alt çizgi olarak yazdırıyor**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "ÇIKTIRESİM.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "AD":
                    textLayer.UpdateText("BAY JACK SMITH");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "YETKİ":
                    textLayer.UpdateText("MEMUR-001");
                    break;
                case "KANGRUP":
                    textLayer.UpdateText("AB-");
                    break;
                case "ADRES":
                    textLayer.UpdateText("BLOK-A, CADDE-7, APARTMAN NO - 047, SEKTÖR-024");
                    break;
                case "KALİCİADRES":
                    textLayer.UpdateText("EV NO - 42, YOL -025, PALM YEŞİL GÖRÜNÜM KONUT TOPLULUĞU, SEKTÖR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. ResolutionSettings, PSD'den PDF'e dışa aktarımda uygulanmaz**

{{< highlight csharp >}}
string input = "Veri1.psd";
string output = "Veri1.pdf";

using (var image = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting resolutionSetting = new ResolutionSetting(300, 300);

    image.Save(output, new PdfOptions()
    {
        ResolutionSettings = resolutionSetting
    });
}
{{< /highlight >}}

**PSDNET-1391. Paragraf ayarlarından Bottom-to-Bottom ve Top-to-Top liderlik modlarına destek ekleme**

{{< highlight csharp >}}
string input = "liderlikModu.psd";
string output = "çıktı_liderlikModu.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var textPortion in text1.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.TopToTop; // Liderlik türünü değiştir   
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var textPortion in text2.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.BottomToBottom; // Liderlik türünü değiştir   
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}
