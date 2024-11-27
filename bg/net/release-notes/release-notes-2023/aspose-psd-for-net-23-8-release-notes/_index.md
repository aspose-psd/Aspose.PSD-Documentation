---
title: Aspose.PSD за .NET 23.8 - Бележки за изданието
type: docs
weight: 50
url: /bg/net/aspose-psd-za-net-23-8-belezhki-za-izdanieto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**     | **Обобщение**                                                                                                  | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Добавяне на нов тип warp (Flag) | Функционалност |
| PSDNET-1621 | Добавяне на нови типове warp: arc up, arc down, sphere | Функционалност |
| PSDNET-1682 | Имплементиране на нов метод PsdImage.AddPosterizeAdjustmentLayer за добавяне на нов слой за Posterize | Функционалност |
| PSDNET-913  | Изгубена информация на PSD при само отваряне и запазване | Проблем |
| PSDNET-1352 | Грешка при зареждане на изображението | Проблем |
| PSDNET-1553 | Грешка при зареждане на изображението: Невъзможност за преобразуване на обект от тип UnknownStructure в тип DescriptorStructure | Проблем |
| PSDNET-1631 | Промяна във файл на библиотека от трета страна кара PSD файла да се повреди, но той може да бъде отворен в Photoshop | Проблем |


## **Промени в публичния API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Премахнати API:**
- Нито един


## **Примери за използване:**

**PSDNET-913. Изгубена информация на PSD при само отваряне и запазване**

{{< highlight csharp >}}
string src = "Оригинален файл.psd";
string outputPsd = "out_Оригинален файл.psd";
string outputPng = "out_Оригинален файл.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Грешка при зареждане на изображението**

{{< highlight csharp >}}
string srcFile1 = "тест_текст.psd";
string srcFile2 = "тест_умен_обект.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Грешка при зареждане на изображението: Невъзможност за преобразуване на обект от тип UnknownStructure в тип DescriptorStructure**

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
            // Трябва да се зареди коректно
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Промяна във файл на библиотека от трета страна псува PSD файла, но той може да бъде отворен в Photoshop**

{{< highlight csharp >}}
string sourceFile = "изход.psd";
string outputFile = "експорт.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Добавяне на нов тип warp (Flag)**

{{< highlight csharp >}}
string sourceFile = "флаг_warp.psd";
string outputFile = "флаг_експорт.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Добавяне на нови типове warp: arc up, arc down, sphere**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ArcUpper_export.png";
string outputFileArcLower = "ArcLower_export.png";
string outputFileBulge = "Bulge_export.png";

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

**PSDNET-1682. Имплементиране на нов метод PsdImage.AddPosterizeAdjustmentLayer за добавяне на нов слой за Posterize**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Проверете запазените промени
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
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}
