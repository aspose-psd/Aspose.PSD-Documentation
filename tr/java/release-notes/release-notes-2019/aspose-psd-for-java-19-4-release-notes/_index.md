---
title: Aspose.PSD for Java 19.4 - Sürüm Notları
type: docs
weight: 20
url: /tr/java/aspose-psd-for-java-19-4-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, Aspose.PSD için Java 19.4 sürümüne ilişkin sürüm notlarını içerir

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-1|JPEG/PNG/vb. görüntü dosyalarını doğrudan yüklemeden PsdImage'e yükleme özelliği ekleyin (Aspose.PSD tarafından desteklenmeyen)|Özellik|
|PSDJAVA-2|Renkli 16 bit/kanal (renk başına 64 bit) ile RGB Renk modunu destekleme|Özellik|
|PSDJAVA-3|Katman Vektör Maskelerinin ve Metin Katmanı Özel Döndürme/Döndürme işlemlerinin desteklenmesi|Özellik|
|PSDJAVA-4|Tüm Asya karakterleri düzgün şekilde oluşturulmamıştır|Hata|
|PSDJAVA-5|\r\n sembolleri çift satır aralığı olarak yorumlanır ki bu yanlıştır|Hata|
|PSDJAVA-6|Metin Katmanı, Satır Kesmeleri içeren dize ile güncellenirse PSD Dosyası okunamaz hale gelir|Hata|
|PSDJAVA-7|Metin Katmanı, Sekmeler sembolleri içeren dize ile güncellenirse işleme istisna ile başarısız olur|Hata|

# **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **Kaldırılan API'ler:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- ...

# **Kullanım Örnekleri:**

**PSDJAVA-1. JPEG/PNG/vb. görüntü dosyalarını doğrudan yüklemeden PsdImage'e yükleme özelliği ekleyin (Aspose.PSD tarafından desteklenmeyen)**

{{< highlight java >}}

 String dosyaYolu = "PsdOrnegi.psd";

    String çıktıDosyaYolu = "PsdSonucu.psd";

    PsdImage görüntü = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(dosyaYolu);

         try 

         {

              Layer katman = null;

              try

              {

                  katman = new Layer((RasterImage)im);

                  görüntü.addLayer(katman);

                  görüntü.save(çıktıDosyaYolu);

              }

              catch

              {

                  if (katman != null)

                  {

                       katman.dispose();

                  }

                  throw;

              }

         }    

         finally 
         {
              im.dispose(); 
         }
    }

    finally

    {

         görüntü.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. Renkli 16 bit/kanal (renk başına 64 bit) ile RGB Renk modunu destekleme**

{{< highlight java >}}

  // Renkli 16 bit/kanal (renk başına 64 bit) ile RGB Renk modunu destekleme

        String sourceFileName = "inRgb16.psd.psd";

        String outputFilePathJpg = "outRgb16.jpg";

        String outputFilePathPsd = "outRgb16.psd";

        PsdLoadOptions options = new PsdLoadOptions();

        PsdImage image = (PsdImage)Image.load(sourceFileName, options);

        try

        {

            PsdOptions psdOpt = new PsdOptions(image);

            image.save(outputFilePathPsd, psdOpt);
...

{{< /highlight >}}

**PSDJAVA-3. Katman Vektör Maskelerinin ve Metin Katmanı Özel Döndürme/Döndürme işlemlerinin desteklenmesi**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-4. Tüm Asya karakterleri düzgün şekilde oluşturulmamıştır**

...

**PSDJAVA-5. \r\n sembolleri çift satır aralığı olarak yorumlanır ki bu yanlıştır**

...

**PSDJAVA-6. Metin Katmanı, Satır Kesmeleri içeren dize ile güncellenirse PSD Dosyası okunamaz hale gelir**

...

**PSDJAVA-7. If TextLayer is updated with string which contains Tabs symbols, processing fails with exception**

...