---
title: Catatan Rilis Aspose.PSD untuk Java 23.12
type: docs
weight: 40
url: /id/java/aspose-psd-for-java-23-12-release-notes/
---

{{% alert color="primary" %}} Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Java 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) {{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                        | **Kategori** |
|:-----------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-565 | [Format AI] Menambahkan dukungan untuk merender Gambar Raster dalam versi baru AI.                    | Fitur        |
| PSDJAVA-566 | Menangani Tipe Gradient Noise dalam GdflResrource.                                                    | Fitur        |
| PSDJAVA-567 | Kesalahan "Object reference not set to an instance of an object." saat menyimpan Lapisan Teks Setelah Diperbarui. | Bug          |
| PSDJAVA-568 | Memperbaiki pengambilan manual font pada MacOS menggunakan System.Drawing.Common dan Aspose.Drawing.   | Bug          |
| PSDJAVA-569 | AllowWarpRepaint dalam PsdLoadOptions menyebabkan pengecualian.                                      | Bug          |
| PSDJAVA-570 | [Format AI] Mengimplementasikan pemrosesan aliran referensi silang.                                    | Peningkatan  |
| PSDJAVA-571 | Lisensi Kontrol untuk VectorPathDataResource tidak berfungsi dengan benar.                           | Peningkatan  |
| PSDJAVA-574 | Membuka berkas gambar apa pun sebagai objek pintar yang disematkan dalam gambar PSD.                  | Peningkatan  |

## **Perubahan API Publik**
# **API Ditambahkan:**

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

# **API Dihapus:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
  M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getHorizontalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getReverse 
- M:com.aspose.psd.fileformats