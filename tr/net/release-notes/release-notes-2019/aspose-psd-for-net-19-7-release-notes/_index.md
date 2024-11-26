---
title: Aspose.PSD için .NET 19.7 - Sürüm Notları
type: docs
weight: 60
url: /tr/net/aspose-psd-for-net-19-7-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD için .NET 19.7](https://www.nuget.org/packages/Aspose.PSD/) sürümü için yayın notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-126|Katman Vektör Maskeleri işleme desteği|Özellik|
|PSDNET-130|PSD dosyaları için doğru Yeniden Boyutlandırma yönteminin uygulanması|Özellik|
|PSDNET-165|PSD'yi PDF'e dışa aktarma desteği eklendi|Özellik|
|PSDNET-186|AI formatının (Sürüm 2 ve 3) diğer formatlara dışa aktarma desteği eklendi|Özellik|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- F:Aspose.PSD.FileFormat.Ai
- T:Aspose.PSD.FileFormats.Ai.AiDataSection
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- T:Aspose.PSD.FileFormats.Ai.AiFinalizeSection
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- T:Aspose.PSD.FileFormats.Ai.AiFormatVersion
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe20
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe30
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf14
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf15
- T:Aspose.PSD.FileFormats.Ai.AiHeader
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Creator
- P:Aspose.PSD.FileFormats.Ai.AiHeader.For
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Title
- P:Aspose.PSD.FileFormats.Ai.AiHeader.CreationDate
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcessColors
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcSets
- P:Aspose.PSD.FileFormats.Ai.AiHeader.BoundingBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.ColorUsage
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TemplateBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TileBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentPreview
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Item(System.String)
- T:Aspose.PSD.FileFormats.Ai.AiImage
- M:Aspose.PSD.FileFormats.Ai.AiImage.#ctor
- P:Aspose.PSD.FileFormats.Ai.AiImage.FileFormat
- P:Aspose.PSD.FileFormats.Ai.AiImage.Version
- P:Aspose.PSD.FileFormats.Ai.AiImage.Header
- P:Aspose.PSD.FileFormats.Ai.AiImage.SetupSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.FinalizeSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.DataSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.IsCached
- P:Aspose.PSD.FileFormats.Ai.AiImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Ai.AiImage.Width
- P:Aspose.PSD.FileFormats.Ai.AiImage.Height
- M:Aspose.PSD.FileFormats.Ai.AiImage.CacheData
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Ai.AiImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.SetPalette(Aspose.PSD.IColorPalette,System.Boolean)
- T:Aspose.PSD.FileFormats.Ai.AiSetupSection
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData
- P:Aspose.PSD.ImageOptions.PdfOptions.PageSize
# **Kaldırılan API'lar:**
- Yok

## **Kullanım örnekleri:**
**PSDNET-126. Katman Vektör Maskeleri işleme desteği**

{{< highlight java >}}

             string sourceFileName = "FarklıKatmanMaskeleri_Kaynak.psd";

            string dışaAktarılacakYol = "FarklıKatmanMaskeleri_DışaAktar.psd";

            string dışaAktarılacakYolPng = "FarklıKatmanMaskeleri_DışaAktar.png";

            // okuma

            using (PsdImage görüntü = (PsdImage)Image.Load(sourceFileName))

            {

                // vektör yol noktalarında değişiklikler yapılması

                foreach (var katman in görüntü.Layers)

                {

                    foreach (var kaynak in katman.Resources)

                    {

                        var kaynak = kaynak as VectorPathDataResource;

                        if (kaynak != null)

                        {

                            foreach (var yolKaydı in kaynak.Paths)

                            {

                                var bezierEğriKaydı = yolKaydı as BezierKnotRecord;

                                if (bezierEğriKaydı != null)

                                {

                                    Point p0 = bezierEğriKaydı.Noktalar[0];

                                    bezierEğriKaydı.Noktalar[0] = bezierEğriKaydı.Noktalar[2];

                                    bezierEğriKaydı.Noktalar[2] = p0;

                                    break;

                                }

                            }

                        }

                    }

                }

                // dışa aktarma

                görüntü.Save(dışaAktarılacakYol);

                görüntü.Save(dışaAktarılacakYolPng, new PngSeçenekleri() { RenkTipi = PngRenkTipi.GerçekRenkAlfa İle });

            }

{{< /highlight >}}

**PSDNET-130. PSD dosyaları için doğru Yeniden Boyutlandırma yönteminin uygulanması**

{{< highlight java >}}

              // PSD dosyaları için doğru Yeniden Boyutlandırma yönteminin uygulanması.

            string sourceFileName = "1.psd";

            string dışaAktarılacakYolPsd = "BoyutlandırmaTesti.psd";

            string exportPathPng = "BoyutlandırmaTesti.png";

            using (RasterImage görüntü = Image.Load(sourceFileName) olarak RasterImage)

            {

                görüntü.Resize(160, 120);

                görüntü.Save(dışaAktarılacakYolPsd, new PsdSeçenekleri());

                görüntü.Save(dışaAktarılacakYolPng, new PngSeçenekleri() { RenkTipi = PngRenkTipi.GerçekRenkAlfa İle });

            }           

{{< /highlight >}}

**PSDNET-165. PSD'yi PDF'e dışa aktarma desteği**

{{< highlight java >}}

   // PSD dışa aktarma desteği PDF

    string[] kaynakDosyalar = yeni string[]

    {

        @"1.psd",

        @"küçük.psb",

        @"psb3.psb",

        @"inRgb16.psd",

        @"FarklıElemanTürleri.psd",

        @"RenkBindirmeVeGölgeVeMask.psd",

        @"ÜçDüzgünKatmanYarıSaydam.psd"

    };

    for (int i = 0; i < kaynakDosyalar.Uzunluk; i++)

    {

        string kaynakDosyaAdı = kaynakDosyalar[i];

        using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaAdı))

        {

           string çıktıDosyaAdı = "PsdToPdf" + i + ".pdf";

           görüntü.Save(çıktıDosyaAdı, yeni PdfSeçenekleri());

        }

    }

