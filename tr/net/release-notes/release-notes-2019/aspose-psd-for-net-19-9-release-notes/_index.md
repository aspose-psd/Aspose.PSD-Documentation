---
title: Aspose.PSD for .NET 19.9 - Sürüm Notları
type: docs
weight: 40
url: /tr/net/aspose-psd-for-net-19-9-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-160|Çıkarılan yanlış katman adı|Özellik|
|PSDNET-175|PSD TextLayer içinde farklı bir metin bölgesinden metin özelliklerinin alınması|Özellik|
|PSDNET-190|Katman grubu ekleme desteği|Özellik|
|PSDNET-192|Derece Dolgu Katmanı için Ölçek Özelliği Desteği|Özellik|
|PSDNET-162|Parlaklığı Ayarlama|Geliştirme|
|PSDNET-174|PSD görüntüsünü JPEG olarak kaydederken IndexOutOfRangeException|Hata|
|PSDNET-180|Metin katmanı metnini güncelleme hata fırlatıyor|Hata|
|PSDNET-182|RotateFlip işleminden sonra PSD görüntüsünün kaydedilmesi, açılamayan bozuk bir dosya oluşturur|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**
**PSDNET-160. Yanlış katman adı çıkarıldı**

Katman adını doğru bir şekilde görüntülemek için **DisplayName** özelliğini kullanın. Bu özelliğe artık bir setter eklendi ve özellik değiştirilebilir hale geldi. Photoshop, Kore karakterlerini ASCII içinde byte 63' '?' olarak sakladığında, ad özelliğini kullanarak katman adının kaydedilmesi durumunda. Kore karakterlerini desteklemediği için **DisplayName** özelliğini kullanın.

{{< highlight java >}}

             // katman adlarında değişiklikler yapın ve kaydedin

            using (var görüntü = (PsdImage)Image.Load("adları olan katmanlar.psd"))

            {

                for (int i = 0; i < görüntü.Katmanlar.Uzunluk; i++)

                {

                    var katman = görüntü.Katmanlar[i];

                    // DisplayName özelliğine yeni değer atayın

                    katman.DisplayName += "_değiştirildi";

                }

                görüntü.Kaydet("çıktı.psd");

            }

{{< /highlight >}}

**PSDNET-175. PSD TextLayer içinde farklı bir metin bölgesinden metin özelliklerinin alınması**

