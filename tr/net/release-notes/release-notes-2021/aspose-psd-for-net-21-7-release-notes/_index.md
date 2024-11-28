---
title: Aspose.PSD için .NET 21.7 - Sürüm Notları
type: docs
weight: 60
url: /tr/net/aspose-psd-icin-net-21-7-sürüm-notları/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 21.7](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içermektedir. 

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-806|Metin Parçaları Kullanılarak Yazı Tipi Düzenleme Desteği|Özellik|
|PSDNET-917|Aspose.PSD 21.6: PSD'den PNG'ye dönüştürme denemesinde ImageSaveException hatası|Hata|
|PSDNET-858|Aspose.PSD .Net 5.0 Yapılandırmasına Ekle|Geliştirme|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FontSettings.GetAdobeFontName(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontName

# **Kaldırılan API'ler:**
- Yok

## **Kullanım örnekleri:**

**PSDNET-806. Metin Parçaları Kullanılarak Yazı Tipi Düzenleme Desteği**

{{< highlight csharp >}}
            string outputFilePng = "sonuc_fontDuzenlemeTesti.png";
            string outputFilePsd = "fontDuzenlemeTesti.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Objeler eşit değil.");
                }
            }

            using (var image = new PsdImage(500, 500))
            {
                FillLayer backgroundFillLayer = FillLayer.CreateInstance(FillType.Color);
                ((IColorFillSettings)backgroundFillLayer.FillSettings).Color = Color.White;
                image.AddLayer(backgroundFillLayer);

                TextLayer textLayer = image.AddTextLayer("Metin 1", new Rectangle(10, 35, image.Width, 35));

                ITextPortion firstPortion = textLayer.TextData.Items[0];
                firstPortion.Style.FontName = FontSettings.GetAdobeFontName("Comic Sans MS");

                var secondPortion = textLayer.TextData.ProducePortion();
                secondPortion.Text = "Metin 2";
                secondPortion.Paragraph.Apply(firstPortion.Paragraph);
                secondPortion.Style.Apply(firstPortion.Style);
                secondPortion.Style.FontName = FontSettings.GetAdobeFontName("Arial");

                textLayer.TextData.AddPortion(secondPortion);
                textLayer.TextData.UpdateLayerData();

                image.Save(outputFilePng, new PngOptions());
                image.Save(outputFilePsd);
            }

            using (var image = (PsdImage)Image.Load(outputFilePsd))
            {
                TextLayer textLayer = (TextLayer)image.Layers[2];

                string adobeFontName1 = FontSettings.GetAdobeFontName("Comic Sans MS");
                string adobeFontName2 = FontSettings.GetAdobeFontName("Arial");

                AssertAreEqual(adobeFontName1, textLayer.TextData.Items[0].Style.FontName);
                AssertAreEqual(adobeFontName2, textLayer.TextData.Items[1].Style.FontName);
            }
{{< /highlight >}}

**PSDNET-917. Aspose.PSD 21.6: PSD'den PNG'ye dönüştürme denemesinde ImageSaveException hatası**

{{< highlight csharp >}}
            string srcFile = "input.psd";
            string output = "output.png";

            using (var image = Aspose.PSD.Image.Load(srcFile))
            {
                image.Save(output, new Aspose.PSD.ImageOptions.PngOptions());
            }
{{< /highlight >}}
