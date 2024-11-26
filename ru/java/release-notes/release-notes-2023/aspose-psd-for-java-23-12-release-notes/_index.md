---
title: Релизные заметки Aspose.PSD для Java 23.12
type: docs
weight: 40
url: /ru/java/aspose-psd-for-java-23-12-release-notes/
---

{{% alert color="primary" %}} Эта страница содержит релизные заметки для [Aspose.PSD для Java 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) {{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                                  | **Категория** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-565 | [Формат AI] Добавлена поддержка растрового изображения в новой версии AI.                            | Функция       |
| PSDJAVA-566 | Обработка шума типа Gradient в GdflResrource.                                                       | Функция       |
| PSDJAVA-567 | Ошибка "Ссылка на объект не установлена на экземпляр объекта" при сохранении слоя текста после обновления. | Ошибка        |
| PSDJAVA-568 | Исправлена ручная загрузка шрифтов на MacOS с использованием System.Drawing.Common и Aspose.Drawing. | Ошибка        |
| PSDJAVA-569 | AllowWarpRepaint в PsdLoadOptions приводит к исключению.                                           | Ошибка        |
| PSDJAVA-570 | [Формат AI] Реализация обработки потоков кросс-ссылок.                                             | Улучшение     |
| PSDJAVA-571 | Управление лицензией для VectorPathDataResource работает некорректно.                                | Улучшение     |
| PSDJAVA-574 | Открывайте любой файл изображения как встроенный умный объект в изображении PSD.                    | Улучшение     |

## **Изменения в общедоступном API**
# **Добавленные API:**

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
- и т.д.

# **Удаленные API:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.и т.д.

## **Примеры использования:**

** PSDJAVA-565. [Формат AI] Добавить поддержку растрового изображения в новой версии AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/raster.ai";
    String outputFile = "src/main/resources/raster_output.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

и т.д.