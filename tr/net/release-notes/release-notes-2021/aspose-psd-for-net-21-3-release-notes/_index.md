---
title: Aspose.PSD for .NET 21.3 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-823|Katman gruplarıyla deneyimi iyileştirmek için SectionDividerLayer ekle|Geliştirme|
|PSDNET-694|PattResource okurken genişlik ve yükseklik değiştirildi|Hata|
|PSDNET-789|Birden fazla Katman Efektinin Yanlış Karıştırılması|Hata|
|PSDNET-805|Birden fazla Katman Efekti olduğunda Yanlış Karıştırma sırası ve mantığı|Hata|
|PSDNET-842|Vuruş efekti özellikleri PSD dosyasına kaydedilmiyor|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-694. PattResource okurken genişlik ve yükseklik değiştirildi**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // deseni işle

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Birden fazla Katman Efektinin Yanlış Karıştırılması**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // Metin Katmanını arama
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "En İyi";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // Bu şekilde değiştirilmiş PSD Dosyası kaydedilir
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Birden fazla Katman Efekti olduğunda Yanlış Karıştırma sırası ve mantığı**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                //Bu şekilde değiştirilmiş PSD Dosyası kaydedilir
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Katman gruplarıyla deneyimi iyileştirmek için SectionDividerLayer ekle**

{{< highlight csharp >}}
            // Aşağıdaki kod, SectionDividerLayer katmanlarını ve ona ilişkin LayerGroup'u nasıl alacağınızı göstermektedir.

            // Katmanlar hiyerarşisi
            //    [0]: 'Group 1' için '</Layer group>' SectionDividerLayer
            //    [1]: 'Layer 1' Regular Layer
            //    [2]: 'Group 2' için '</Layer group>' SectionDividerLayer
            //    [3]: 'Group 3' için '</Layer group>' SectionDividerLayer
            //    [4]: 'Group 3' Grup Katmanı
            //    [5]: 'Group 2' Grup Katmanı
            //    [6]: 'Group 1' Grup Katmanı

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Nesneler eşit değil.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Katmanlar hiyerarşisi oluşturma
                // 'Group 1' adında LayerGroup ekle
                LayerGroup group1 = image.AddLayerGroup("Group 1", 0, true);
                // Normal katman ekle
                Layer layer1 = new Layer();
                layer1.DisplayName = "Layer 1";
                group1.AddLayer(layer1);
                // 'Group 2' adında LayerGroup ekle
                LayerGroup group2 = group1.AddLayerGroup("Group 2", 1);
                // 'Group 3' adında LayerGroup ekle
                LayerGroup group3 = group2.AddLayerGroup("Group 3", 0);

                // SectionDividerLayer'ları al
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // SectionDividerLayer.GetRelatedLayerGroup() yöntemini kullanarak ilgili LayerGroup örneğini alın.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // aynı LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // aynı LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // aynı LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Group 1', 5 katman içeriyor
            }
{{< /highlight >}}

**PSDNET-842. Vuruş efekti özellikleri PSD dosyasına kaydedilmiyor**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Nesneler eşit değil.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // ArgumentNullException atmayacak

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Kaydedilen değerleri kontrol et
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
