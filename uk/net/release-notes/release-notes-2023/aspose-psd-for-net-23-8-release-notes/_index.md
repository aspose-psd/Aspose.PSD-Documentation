---
title: Особливості версії Aspose.PSD для .NET 23.8 - Примітки до релізу
type: docs
weight: 50
url: /uk/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до релізу [Aspose.PSD для .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Опис**                                                                                                 | **Категорія** |
|:------------|:---------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Додано новий тип змін (Прапорець) | Функція |
| PSDNET-1621 | Додано нові типи змін: дуга угору, дуга вниз, сфера | Функція |
| PSDNET-1682 | Реалізовано новий метод PsdImage.AddPosterizeAdjustmentLayer для додавання нового шару Постеризації | Функція |
| PSDNET-913  | Інформація у файлі PSD втрачається під час простого відкривання та збереження | Помилка  |
| PSDNET-1352 | Не вдалося завантажити зображення | Помилка  |
| PSDNET-1553 | Не вдалося завантажити зображення: Неможливо привести об'єкт типу UnknownStructure до типу DescriptorStructure | Помилка  |
| PSDNET-1631 | Файл, змінений в бібліотеці стороннього виробника, руйнує файл PSD, але його можна відкрити в Photoshop | Помилка  |


## **Зміни в публічному API**
# **Додані API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Вилучені API:**
- Немає


## **Приклади використання:**

**PSDNET-913. Інформація у файлі PSD втрачається під час простого відкривання та збереження**

{{< highlight csharp >}}
string src = "Оригінальний файл.psd";
string outputPsd = "вихідний_Оригінальний файл.psd";
string outputPng = "вихідний_Оригінальний файл.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Не вдалося завантажити зображення**

{{< highlight csharp >}}
string srcFile1 = "текст_тесту.psd";
string srcFile2 = "тест_розумному_об'єкті.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Не вдалося завантажити зображення: Неможливо привести об'єкт типу UnknownStructure до типу DescriptorStructure**

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
            // Повинно завантажитися правильно
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Файл, змінений в бібліотеці стороннього виробника, руйнує файл PSD, але його можна відкрити в Photoshop**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "експорт.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Додано новий тип змін (Прапорець)**

{{< highlight csharp >}}
string sourceFile = "прапорець_зміна.psd";
string outputFile = "прапорець_експорт.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Додано нові типи змін: дуга угору, дуга вниз, сфера**

{{< highlight csharp >}}
string sourceFileArcUpper = "дуга_вверху_зміна.psd";
string sourceFileArcLower = "дуга_внизу_зміна.psd";
string sourceFileBulge =  "випуклість_зміна.psd";

string outputFileArcUpper ="Експорт_дуга_вверху.png";
string outputFileArcLower = "Експорт_дуга_внизу.png";
string outputFileBulge = "Експорт_випуклість.png";

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

**PSDNET-1682. Реалізовано новий метод PsdImage.AddPosterizeAdjustmentLayer для додавання нового шару Постеризації**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Перевірка збережених змін
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
        throw new Exception(message ?? "Об'єкти не рівні.");
    }
}
{{< /highlight >}}
