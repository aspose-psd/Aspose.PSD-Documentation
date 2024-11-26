---
title: Aspose.PSD для .NET 22.6 - Примечания к выпуску
type: docs
weight: 70
url: /ru/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-940|Создание API для получения уникального хэша для похожих слоев в разных файлах|Улучшение|
|PSDNET-678|Некорректное отображение слоя FillLayer с узором в случае, когда узоров больше одного и изменен порядок слоев|Ошибка|
|PSDNET-1125|Исключение при загрузке конкретного файла PSD с режимом цвета CMYK|Ошибка|


## **Изменения в общедоступном API**
# **Добавленные API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDNET-678. Некорректное отображение слоя FillLayer с узором в случае, когда узоров больше одного и изменен порядок слоев**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Создание API для получения уникального хэша для похожих слоев в разных файлах**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    // код на C#
}
{{< /highlight >}}

**PSDNET-1125. Исключение при загрузке конкретного файла PSD с режимом цвета CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}