---
title: Aspose.PSD за Java 23.12 - Бележки към версията
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-23-12-belezki-kam-versiyata/
---

{{% alert color="primary" %}} Тази страница съдържа бележки към версията за [Aspose.PSD за Java 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) {{% /alert %}}

| **Ключ**     | **Обобщение**                                                                                         | **Категория** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-565 | [AI Format] Добавяне на поддръжка за визуализация на растрени изображения в новата версия на AI.                             | Функционалност      |
| PSDJAVA-566 | Обработване на градиентен тип Шум в GdflResrource.                                                        | Функционалност      |
| PSDJAVA-567 | Грешка "Обектната връзка не е зададена за екземпляр на обект." при запазване на текстов слой след актуализация. | Грешка          |
| PSDJAVA-568 | Оправяне на ръчното зареждане на шрифтове в MacOS с използване на System.Drawing.Common и Aspose.Drawing.            | Грешка          |
| PSDJAVA-569 | AllowWarpRepaint в PsdLoadOptions води до изключение.                                      | Грешка          |
| PSDJAVA-570 | [AI Format] Внедряване на обработка на потоци с крос-референции.                                        | Подобрение  |
| PSDJAVA-571 | Контрол на лиценза за VectorPathDataResource работи некоректно.                                       | Подобрение  |
| PSDJAVA-574 | Отваряне на всякакъв вид файлове с изображения като вградени умни обекти в изображението на PSD.                                   | Подобрение  |

## **Промени в публичния API**
# **Добавени API:**

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
...

## **Примери за използване:**

** PSDJAVA-565. [AI Format] Добавяне на поддръжка за визуализация на растрени изображения в новата версия на AI **

{{< highlight java >}}

    String sourceFile = "src/main/resources/raster.ai";
    String outputFile = "src/main/resources/raster_output.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

** PSDJAVA-566. Обработване на градиентен тип Шум в GdflResrource **

{{< highlight java >}}

    String sourceFile = "src/main/resources/Gradient-Fill.psd";
    String destFile = "src/main/resources/Gradient-Fill-out.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile, new PsdLoadOptions())) {
        Layer layer = image.getLayers()[1];

        for (LayerResource resource : layer.getResources()) {
            GdFlResource gdFlResource = (GdFlResource) resource;

            if (gdFlResource != null) {
                gdFlResource.setScale(90);
                gdFlResource.setAngle(30);
                gdFlResource.setDither(false);
                gdFlResource.setAlignWithLayer(true);
                gdFlResource.setReverse(false);

                break;
            }
        }
        image.save(destFile, new PsdOptions());
    }

{{< /highlight >}}

** PSDJAVA-567. Грешка "Обектната връзка не е зададена за екземпляр на обект." при запазване на текстов слой след актуализация **

{{< highlight java >}}

    String sourceFile = "src/main/resources/input_1827.psd";
    String outputFile = "src/main/resources/out_1827.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                ((TextLayer) layer).getTextData().updateLayerData();
            }
        }

        // Тук не би трябвало да има грешка
        psdImage.save(outputFile);
    }

{{< /highlight >}}

...

** PSDJAVA-574. Отваряне на всякакъв вид файлове с изображения като вградени умни обекти в изображението на PSD **

{{< highlight java >}}

    String sourceFile = "src/main/resources/empty.psd";

    String addTreeFile = "src/main/resources/tree.psd";
    String addFrostFile = "src/main/resources/frost.png";

    String outputTreeFile = "src/main/resources/tree_export.psd";
    String outputFrostFile = "src/main/resources/frost_export.psd";

    PsdLoadOptions firstPsdLoadOptions = new PsdLoadOptions();
    firstPsdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, firstPsdLoadOptions)) {
        final Stream stream = new FileStream(addTreeFile, FileMode.Open);
        try {
            try (SmartObjectLayer smartLayer = new SmartObjectLayer(stream)) {
                psdImage.addLayer(smartLayer);

                psdImage.save(outputTreeFile, new PsdOptions());
            }
        } finally {
            stream.close();
        }
    }

    PsdLoadOptions secondPsdLoadOptions = new PsdLoadOptions();
    secondPsdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, secondPsdLoadOptions)) {
        final Stream stream = new FileStream(addFrostFile, FileMode.Open);
        try {
            try (SmartObjectLayer smartLayer = new SmartObjectLayer(stream)) {
                psdImage.addLayer(smartLayer);

                psdImage.save(outputFrostFile, new PsdOptions());
            }
        } finally {
            stream.close();
        }
    }

{{< /highlight >}}