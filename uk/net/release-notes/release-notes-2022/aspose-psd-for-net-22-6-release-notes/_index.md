---
title: Aspose.PSD для .NET 22.6 - Примітки до випуску
type: docs
weight: 70
url: /uk/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до випуску [Aspose.PSD для .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-940|Створення API для отримання унікального хешу для схожих прошарків у різних файлах|Покращення|
|PSDNET-678|Некоректне відтворення FillLayer з шаблоном у випадку, коли шаблонів більше одного і змінено порядок прошарків|Помилка|
|PSDNET-1125|Виняток при завантаженні конкретного файлу PSD з кольоровим режимом CMYK|Помилка|


## **Зміни у публічному API**
# **Додані API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Вилучені API:**
- Немає


## **Приклади використання:**

**PSDNET-678. Некоректне відтворення FillLayer з шаблоном у випадку, коли шаблонів більше одного і змінено порядок прошарків**

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

**PSDNET-940. Створення API для отримання унікального хешу для схожих прошарків у різних файлах**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

// Код імплементовано вище.
{{< /highlight >}}

**PSDNET-1125. Виняток при завантаженні конкретного файлу PSD з кольоровим режимом CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}