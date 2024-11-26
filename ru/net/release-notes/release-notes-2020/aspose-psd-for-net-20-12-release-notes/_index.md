---
title: Aspose.PSD for .NET 20.12 - Примечания к выпуску
type: docs
weight: 10
url: /ru/net/aspose-psd-for-net-20-12-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к выпуску [Aspose.PSD для .NET 20.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Сводка**|**Категория**|
| :- | :- | :- |
|PSDNET-757|Поддержка преобразования слоев в слой смарт-объекта|Функция|
|PSDNET-764|Метод SmartObjectLayer.ReplaceContents вызывает исключение NullReferenceException при попытке добавить файл PSB|Ошибка|
|PSDNET-773|Некорректное отображение изображений CMYK 8-бит и CMYK 16-бит, если слой больше холста|Ошибка|
|PSDNET-782|Сохраненный файл PSB можно открыть с помощью нашего API, но не получается сделать это с помощью Photoshop|Ошибка|
|PSDNET-783|При попытке изменить умный слой в конкретном PSD с общим источником данных мы получаем исключение|Ошибка|
|PSDNET-172|Переименование FileFormatVersion в PsdVersion для избежания путаницы|Улучшение|
|PSDNET-620|Удаление конфигурации Compact framework из Aspose.PSD .NET|Улучшение|
|PSDNET-765|PsdImageException: Неизвестный заголовок ресурса при попытке открыть файл PSB с SmartObjectLayers|Улучшение|
|PSDNET-798|Перенос Иерархии Классов Векторной Маски в Пространство Имен Ядра для обеспечения единообразия с продуктами Aspose.PSD и Aspose.Imaging|Улучшение|

## **Изменения в публичном API**
# **Добавленные API:**
- T:Aspose.PSD.FileFormats.Psd.PsdVersion
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.PsdVersion
- T:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor(System.Byte[])
...
(продолжение в уведомлении)