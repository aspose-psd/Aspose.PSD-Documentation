---
title: Aspose.PSD için .NET 21.1 - Sürüm Notları
type: docs
weight: 120
url: /tr/net/aspose-psd-icin-net-21-1-sürüm-notları/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD için .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/) için yayımlama notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Belirli Psd dosyasını png'ye dönüştürmeye çalışırken istisna oluşuyor|Hata|
|PSDNET-792|Akıllı nesne içeren PSD'yi PNG olarak kaydederken istisna oluşur|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- Yok

# **Kaldırılan API'ler:**
- Yok

## **Kullanım örnekleri:**
**PSDNET-766. Aspose.PSD 20.10: Belirli Psd dosyasını png'ye dönüştürmeye çalışırken istisna oluşuyor**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Akıllı nesne içeren PSD'yi PNG olarak kaydederken istisna oluşur**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder + "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Akıllı Nesneyi Arıyoruz
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Akıllı Nesne Katmanını Bellek Akışından Yüklüyoruz,
                        // Ancak smart.ExportContents(somePath) yöntemini kullanarak akıllı nesneyi dosyaya dışa aktarabiliriz
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Metin Katmanını Arıyoruz
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Basitçe UpdateText kullanabiliriz, ancak bu şekilde bize metni kısımlar halinde düzenleme olanağı sağlar
                                        // Çok satırlı metin katmanları ve diğer metin ve paragraf stili özellikleri oluşturabiliriz
                                        // Dikkatli olmalısınız. Eğer Akıllı Nesne İçeriği PSD değilse, metin düzenleme bu yolu kullanamazsınız
                                        // Bu durumda, grafiği kullanmalısınız: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "En İyi";

                                        // Görüntünün güzel görünmesini istiyorsanız metin boyutunu değiştirmelisiniz.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // ReplaceContents kullanmak daha iyidir. Akıllı Nesneyi otomatik olarak yeniden oluşturacaktır
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Bu şekilde değiştirilmiş PSD Dosyasını kaydediyoruz
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