{{< /highlight >}}

**PSDNET-186. AI formatının (Sürüm 2 ve 3) diğer formatlara dışa aktarma desteği**

{{< highlight java >}}

 // AI formatının (Sürüm 2 ve 3) diğer formatlara dışa aktarma desteği

            string[] kaynakDosyalar = yeni string[]

            {

                @"34992OStroke",

                @"rect2_color",

            };

            for (int i = 0; i < kaynakDosyalar.Uzunluk; i++)

            {

                string ad = kaynakDosyalar[i];

                string kaynakDosyaAdı = @"testdata\Images\Ai\" + ad + ".ai";

                ImageOptionsBase seçenekler;

                string çıktıDosyaAdı;

                using (AiImage görüntü = (AiImage)Image.Load(kaynakDosyaAdı))

                {

                    çıktıDosyaAdı = ad + ".psd";

                    seçenekler = new PsdSeçenekleri();

                    görüntü.Save(çıktıDosyaAdı, seçenekler);

                    çıktıDosyaAdı = ad + ".png";

                    seçenekler = new PngSeçenekleri() { RenkTipi = PngRenkTipi.GerçekRenkAlfa İle };

                    görüntü.Save(çıktıDosyaAdı, seçenekler);

                    çıktıDosyaAdı = ad + ".jpg";

                    seçenekler = new JpegSeçenekleri() { Kalite = 85 };

                    görüntü.Save(çıktıDosyaAdı, seçenekler);

                    çıktıDosyaAdı = ad + ".gif";

                    seçenekler = new GifSeçenekleri() { RenkPaletiDüzeltmeYap = false };

                    görüntü.Save(çıktıDosyaAdı, seçenekler);

                    çıktıDosyaAdı = ad + ".tif";

                    seçenekler = new TiffSeçenekleri(TiffBeklenenFormat.TiffDeflateRgba);

                    görüntü.Save(çıktıDosyaAdı, seçenekler);

                    çıktıDosyaAdı = ad + ".psd";

                    seçenekler = new PsdSeçenekleri();

                    görüntü.Save(çıktıDosyaAdı, seçenekler);

                }

            }

{{< /highlight >}}
