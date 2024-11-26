---
title: Aspose.PSD для .NET 20.7 - Примечания к выпуску
type: docs
weight: 60
url: /ru/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-673|Поддержка ресурса LnkE|Функция|
|PSDNET-392|Поддержка britResource (ресурс яркости/контраста слоя коррекции)|Функция|
|PSDNET-629|Изменение сообщения об ошибке при попытке открыть не поддерживаемые форматы как изображение|Улучшение|
|PSDNET-594|Не удалось сохранить маску слоя|Ошибка|
|PSDNET-597|При сохранении файла PSD после создания новой группы слоев получается предупреждение Photoshop при открытии файла|Ошибка|
|PSDNET-618|Обрезка маски не применяется к папке|Ошибка|
|PSDNET-625|Невозможно открыть файл с помощью Aspose.PSD для .NET|Ошибка|
|PSDNET-650|Исключение при сохранении изображения при конвертации PSD в PDF|Ошибка|
|PSDNET-655|Операция rop делает недопустимым путь обрезки в изображении PSD|Ошибка|
|PSDNET-662|Исключение NullReference при попытке сохранить конкретный файл PSD с эффектом тени|Ошибка|
|PSDNET-666|Aspose.PSD возвращает true на Image.CanLoad(pdfStream)|Ошибка|
|PSDNET-676|Слои не отображаются в созданном PNG|Ошибка|
|PSDNET-677|Исключение при доступе к TextData|Ошибка|
|PSDNET-679|ImageSaveException при сохранении PSD|Ошибка|

## **Изменения в публичном API**
# **Добавлены API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **Удаленные API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Примеры использования:**
**PSDNET-606. Поддержка ресурса LnkE**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-201. Поддержка прогресса конвертации документов**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-386. Поддержка britResource (ресурс яркости/контраста слоя коррекции)**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-596. Группа слоев с непрозрачным режимом наложения не отображается**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-610. Исключение при попытке преобразовать определенный файл Psd в изображение**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-636. Некорректное изменение размера файлов PSD, если на слое коррекции есть маска с пустыми границами**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-611. OverflowException при попытке открыть определенный файл Psd**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-565. Psd Image с режимом RGB 16 бит/канал обновляет слои только на предварительном просмотре**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-652. Исключение при загрузке определенного файла PSD с составным ресурсом LnkE и свойством adobeStockLicenseState**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDNET-638. Неверный порядок слоев после добавления группы слоев в пустую группу слоев**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}

**PSDBET-219. Перенос настройки DefaultReplacementFont в класс ImageOptionsBase**

{{< highlight csharp >}}
// Здесь приведен пример использования
{{< /highlight >}}