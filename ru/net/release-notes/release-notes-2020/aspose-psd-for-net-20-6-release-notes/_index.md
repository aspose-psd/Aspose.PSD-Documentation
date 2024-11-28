---
title: Aspose.PSD для .NET 20.6 - Примечания к выпуску
type: docs
weight: 70
url: /ru/net/aspose-psd-for-net-20-6-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания к версии [Aspose.PSD для .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-606 |Поддержка ресурса LnkE|Функциональность|
|PSDNET-386 |Поддержка britResource (Ресурс яркости/контраста слоя коррекции)|Функциональность|
|PSDNET-219|Перенос настройки DefaultReplacementFont в класс ImageOptionsBase|Улучшение|
|PSDNET-596|Группа слоев с режимом наложения не PassThrough не отображается|Ошибка|
|PSDNET-610|Исключение NullReference при попытке конвертировать определенный файл Psd в изображение|Ошибка|
|PSDNET-636|Исправление работа изменения размера PSD-файлов, если в слое коррекции есть маска с пустыми границами|Ошибка|
|PSDNET-611|OverflowException при попытке открыть конкретный файл Psd|Ошибка|
|PSDNET-565|Слой изображения Psd с цветовым режимом RGB 16 бит/канал обновляет слои только на экране предварительного просмотра|Ошибка|
|PSDNET-652|Исключение при загрузке конкретного файла PSD с составным ресурсом LnkE и свойством adobeStockLicenseState|Ошибка|
|PSDNET-640|Изменения маски слоя PSD не сохраняются при сохранении|Ошибка|
|PSDNET-593|Сохранение файла AI в формате Jpeg2000 не работает|Ошибка|
|PSDNET-638|Некорректный порядок слоев после добавления группы слоев в пустую группу слоев|Ошибка|

## **Изменения в общедоступном API:**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.MaskRectangle
- P:Aspose.PSD.ImageOptionsBase.DefaultReplacementFont
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Type
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileCreator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.ChildDocId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetModTime
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetLockedState
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.IsLibraryLink
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.HasFileOpenDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Length
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.None
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFD
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFE
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFA
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.Date
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileSize
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FullPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.RelativePath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementRef
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockLicenseState
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.IsEmpty
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.DataSourceCount
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.StringStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String)
# **Удаленные API:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Примеры использования:**
**PSDNET-606. Поддержка ресурса LnkE**

{{< highlight java >}}

 string message = "Пример работы ExampleOfLnkEResourceSupport работает неправильно.";\

void AssertIsTrue(bool condition)\

{\

    if (!condition)\

    {\

        throw new FormatException(message);\

    }\

}\

void AssertAreEqual(object actual, object expected)\

{\

    if (!object.Equals(actual, expected))\

    {\

        throw new FormatException(message);\

    }\

}\

// Этот пример демонстрирует, как получить и установить свойства ресурса Photoshop Psd LnkE, содержащего информацию о внешнем связанном файле.\

void ExampleOfLnkEResourceSupport(\

    string filePath,\

    int length,\

    int length2,\

    int length3,\

    int length4,\

    string fullPath,\

    string date,\

    double assetModTime,\

    string childDocId,\

    bool locked,\

    string uid,\

    string name,\

    string originalFileName,\

    string fileType,\

    long size)\

{\

    string fileName = Path.GetFileName(filePath);\

    string outputPath = @"Output\" + fileName;\

    using (PsdImage image = (PsdImage)Image.Load(filePath))\

    {\

        LnkeResource lnkeResource = null;\

        foreach (var resource in image.GlobalLayerResources)\

        {\

            lnkeResource = resource as LnkeResource;\

            if (lnkeResource != null)\

            {\

                AssertAreEqual(lnkeResource.Length, length);\

                AssertAreEqual(lnkeResource.UniqueId, new Guid(uid));\

                AssertAreEqual(lnkeResource.FullPath, fullPath);\

                AssertAreEqual(lnkeResource.Date.ToString(CultureInfo.InvariantCulture), date);\

                AssertAreEqual(lnkeResource.AssetModTime, assetModTime);\

                AssertAreEqual(lnkeResource.AssetLockedState, locked);\

                AssertAreEqual(lnkeResource.FileName, name);\

                AssertAreEqual(lnkeResource.FileSize, size);\

                AssertAreEqual(lnkeResource.ChildDocId, childDocId);\

                AssertAreEqual(lnkeResource.Version, 7);\

                AssertAreEqual(lnkeResource.FileType, fileType);\

                AssertAreEqual(lnkeResource.FileCreator, string.Empty);\

                AssertAreEqual(lnkeResource.OriginalFileName, originalFileName);\

                AssertAreEqual(lnkeResource.CompId, -1);\

                AssertAreEqual(lnkeResource.OriginalCompId, -1);\

                AssertIsTrue(lnkeResource.HasFileOpenDescriptor);\

                AssertIsTrue(!lnkeResource.IsEmpty);\

                AssertIsTrue(lnkeResource.Type == LinkResourceType.liFE);\

                lnkeResource.FullPath =\

                    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png";\

                AssertAreEqual(lnkeResource.Length, length2);\

                lnkeResource.FileName = "rgb8_2x23.png";\

                AssertAreEqual(lnkeResource.Length, length3);\

                lnkeResource.ChildDocId = Guid.NewGuid().ToString();\

                AssertAreEqual(lnkeResource.Length, length4);\

                lnkeResource.Date = DateTime.Now;\

                lnkeResource.AssetModTime = double.MaxValue;\

                lnkeResource.FileSize = long.MaxValue;\

                lnkeResource.FileType = "test";\

                lnkeResource.FileCreator = "file";\

                lnkeResource.CompId = int.MaxValue;\

                break;\

            }\

        }\

        AssertIsTrue(lnkeResource != null);\

        image.Save(outputPath, new PsdOptions(image));\

    }\

    using (PsdImage image = (PsdImage)Image.Load(outputPath))\

    {\

        image.Save(\

            Path.ChangeExtension(outputPath, "png"),\

            new PngOptions\

            {\

                ColorType = PngColorType.TruecolorWithAlpha\

            });\

    }\

}\

