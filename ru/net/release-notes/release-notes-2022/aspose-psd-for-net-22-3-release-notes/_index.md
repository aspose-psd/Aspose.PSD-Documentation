---
title: Aspose.PSD для .NET 22.3 - Примечания к выпуску
type: docs
weight: 100
url: /ru/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-210|Добавлено свойство IsOpen для группы слоев|Функция|
|PSDNET-643|Изображение PSD с растровыми масками слоя теряет маски при сохранении в изображение PSD с 16 битами|Ошибка|
|PSDNET-899|Режим смешивания Dissolve не применяется к папке с маской|Ошибка|
|PSDNET-1047|Конкретный файл не может быть открыт в Photoshop после сохранения в Aspose.PSD 21.11|Ошибка|
|PSDNET-1068|Неправильное отображение слоя с режимом наложения Linear Dodge (Add)|Ошибка|
|PSDNET-1069|Слой заполнения узором вызывает исключение при обновлении после загрузки|Ошибка|


## Изменения в общедоступном API
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDNET-210. Добавление свойства IsOpen для группы слоев**

{{< highlight csharp >}}
// Пример чтения и записи свойства IsOpen во время выполнения.
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. Изображение PSD с растровыми масками слоя теряет маски при сохранении в изображение PSD с 16 битами**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Режим смешивания Dissolve не применяется к папке с маской**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Конкретный файл не может быть открыт в Photoshop после сохранения в Aspose.PSD 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Необходимо вручную открыть PSD-файл Photoshop'ом.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // нет исключения.
            }
{{< /highlight >}}

**PSDNET-1068. Неправильное отображение слоя с режимом наложения Linear Dodge (Add)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Слой заполнения узором вызывает исключение при обновлении после загрузки**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}
