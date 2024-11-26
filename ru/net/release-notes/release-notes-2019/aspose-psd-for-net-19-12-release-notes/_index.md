---
title: Aspose.PSD для .NET 19.12 - Примечания к выпуску
type: docs
weight: 10
url: /ru/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит заметки к выпуску [Aspose.PSD для .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-11|[Поддержка связанных слоев](/ru/psd/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|Функция|
|PSDNET-131|[Поддержка SoCoResource](/ru/psd/net/support-of-socoresource/)|Функция|
|PSDNET-115|Добавление LineBreaks к существующим LineBreaks при обновлении TextLayer текстом|Ошибка|
|PSDNET-157|Замораживание при сохранении PSB в PNG|Ошибка|
|PSDNET-250|Исключение при загрузке CMYK PSD файла без слоев с сжатием RLE|Ошибка|
|PSDNET-161|Исключение при обновлении текстовых слоев|Ошибка|
|PSDNET-222|Некорректная работа изменения размера некоторых PSD файлов с масками слоев|Ошибка|
|PSDNET-244|Сохранение PSD с некоторыми Globalization.CultureInfo.CurrentCulture приводит к исключениям при загрузке|Ошибка|

## **Изменения в публичном API**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **Удаленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Примеры использования:**
**PSDNET-11. Поддержка связанных слоев**

{{< highlight java >}}

        using (var psd = (PsdImage)Image.Load("example.psd"))

...

{{< /highlight >}}

**PSDNET-131. Поддержка SoCoResource**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-115. LineBreaks are added to existing LineBreaks if TextLayer is updated with a string**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-157. Saving PSB as PNG freezing**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-250. Exception on loading CMYK PSD file without layers with RLE compression**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDNET-161. Exception on updating text layers**

{{< highlight java >}}

...

{{< /highlight >}}


**PSDNET-222. Resize some PSD files with layer masks works incorrect**

{{< highlight java >}}

...

{{< /highlight >}}


**PSDNET-244. Saving PSD with some Globalization.CultureInfo.CurrentCulture leads to exceptions on loading**

{{< highlight java >}}

...

{{< /highlight >}}