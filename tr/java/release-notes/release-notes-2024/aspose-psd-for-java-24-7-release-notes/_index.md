---
title: Aspose.PSD için Java 24.7 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-icin-java-24-7-sürüm-notları/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD için Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) sürümü için sürüm notlarını içermektedir. {{% /alert %}}

| **Anahtar**  | **Özet**                                                                                         | **Kategori** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | AI belgesi açıldığında "Resim yüklenemedi." istisnası                                            | Hata         |
| PSDJAVA-636 | Metin, çıktı PDF dosyalarında yanlış bir şekilde oluşturuldu                                       | Hata         |
| PSDJAVA-637 | Belirtilen dosya için görüntü dışa aktarma başarısız oldu hatası düzeltildi                       | Hata         |
| PSDJAVA-638 | Aspose.Drawing kullanırken yazı tipleri yüklendi                                                   | Hata         |
| PSDJAVA-639 | Büyük JPEG kullanılarak akıllı nesne katmanı oluşturulurken "Aritmetik işlem taşmaya neden oldu" hatası | Hata       |
| PSDJAVA-640 | AI dosyası JPG dosyasına dönüştürülemez                                                           | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**

- Yok

# **Kaldırılan API'ler:**

- Yok 

## **Kullanım örnekleri:**

**PSDJAVA-635. AI belgesi açıldığında "Resim yüklenemedi." hatası**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Metin, çıktı PDF dosyalarında yanlış bir şekilde oluşturuldu**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Belirtilen dosya için görüntü dışa aktarma başarısız oldu hatası düzeltildi**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. Aspose.Drawing kullanılırken yazı tipleri yüklendi**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Güncellemeden önce. Yüklü yazı tipleri sayısı: " + installedFonts.getFamilies().length);
        System.out.println("- Platform: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- 'Arial' için Adobe yazı tipi adını alarak yazı tipi önbelleğini yenileyin: "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Güncellemeden sonra. Yüklü yazı tipleri sayısı: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. Büyük JPEG kullanılarak akıllı nesne katmanı oluşturulurken "Aritmetik işlem taşmaya neden oldu" hatası**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. AI dosyası JPG dosyasına dönüştürülemez**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
