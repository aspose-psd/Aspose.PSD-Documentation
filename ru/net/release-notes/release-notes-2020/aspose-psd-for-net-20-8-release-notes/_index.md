---
title: Aspose.PSD для .NET 20.8 - Примечания к выпуску
type: docs
weight: 50
url: /ru/net/aspose-psd-for-net-20-8-release-notes/
---

{{% alert color="primary" %}} 

На этой странице содержатся примечания к [Aspose.PSD для .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-390|Поддержка PlLdResource (ресурс для установленного слоя Smart Object Layer)|Функция|
|PSDNET-400|Поддержка SoLdResource (ресурс данных слоя Smart Object)|Функция|
|PSDNET-693|Добавлена поддержка структур Object Array и Unit Array: подписи ObAr / UnFl|Функция|
|PSDNET-600|Исправление сохранения измененного изображения PSD с цветовым режимом CMYK 16 бит на канал|Ошибка|
|PSDNET-664|Подчеркивание и зачеркивание потеряны после фокусировки на тексте в файле, сохраненном с помощью Aspose.PSD|Ошибка|
|PSDNET-710|Регрессия: Aspose.PSD 20.7.0 нарушает размеры шрифтов для старых файлов|Ошибка|

## **Изменения в общедоступном API**
# **Добавленные API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Structures
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitTypes,System.Double[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.UnitType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Values
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.ValueCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- ...

## **Примеры использования:**
**PSDNET-390. Поддержка PlLdResource (ресурс установленного слоя для слоя Smart Object)**

{{< highlight csharp >}}
        void AssertAreEqual(object actual, object expected)
        {
            var areEqual = object.Equals(actual, expected);
            if (!areEqual && actual is Array && expected is Array)
            {
                var actualArray = (Array)actual;
                var expectedArray = (Array)actual;
                if (actualArray.Length == expectedArray.Length)
                {
                    for (int i = 0; i < actualArray.Length; i++)
...
{{< /highlight >}}
**PSDNET-400. Поддержка SoLdResource (ресурс данных слоя Smart Object)**

{{< highlight csharp >}}
        // This example shows how to get or set the smart object layer data properties of the PSD file.
...
{{< /highlight >}}
**PSDNET-693. Добавлена поддержка структур Object Array и Unit Array: подписи ObAr / UnFl**

{{< highlight csharp >}}
            void AssertAreEqual(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(string.Format("Actual value {0} are not equal to expected {1}.", actual, expected));
                }
            }
...
{{< /highlight >}}
**PSDNET-600. Исправление сохранения измененного изображения PSD с цветовым режимом CMYK 16 бит на канал**

{{< highlight csharp >}}
           using (PsdImage image = (PsdImage)Image.Load("cub16bit_cmyk.psd"))
            {
                RasterCachedImage raster = image.Layers[0];
                Aspose.PSD.Graphics graphics = new Graphics(raster);
                int width = raster.Width;
                int height = raster.Height;
                Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);
                graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1),  rect);
                image.Save("output.png", new PngOptions());
            }
...
{{< /highlight >}}
**PSDNET-664. Потеря подчеркивания и зачеркивания после фокусировки на тексте в файле, сохраненном с помощью Aspose.PSD**

{{< highlight csharp >}}
            string sourceFile = "source.psd";
            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var layers = image.Layers;
                var textLayer = (TextLayer)layers[1];

                textLayer.TextData.Items[0].Style.Underline = true;
                textLayer.TextData.Items[1].Style.Strikethrough = true;

                textLayer.TextData.UpdateLayerData();

                image.Save(outputFile, new PsdOptions(image));
            }
...
{{< /highlight >}}
**PSDNET-710. Регрессия: Aspose.PSD 20.7.0 нарушает размеры шрифтов для старых файлов**

{{< highlight csharp >}}
            string srcFile = "font_size_lost.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[0];
                textLayer.TextData.UpdateLayerData();

                psdImage.Save(outputFilePng, new PngOptions());
            }
...
{{< /highlight >}}```csharp
            string dataDir = "PSDNET693_1\\";
            var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                UnitArrayStructure verticalStructure = null;
                foreach (Layer imageLayer in image.Layers)
                {
                    foreach (var imageResource in imageLayer.Resources)
                    {
                        var resource = imageResource as PlLdResource;
                        if (resource != null && resource.IsCustom)
                        {
                            foreach (OSTypeStructure structure in resource.Items)
                            {
                                if (structure.KeyName.ClassName == "customEnvelopeWarp")
                                {
                                    AssertAreEqual(typeof(DescriptorStructure), structure.GetType());
                                    var custom = (DescriptorStructure)structure;
                                    AssertAreEqual(custom.Structures.Length, 1);
                                    var mesh = custom.Structures[0];
                                    AssertAreEqual(typeof(ObjectArrayStructure), mesh.GetType());
                                    var meshObjectArray = (ObjectArrayStructure)mesh;
                                    AssertAreEqual(meshObjectArray.Structures.Length, 2);
                                    var vertical = meshObjectArray.Structures[1];
                                    AssertAreEqual(typeof(UnitArrayStructure), vertical.GetType());
                                    verticalStructure = (UnitArrayStructure)vertical;
                                    AssertAreEqual(verticalStructure.UnitType, UnitTypes.Pixels);
                                    AssertAreEqual(verticalStructure.ValueCount, 16);

                                    break;
                                }
                            }
                        }
                    }
                }

                AssertAreEqual(true, verticalStructure != null);
            }
```

```csharp
            using (PsdImage image = (PsdImage)Image.Load("cub16bit_cmyk.psd"))
            {
                RasterCachedImage raster = image.Layers[0];
                Aspose.PSD.Graphics graphics = new Graphics(raster);
                int width = raster.Width;
                int height = raster.Height;
                Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);
                graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1),  rect);
                image.Save("output.png", new PngOptions());
            }
```

```csharp
            string sourceFile = "source.psd";
            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var layers = image.Layers;
                var textLayer = (TextLayer)layers[1];

                textLayer.TextData.Items[0].Style.Underline = true;
                textLayer.TextData.Items[1].Style.Strikethrough = true;

                textLayer.TextData.UpdateLayerData();

                image.Save(outputFile, new PsdOptions(image));
            }
```

```csharp
            string srcFile = "font_size_lost.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[0];
                textLayer.TextData.UpdateLayerData();

                psdImage.Save(outputFilePng, new PngOptions());
            }
```