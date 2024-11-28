---
title: Aspose.PSD for Java 23.12 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-23-12-release-notes/
---

{{% alert renk="primary" %}} Bu sayfa, [Aspose.PSD for Java 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) için sürüm notlarını içerir. {{% /alert %}}

| **Anahtar**  | **Özet**                                                                                              | **Kategori**  |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-565 | [AI Format] Yeni AI sürümünde Raster Görüntü oluşturma desteği eklendi.                              | Özellik      |
| PSDJAVA-566 | GdflResrource'daki Gradyan türü Gürültüyü işle.                                                       | Özellik      |
| PSDJAVA-567 | Metin Katmanı Güncellemeden Sonra "Nesne başvurusu bir örneğe ayarlanmadı" hatası.                   | Hata         |
| PSDJAVA-568 | MacOS'ta System.Drawing.Common ve Aspose.Drawing kullanarak yazı tiplerinin manuel yüklenmesini düzeltin. | Hata         |
| PSDJAVA-569 | PsdLoadOptions'daki AllowWarpRepaint, istisnaya yol açar.                                            | Hata         |
| PSDJAVA-570 | [AI Format] Çapraz referans akışlarının işlenmesini uygula.                                          | İyileştirme  |
| PSDJAVA-571 | VectorPathDataResource için Lisans Kontrolü yanlış çalışır.                                           | İyileştirme  |
| PSDJAVA-574 | PSD görüntüsünde gömülü akıllı nesne olarak herhangi bir görüntü dosyasını açın.                      | İyileştirme  |

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setColorModel(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setGradientMode(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setUseVectorColor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.#ctor(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent1
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent2
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent3
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent4 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorSpace 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getFlag 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getKey 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getLength 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getOpacity 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getPsdVersion 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getSignature 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent1(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent2(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent3(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent4(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorSpace(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setOpacity(short)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.TypeToolKey 
- T:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.CMYK 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.GrayScale 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.HSB 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.Lab 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB 
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getColorModel 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMaximumColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMinimumColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRndNumberSeed 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRoughness 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getShowTransparency 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setColorModel(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setUseVectorColor(boolean)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientNoise 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientSolid 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelHSB 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelLAB 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelRGB 
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAlignWithLayer 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAngle 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientMode 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getHorizontalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getReverse 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getScale 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getVerticalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setVerticalOffset(double)

# **Kaldırılan API'lar:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getHorizontalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getReverse 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getScale 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getVerticalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setVerticalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColorPoints 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientName 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getTransparencyPoints 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColorPoints(com.aspose.psd.fileformats.psd.layers.IGradientColorPoint[])
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setTransparencyPoints(com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint[])
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

## **Kullanım örnekleri:**

** PSDJAVA-565. [AI Format] Yeni sürümde Raster Görüntü oluşturma desteği eklendi **

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/raster.ai";
    String çıktıDosyası = "src/main/resources/raster_output.png";

    try (AiImage görüntü = (AiImage) Image.load(kaynakDosya)) {
        görüntü.save(çıktıDosyası, new PngOptions());
    }

{{< /highlight >}}

** PSDJAVA-566. GdflResrource'daki Gradyan türü Gürültüyü işle **

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/Gradient-Fill.psd";
    String hedefDosya = "src/main/resources/Gradient-Fill-out.psd";

    try (PsdImage görüntü = (PsdImage) Image.load(kaynakDosya, new PsdLoadOptions())) {
        Layer katman = görüntü.getLayers()[1];

        for (LayerResource kaynak : katman.getResources()) {
            GdFlResource gdFlKaynak = (GdFlResource) kaynak;

            if (gdFlKaynak != null) {
                gdFlKaynak.setScale(90);
                gdFlKaynak.setAngle(30);
                gdFlKaynak.setDither(false);
                gdFlKaynak.setAlignWithLayer(true);
                gdFlKaynak.setReverse(false);

                break;
            }
        }
        görüntü.save(hedefDosya, new PsdOptions());
    }

{{< /highlight >}}

** PSDJAVA-567. "Nesne başvurusu bir örneğe ayarlanmadı" hatası metin katmanını güncelleme sırasında **

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/input_1827.psd";
    String çıktıDosyası = "src/main/resources/out_1827.psd";

    try (PsdImage psdGörüntü = (PsdImage) Image.load(kaynakDosya)) {
        for (Layer katman : psdGörüntü.getLayers()) {
            if (katman instanceof TextLayer) {
                ((TextLayer) katman).getTextData().updateLayerData();
            }
        }

        // Burada hata olmamalı
        psdGörünt