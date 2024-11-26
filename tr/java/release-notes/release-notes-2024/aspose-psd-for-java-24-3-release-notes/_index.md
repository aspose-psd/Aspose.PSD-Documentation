---
title: Aspose.PSD for Java 24.3 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-24-3-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 24.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.3/) için sürüm notlarını içerir. {{% /alert %}}

| **Anahtar**  | **Özet**                                                                      | **Kategori** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDJAVA-601 | [AI Format] Büyük çoklu sayfalı AI görüntülerinin yükleme süresini azaltın. | Geliştirme   |
| PSDJAVA-604 | 8 bit'ten 16 bit'e dönüştürülen PSD dosyası okunamaz hale geldi.          | Hata        |
| PSDJAVA-605 | 8 bit'ten 32 bit'e dönüştürülen PSD dosyası okunamaz hale geldi.          | Hata        |
| PSDJAVA-606 | [AI Format] AI dosyasındaki Kısa Eğri render'ını düzelt.                   | Hata        |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**

- T:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.getFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskExtendWithWhite 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskLinked 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isValidAtPosition 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.setFilters(com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter[])
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.updateResourceValues 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.apply(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.applyToMask(com.aspose.psd.fileformats.psd.layers.Layer)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.deepClone 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getBlendMode 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getOpacity 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getSourceDescriptor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.isEnabled 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getAmountNoise 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getDistribution 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setAmountNoise(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setDistribution(int)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setMonochromatic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.isMonochromatic 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer.render(com.aspose.psd.PixelsData)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getRadius 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.setRadius(double)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Gaussian 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Uniform 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getName

# **Kaldırılan API'ler:**

- Hiçbiri

## **Kullanım örnekleri:**

** PSDJAVA-604. PSD dosyası, 8 bit'ten 16 bit'e dönüştürüldükten sonra okunamaz hale geldi**

{{< highlight java >}}

        String kaynakDosya = "src/main/resources/test_smart_layer.psd";
        String çıktıDosyası = "src/main/resources/export.psd";

        try (PsdImage psdImage8 = (PsdImage) Image.load(kaynakDosya)) {
            PsdOptions psdOptions16 = new PsdOptions();
            psdOptions16.setChannelBitsCount((short) 16);

            psdImage8.save(çıktıDosyası, psdOptions16);
        }

        try (PsdImage psdImage16 = (PsdImage) Image.load(çıktıDosyası)) {
            if (psdImage16.getGlobalLayerResources()[0] instanceof Lr16Resource) {
                // sorun yok
            } else {
                throw new Exception("Yanlış global kaynak, ilk kaynak Lr16Resource olmalı");
            }
        }

{{< /highlight >}}

** PSDJAVA-605. PSD dosyası, 8 bit'ten 32 bit'e dönüştürüldükten sonra okunamaz hale geldi**

{{< highlight java >}}

        String kaynakDosya = "src/main/resources/test_smart_layer.psd";
        String çıktıDosyası = "src/main/resources/export.psd";

        try (PsdImage psdImage8 = (PsdImage) Image.load(kaynakDosya)) {
            PsdOptions psdOptions32 = new PsdOptions();
            psdOptions32.setChannelBitsCount((short) 32);

            psdImage8.save(çıktıDosyası, psdOptions32);
        }

        try (PsdImage psdImage8 = (PsdImage) Image.load(çıktıDosyası)) {
            if (psdImage8.getGlobalLayerResources()[0] instanceof Lr32Resource) {
                // sorun yok
            } else {
                throw new Exception("Yanlış global kaynak, ilk kaynak Lr16Resource olmalı");
            }
        }

{{< /highlight >}}

** PSDJAVA-606. [AI Format] Kısa Eğri'nin AI dosyasındaki renderlamasını düzelt**

{{< highlight java >}}

        String kaynakDosya = "src/main/resources/shortCurve.ai";
        String çıktıDosyaYolu = "src/main/resources/shortCurve.png";

        try (AiImage image = (AiImage) Image.load(kaynakDosya)) {
            image.save(çıktıDosyaYolu, new PngOptions());
        }

{{< /highlight >}}