// Этот пример демонстрирует, как получить и установить свойства ресурса Psd LnkE, содержащего информацию о внешнем связанном файле JPEG.\

this.ExampleOfLnkEResourceSupport(\

    @"..\..\..\Issues\IMAGINGNET-2375\photooverlay_5_new.psd",\

    0x21c,\

    0x26c,\

    0x274,\

    0x27c,\

    @"file:///C:/Users/cvallejo/Desktop/photo.jpg",\

    "05/09/2017 22:24:51",\

    0,\

    "F062B9DB73E8D124167A4186E54664B0",\

    false,\

    "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",\

    "photo.jpg",\

    "photo.jpg",\

    "JPEG",\

    0x1520d);\

// Этот пример демонстрирует, как получить и установить свойства ресурса Photoshop Psd LnkE, содержащего информацию обо внешнем связанном PNG-файле.\

this.ExampleOfLnkEResourceSupport(\

    "rgb8_2x2_linked.psd",\

    0x284,\

    0x290,\

    0x294,\

    0x2dc,\

    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",\

    "04/14/2020 14:23:44",\

    0,\

    "",\

    false,\

    "5867318f-3174-9f41-abca-22f56a75247e",\

    "rgb8_2x2.png",\

    "rgb8_2x2.png",\

    "png",\

    0x53);\

// Этот пример демонстрирует, как получить и установить свойства ресурса Psd LnkE содержащего информацию обо внешнем связанном файле библиотеки CC Libraries.\

this.ExampleOfLnkEResourceSupport(\

    "rgb8_2x2_asset_linked.psd",\

    0x398,\

    0x38c,\

    0x388,\

    0x3d0,\

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Feature is available in Photoshop CC 2015)",\

    "01/01/0001 00:00:00",\

    1588890915488.0d,\

    "",\

    false,\

    "ec15f0a8-7f13-a640-b928-7d29c6e9859c",\

    "rgb8_2x2_linked",\

    "rgb8_2x2.png",\

    "png",\

    0);\

{{< /highlight >}}

**PSDNET-201. Поддержка прогресса конвертации документа**

{{< highlight java >}}

 string sourceFilePath = "Apple.psd";\

Stream outputStream = new MemoryStream();\

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)\

{\

      string message = string.Format(\

           "{0} {1}: {2} из {3}",\

           progressInfo.Description,\

           progressInfo.EventType,\

           progressInfo.Value,\

           progressInfo.MaxValue);\

      Console.WriteLine(message);\

};\

Console.WriteLine("---------- Загрузка Apple.psd ----------");\

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };\

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))\

{\

      Console.WriteLine("---------- Сохранение Apple.psd в формат PNG ----------");\

      image.Save(\

           outputStream,\

           new PngOptions()\

           {\

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler\

           });\

      Console.WriteLine("---------- Сохранение Apple.psd в формат PSD ----------");\

      image.Save(\

           outputStream,\

           new PsdOptions()\

           {\

                 ColorMode = ColorModes.Rgb,\

                 ChannelsCount = 4,\

                 ProgressEventHandler = localProgressEventHandler\

           });\

}\

{{< /highlight >}}

**PSDNET-386. Поддержка britResource (Ресурс слоя яркости/контраста)**

{{< highlight java >}}

 /* Этот пример демонстрирует, как можно программно изменить ресурс слоя яркости/контраста изображения PSD - BritResource\

   Это низкоуровневый API Aspose.PSD. Можно использовать слой яркости/контраста через его API, что будет гораздо проще,\

   но прямое редактирование ресурсов PhotoShop дает больший контроль над содержимым файла PSD.  */\

string path = @"BrightnessContrastPS6.psd";\

string outputPath = @"BrightnessContrastPS6_output.psd";\

using (PsdImage im = (PsdImage)Image.Load(path))\

{\

    foreach (var layer in im.Layers)\

    {\

        if (layer is BrightnessContrastLayer)\

        {\

            foreach (var layerResource in layer.Resources)\

            {\

                if (layerResource is BritResource)\

                {\

                    var