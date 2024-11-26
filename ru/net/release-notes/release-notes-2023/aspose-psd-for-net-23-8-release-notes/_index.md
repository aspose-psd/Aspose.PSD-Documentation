---
title: Aspose.PSD для .NET 23.8 - Примечания к выпуску
type: docs
weight: 50
url: /ru/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к выпуску для [Aspose.PSD для .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**     | **Краткое описание**                                                                                                  | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Добавлен новый тип деформации (Флаг) | Функция |
| PSDNET-1621 | Добавлены новые типы деформации: дуга вверх, дуга вниз, сфера | Функция |
| PSDNET-1682 | Реализован новый метод PsdImage.AddPosterizeAdjustmentLayer для добавления нового слоя плаката| Функция |
| PSDNET-913  | Потеря информации PSD при простом открытии и сохранении | Ошибка     |
| PSDNET-1352 | Ошибка при загрузке изображения | Ошибка     |
| PSDNET-1553 | Ошибка при загрузке изображения: Невозможно привести объект типа UnknownStructure к типу DescriptorStructure| Ошибка     |
| PSDNET-1631 | Изменение файла в сторонней библиотеке портит файл PSD, но его можно открыть в Photoshop | Ошибка     |


## **Изменения в общедоступном API**
# **Добавленные API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDNET-913. Потеря информации PSD при простом открытии и сохранении**

{{< highlight csharp >}}
string src = "Исходный файл.psd";
string outputPsd = "out_Исходный файл.psd";
string outputPng = "out_Исходный файл.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Ошибка при загрузке изображения**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Ошибка при загрузке изображения: Невозможно привести объект типа UnknownStructure к типу DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Should load correctly
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Изменение файла в сторонней библиотеке портит файл PSD, но его можно открыть в Photoshop**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Добавлен новый тип деформации (Флаг)**

{{< highlight csharp >}}
string sourceFile = "флаг_деформация.psd";
string outputFile = "флаг_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Добавлены новые типы деформации: дуга вверх, дуга вниз, сфера**

{{< highlight csharp >}}
string sourceFileArcUpper = "дуга_вверх_деформация.psd";
string sourceFileArcLower = "дуга_вниз_деформация.psd";
string sourceFileBulge =  "выпуклость_деформация.psd";

string outputFileArcUpper ="Дуга_вверх_export.png";
string outputFileArcLower = "Дуга_вниз_export.png";
string outputFileBulge = "Выпуклость_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Реализован новый метод PsdImage.AddPosterizeAdjustmentLayer для добавления нового слоя плаката**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Check saved changes
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}
