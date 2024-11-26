---
title: Aspose.PSD for .NET 21.5 - Sürüm Notları
type: docs
weight: 80
url: /tr/net/aspose-psd-for-net-21-5-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 21.5](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-758|Vektör yolları olan şekil katmanlarını yeniden boyutlandırma desteği|Özellik|
|PSDNET-862|Yalnızca bir katman yeniden boyutlandırıldığında vektör yolları olan şekil katmanlarını yeniden boyutlandırma desteği|Özellik|
|PSDNET-578|Kısaltılmış metin dizisi|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- Yok

# **Kaldırılan API'lar:**
- Yok

## **Kullanım örnekleri:**

**PSDNET-578. Kısaltılmış metin dizisi**

{{< highlight csharp >}}
            string srcFile = "grinched-regular-font.psd";
            string output = "output_grinched-regular-font.psd.png";

            // Yazı tipleri yolunu ayarlayın
            System.Collections.Generic.List<string> fonts = new System.Collections.Generic.List<string>();
            fonts.AddRange(FontSettings.GetDefaultFontsFolders());
            fonts.Add(@"Fonts\");
            FontSettings.SetFontsFolders(fonts.ToArray(), true);

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-758. Vektör yolları olan şekil katmanlarını yeniden boyutlandırma desteği**

{{< highlight csharp >}}
            string kaynakDosyaAdı = "vectorShapes.psd";
            string çıkışDosyaAdı = "çıktı_vectorShapes.psd";
            string veriDizini = "PSDNET758_1";
            string kaynakYolu = Path.Combine(veriDizini, kaynakDosyaAdı);
            string çıkışYolu = Path.Combine(veriDizini, çıkışDosyaAdı);
            using (var psdImage = (PsdImage)Image.Load(kaynakYolu))
            {
                foreach (var katman in psdImage.Layers)
                {
                    katman.Resize(katman.Width * 5 / 4, katman.Height / 2);
                }

                psdImage.Save(çıkışYolu);
                psdImage.Save(Path.ChangeExtension(çıkışYolu, ".png"), new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-862. Yalnızca bir katman yeniden boyutlandırıldığında vektör yolları olan şekil katmanlarını yeniden boyutlandırma desteği**

{{< highlight csharp >}}
            // Bu örnek, PSD görüntüsündeki bir Vogk ve vektör yol kaynağını yeniden boyutlandırmanın nasıl yapıldığını gösterir
            float scaleX = 0.45f;
            float scaleY = 1.60f;
            string veriDizini = "PSDNET862_1";
            string kaynakDosyaAdı = Path.Combine(veriDizini, "vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaAdı))
            {
                for (int katmanIndex = 1; katmanIndex < image.Layers.Length; katmanIndex++, scaleX += 0.25f, scaleY -= 0.25f)
                {
                    var katman = image.Layers[katmanIndex];
                    var yeniGenişlik = (int)Math.Round(katman.Width * scaleX);
                    var yeniYükseklik = (int)Math.Round(katman.Height * scaleY);
                    katman.Resize(yeniGenişlik, yeniYükseklik);

                    Thread.CurrentThread.CurrentCulture = CultureInfo.CreateSpecificCulture("en-GB");
                    string çıkışAdı = string.Format("yeniden_boyutlandırılmış_{0}_{1}_{2}", katmanIndex, scaleX, scaleY);
                    string çıkışYolu = Path.Combine(veriDizini, çıkışAdı + ".psd");
                    string çıkışPngYolu = Path.Combine(veriDizini, çıkışAdı + ".png");
                    image.Save(çıkışYolu, new PsdOptions(image));
                    image.Save(çıkışPngYolu, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
