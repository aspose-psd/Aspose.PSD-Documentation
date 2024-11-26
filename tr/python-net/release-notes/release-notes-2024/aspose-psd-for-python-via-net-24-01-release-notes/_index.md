---
title: Aspose.PSD için Python via .NET 24.1 - Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-icin-python-via-net-24-1-surum-notlari/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için Python via .NET 24.1](https://pypi.org/project/aspose-psd/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                                                  | **Kategori** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [AI Formatı] Çoklu sayfalı AI görüntülerinde temel işleme ekle                                                | Özellik     |
|  PSDPYTHON-22 | Warp Metin Efekti metne uygulanmaz                                                                         | Hata        |
|  PSDPYTHON-23 | Belirli bir dosyadaki maskenin yanlış işlenmesi                                                             | Hata        |
|  PSDPYTHON-24 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor'da NullReferenceException               | Hata        |
|  PSDPYTHON-25 | [AI Formatı] AiExporterUtils'ta bellek kullanımını düzelt                                                    | Hata        |



## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Kaldırılan API'ler:**
- Yok


## **Kullanım örnekleri:**

**PSDPYTHON-19. [AI Formatı] Çoklu sayfalı AI görüntülerinde temel işleme ekle**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # AI görüntüsünü yükle.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Varsayılan olarak, ActivePageIndex 0'dır.
            # Bu özelliği değiştirmeden AI görüntüsünü kaydederseniz, ilk sayfa render edilir ve kaydedilir.
            image.save(firstPageOutputPng, PngOptions())

            # Aktif sayfa indeksini ikinci sayfaya değiştir.
            image.active_page_index = 1

            # AI görüntüsünün ikinci sayfasını PNG görüntüsü olarak kaydedin.
            image.save(secondPageOutputPng, PngOptions())

            # Aktif sayfa indeksini üçüncü sayfaya değiştir.
            image.active_page_index = 2

            # AI görüntüsünün üçüncü sayfasını PNG görüntüsü olarak kaydedin.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Warp Metin Efekti metne uygulanmaz**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. Belirli bir dosyadaki maskenin yanlış işlenmesi**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor'da NullReferenceException**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI Formatı] AiExporterUtils'ta bellek kullanımını düzelt**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # C# Bellek kullanımı 220'dir, ancak python için GC etkinliklerine doğrudan erişimimiz yok.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # AI görüntüsünü yükle.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # AI görüntüsünün ilk sayfasını bir PNG görüntüsü olarak kaydedin.
            image.save(firstPageOutputPng, pngOpt)

            # Aktif sayfa indeksini ikinci sayfaya değiştir.
            image.active_page_index = 1

            # AI görüntüsünün ikinci sayfasını bir PNG görüntüsü olarak kaydedin.
            image.save(secondPageOutputPng, pngOpt)

            # Aktif sayfa indeksini üçüncü sayfaya değiştir.
            image.active_page_index = 2

            # AI görüntüsünün üçüncü sayfasını bir PNG görüntüsü olarak kaydedin.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Bellek kullanımı çok fazla. {:.1f}'dan fazla {}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}