{{< highlight java >}}

            const double Tolerans = 0.0001;

            var dosyaYolu = "ThreeColorsParagraphs.psd";

            var çıktıYolu = "ThreeColorsParagraph_out.psd";

            using (var görüntü = (PsdImage)Image.Load(dosyaYolu))

            {

                for (int i = 0; i < görüntü.Katmanlar.Uzunluk; i++) 

                {

                    var katman = görüntü.Katmanlar[i] olarak TextLayer;

                    if (katman != null)

                    {

                        var kısımlar = katman.TextData.Items;

                        if (kısımlar.Uzunluk != 4)

                        {

                            throw new Exception();

                        }

                        // Her parçanın metninin kontrol edilmesi

                        if (kısımlar[0].Text != "Eski " ||

                            kısımlar[1].Text != "renk" ||

                            kısımlar[2].Text != " metin\r" ||

                            kısımlar[3].Text != "İkinci paragraf\r")

                        {

                            throw new Exception();

                        }

                        // Paragrafların verilerinin kontrol edilmesi

                        // Paragraflar farklı hizalamalara sahip

                        if (

                            kısımlar[0].Paragraph.Justification != 0 ||

                            kısımlar[1].Paragraph.Justification != 0 ||

                            kısımlar[2].Paragraph.Justification != 0 ||

                            kısımlar[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // İlk ve ikinci paragrafın diğer tüm özellikleri eşit

                        for (int j = 0; j < kısımlar.Uzunluk; j++)

                        {

                            var paragraf = kısımlar[j].Paragraph;

                            if (Math.Abs(paragraf.AutoLeading - 1.2) > Tolerans ||

                                 paragraf.AutoHyphenate != false ||

                                 paragraf.Burasagari != false ||

                                 paragraf.ConsecutiveHyphens != 8 ||

                                 Math.Abs(paragraf.StartIndent) > Tolerans ||

                                 Math.Abs(paragraf.EndIndent) > Tolerans ||

                                 paragraf.EveryLineComposer != false ||

                                 Math.Abs(paragraf.FirstLineIndent) > Tolerans ||

                                 paragraf.GlyphSpacing.Uzunluk != 3 ||

                                 Math.Abs(paragraf.GlyphSpacing[0] - 1) > Tolerans ||

                                 Math.Abs(paragraf.GlyphSpacing[1] - 1) > Tolerans ||

                                 Math.Abs(paragraf.GlyphSpacing[2] - 1) > Tolerans ||

                                 paragraf.Hanging != false ||

                                 paragraf.HyphenatedWordSize != 6 ||

                                 paragraf.KinsokuOrder != 0 ||

                                 paragraf.LetterSpacing.Uzunluk != 3 ||

                                 Math.Abs(paragraf.LetterSpacing[0]) > Tolerans ||

                                 Math.Abs(paragraf.LetterSpacing[1]) > Tolerans ||

                                 Math.Abs(paragraf.LetterSpacing[2]) > Tolerans ||

                                 paragraf.LeadingType != LeadingMode.Auto ||

                                 paragraf.PreHyphen != 2 ||

                                 paragraf.PostHyphen != 2 ||

                                 Math.Abs(paragraf.SpaceBefore) > Tolerance ||

                                 Math.Abs(paragraf.SpaceAfter) > Tolerance ||

                                 paragraf.WordSpacing.Uzunluk != 3 ||

                                 Math.Abs(paragraf.WordSpacing[0] - 0.8) > Tolerance ||

                                 Math.Abs(paragraf.WordSpacing[1] - 1.0) > Tolerance ||

                                 Math.Abs(paragraf.WordSpacing[2] - 1.33) > Tolerance ||

                                 Math.Abs(paragraf.Zone - 36.0) > Tolerance)

                            {

                                throw new Exception();

                            }

                        }

                         // Stil verilerinin kontrol edilmesi

                         // Stiller farklı renklere ve font boyutlarına sahip

                         if (Math.Abs(kısımlar[0].Style.FontSize - 12) > Tolerans ||

                             Math.Abs(kısımlar[1].Style.FontSize - 12) > Tolerans ||

                             Math.Abs(kısımlar[2].Style.FontSize - 12) > Tolerance ||

                             Math.Abs(kısımlar[3].Style.FontSize - 10) > Tolerance)

                         {

                             throw new Exception();

                         }

                         if (kısımlar[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                             kısımlar[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                             kısımlar[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                             kısımlar[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                         {

                             throw new Exception();

                         }

                         for (int j = 0; j < kısımlar.Uzunluk; j++) 

                         {

                             var stil = kısımlar[j].Style;

                             if (stil.AutoLeading != false ||

                                 stil.HindiNumbers != false ||

                                 stil.Kerning != 0 ||

                                 stil.Leading != 0 ||

                                 stil.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                 stil.Tracking != 50)

                             {

                                 throw new Exception();

                             }

                        }

                         // Metin düzenleme örneği

                         kısımlar[0].Text = "Merhaba ";

                         kısımlar[1].Text = "Dünya";

                         // Metin parçalarının çıkarılması örneği

                         katman.TextData.RemovePortion(3);

                         katman.TextData.RemovePortion(2);

                         // Yeni metin parçası ekleme örneği

                         var oluşturulanParça = katman.TextData.ProducePortion();

                         oluşturulanParça.Text = "!!!\r";

                         katman.TextData.AddPortion(oluşturulanParça);

                         kısımlar = katman.TextData.Items;

                         // Parçalar için paragraf ve stil düzenleme örneği

                         // Doğru hizalamayı ayarlayın

                         kısımlar[0].Paragraph.Justification = 1;

                         kısımlar[1].Paragraph.Justification = 1;

                         kısımlar[2].Paragraph.Justification = 1;

                         // Her stil için farklı renkler. Değişecek, ancak render tam olarak desteklenmiyor

                         kısımlar[0].Style.FillColor = Color.Aquamarine;

                         kısımlar[1].Style.FillColor = Color.Violet;

                         kısımlar[2].Style.FillColor = Color.LightBlue;

                         // Farklı font. Değişecek, ancak render tam olarak desteklenmiyor

                         kısımlar[0].Style.FontSize = 6;

                         kısımlar[1].Style.FontSize = 8;

                         kısımlar[2].Style.FontSize = 10;

                         katman.TextData.UpdateLayerData();

                         görüntü.Save(çıktıYolu, new PsdOptions(görüntü));

                         break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Katman grubu ekleme desteği**

{{< highlight java >}}

             // -Grup 1

             // --Katman 1

             // --Grup 2

             // ---Katman 2

             // ---Katman 3

             // --Katman 4

             string veriDizini = "psdnet190_test.psd";

             var oluşturSeçenekler = new PsdOptions();

             oluşturSeçenekler.Source = new FileCreateSource(veriDizini, false);

             oluşturSeçenekler.Palette = new PsdColorPalette(new Color[] { Color.Green });

             using (var psdGörüntü = (PsdImage)Image.Create(oluşturSeçenekler, 500, 500))

             {

                 LayerGroup grup1 = psdGörüntü.AddLayerGroup("Grup 1", 0, true);

                 Layer katman1 = new Layer(psdGörüntü);

                 katman1.Name = "Katman 1";

                 grup1.AddLayer(katman1);

                 LayerGroup grup2 = grup1.AddLayerGroup("Grup 2", 1);

                 Layer katman2 = new Layer(psdGörüntü);

                 katman2.Name = "Katman 2";

                 grup2.AddLayer(katman2);

                 Layer katman3 = new Layer(psdGörüntü);

                 katman3.Name = "Katman 3";

                 grup2.AddLayer(katman3);

                 Layer katman4 = new Layer(psdGörüntü);

                 katman4.Name = "Katman 4";

                 grup1.AddLayer(katman4);

                 psdGörüntü.Save();

             }

{{< /highlight >}}

**PSDNET-192. Derece Dolgu Katmanı için Ölçek Özelliği Desteği**

{{< highlight java >}}

             using (var image = (PsdImage)Image.Load("Fill