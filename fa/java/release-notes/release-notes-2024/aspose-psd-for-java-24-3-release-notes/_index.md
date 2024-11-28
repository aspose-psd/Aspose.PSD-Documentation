---
title: دفاتر توضیحات Aspose.PSD برای Java 24.3
type: مستندات
weight: 40
url: /fa/java/aspose-psd-for-java-24-3-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل دفاتر توضیحات برای [Aspose.PSD برای Java 24.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.3/) می‌باشد {{% /alert %}}

| **کلید**    | **خلاصه**                                                      | **دسته**     |
|:-----------|:----------------------------------------------------------------|:-------------|
| PSDJAVA-601 | [فرمت AI] کاهش زمان بارگذاری تصاویر AI چندصفحه بزرگ.       | بهبود        |
| PSDJAVA-604 | بعد از تبدیل PSD از 8 بیت به 16 بیت، پرونده غیرقابل خواندن شد. | باگ          |
| PSDJAVA-605 | بعد از تبدیل PSD از 8 بیت به 32 بیت، پرونده غیرقابل خواندن شد. | باگ          |
| PSDJAVA-606 | [فرمت AI] رفع رندرینگ خط کوتاه در پرونده AI.                 | باگ          |

## **تغییرات API عمومی**
# **API های اضافه شده:**

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

# **API های حذف شده:**

- هیچکدام

## **مثال‌های استفاده:**

**PSDJAVA-604. پرونده PSD بعد از تبدیل از 8 بیت به 16 بیت، غیرقابل خواندن شد**

{{< highlight java >}}

        String sourceFile = "src/main/resources/test_smart_layer.psd";
        String outputFile = "src/main/resources/export.psd";

        try (PsdImage psdImage8 = (PsdImage) Image.load(sourceFile)) {
            PsdOptions psdOptions16 = new PsdOptions();
            psdOptions16.setChannelBitsCount((short) 16);

            psdImage8.save(outputFile, psdOptions16);
        }

        try (PsdImage psdImage16 = (PsdImage) Image.load(outputFile)) {
            if (psdImage16.getGlobalLayerResources()[0] instanceof Lr16Resource) {
                // اوکی است
            } else {
                throw new Exception("منبع سراسری اشتباه است، منبع اول باید Lr16Resource باشد");
            }
        }

{{< /highlight >}}

**PSDJAVA-605. پرونده PSD بعد از تبدیل از 8 بیت به 32 بیت، غیرقابل خواندن شد**

{{< highlight java >}}

        String sourceFile = "src/main/resources/test_smart_layer.psd";
        String outputFile = "src/main/resources/export.psd";

        try (PsdImage psdImage8 = (PsdImage) Image.load(sourceFile)) {
            PsdOptions psdOptions32 = new PsdOptions();
            psdOptions32.setChannelBitsCount((short) 32);

            psdImage8.save(outputFile, psdOptions32);
        }

        try (PsdImage psdImage8 = (PsdImage) Image.load(outputFile)) {
            if (psdImage8.getGlobalLayerResources()[0] instanceof Lr32Resource) {
                // اوکی است
            } else {
                throw new Exception("منبع سراسری اشتباه است، منبع اول باید Lr16Resource باشد");
            }
        }

{{< /highlight >}}

**PSDJAVA-606. [فرمت AI] رفع مشکل رندرینگ خط کوتاه در پرونده AI**

{{< highlight java >}}

        String sourceFile = "src/main/resources/shortCurve.ai";
        String outputFilePath = "src/main/resources/shortCurve.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}
