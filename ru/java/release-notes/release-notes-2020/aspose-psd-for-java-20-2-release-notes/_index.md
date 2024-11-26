---
title: Aspose.PSD для Java 20.2 - Примечания к выпуску
type: docs
weight: 20
url: /ru/java/aspose-psd-for-java-20-2-release-notes/
---

{{% alert color="primary" %}} На данной странице содержатся примечания к выпуску для [Aspose.PSD для Java 20.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDJAVA-96|Улучшение возможности отображения текста различных цветов в текстовом слое|Функциональность|
|PSDJAVA-97|Поддержка ресурса clbl (Ресурс слоя содержит информацию о Blend-обрезке элементов)|Функциональность|
|PSDJAVA-100|Поддержка ресурса blwh (Ресурс содержит данные слоя настройки черного и белого цветов)|Функциональность|
|PSDJAVA-101|Возможность экспорта группы слоев в форматах Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Функциональность|
|PSDJAVA-105|Поддержка ресурса lspf (Содержит настройки о защищенных слоях)|Функциональность|
|PSDJAVA-106|Поддержка ресурса infx (Содержит данные о смешивании внутренних элементов)|Функциональность|
|PSDJAVA-99|Рефакторинг PsdImage и Layer для изменения поведения трансформации (Правильное изменение размера/поворота/обрезки для масок слоев)|Улучшение|
|PSDJAVA-98|В некоторых настройках глобализации растр изображения AI не может быть открыт|Ошибка|
|PSDJAVA-102|После выполнения операции FlipRotate на слое, изображение PSD становится нечитаемым|Ошибка|
|PSDJAVA-103|System.ArgumentException при загрузке файла PSD|Ошибка|
|PSDJAVA-104|После использования метода трансформации только для слоя, сохраненный слой имеет неверные границы или маску|Ошибка|

# **Изменения общедоступного API**
# **Это API временно отключено и будет включено в следующем выпуске:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)

` `**Пожалуйста, используйте v19.4 в промежутке времени, пока у Вас есть соответствующая зависимость.**
# **Добавленные API:**
- M:com.aspose.psd.Color.op_Equality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.Color.op_Inequality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.CustomLineCap.getStrokeCaps(int[],int[])
- M:com.aspose.psd.DisposableObject.finalize
...
... (продолжение аналогично для остальных API)
...

```markdown
...
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleY
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleY(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getMinimalVersion
- M:com.aspose.psd.fileformats.ai.AiDataSection.dispose
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.#ctor(int)
- T:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.#ctor
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuides
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGuides(com.aspose.psd.fileformats.psd.resources.GuideResource[])
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuideCount
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getHeaderVersion
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setHeaderVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleX
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleX(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleY
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleY(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getMinimalVersion
- M:com.aspose.psd.fileformats.ai.AiDataSection.dispose
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.#ctor(int)
- T:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.#ctor
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuides
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGuides(com.aspose.psd.fileformats.psd.resources.GuideResource[])
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuideCount
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getHeaderVersion
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setHeaderVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleX
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleX(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleY
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleY(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getMinimalVersion
- M:com.aspose.psd.fileformats.ai.AiDataSection.dispose
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.#ctor(int)
- T:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.#ctor
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuides
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGuides(com.aspose.psd.fileformats.psd.resources.GuideResource[])
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuideCount
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getHeaderVersion
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setHeaderVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleX
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleX(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleY
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleY(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getMinimalVersion
- M:com.aspose.psd.fileformats.ai.AiDataSection.dispose
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.#ctor(int)
- T:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.#ctor
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuides
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGuides(com.aspose.psd.fileformats.psd.resources.GuideResource[])
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuideCount
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getHeaderVersion
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setHeaderVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleX
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleX(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleY
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleY(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getMinimalVersion
- M:com.aspose.psd.fileformats.ai.AiDataSection.dispose
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.#ctor(int)
- T:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.#ctor
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuides
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGuides(com.aspose.psd.fileformats.psd.resources.GuideResource[])
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuideCount
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getHeaderVersion
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setHeaderVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleX
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleX(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleY
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleY(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getMinimalVersion
- M:com.aspose.psd.fileformats.ai.AiDataSection.dispose

# **Примеры использования:**
...
```