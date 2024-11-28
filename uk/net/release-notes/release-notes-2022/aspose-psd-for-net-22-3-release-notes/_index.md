---
title: Aspose.PSD для .NET 22.3 - Примітки до випуску
type: docs
weight: 100
url: /uk/net/aspose-psd-dlya-net-22-3-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до [Aspose.PSD для .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}


|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-210|Додано властивість IsOpen для групи шарів|Функція|
|PSDNET-643|Зображення PSD з растровими масками шарів відкидає маски при збереженні у зображення PSD 16 біт|Помилка|
|PSDNET-899|Режим змішування розпад не застосовується до папки з маскою|Помилка|
|PSDNET-1047|Певний файл не може бути відкритий у Photoshop після збереження у Aspose.PSD 21.11|Помилка|
|PSDNET-1068|Неправильне відтворення шару з режимом змішування Linear Dodge (Add)|Помилка|
|PSDNET-1069|Шар заповнення візерунком видає виняток при оновленні після завантаження|Помилка|


## **Зміни у публічному API**
# **Додані API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Вилучені API:**
- Немає


## **Приклади використання:**

**PSDNET-210. Додано властивість IsOpen для групи шарів**

{{< highlight csharp >}}
// Приклад читання та запису властивості IsOpen під час виконання.
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

**PSDNET-643. Зображення PSD з растровими масками шарів відкидає маски при збереженні у зображення PSD 16 біт**

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

**PSDNET-899. Режим змішування розпад не застосовується до папки з маскою**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Певний файл не може бути відкритий у Photoshop після збереження у Aspose.PSD 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Потрібно вручну відкрити вихідний PSD у Photoshop.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // немає винятків.
            }
{{< /highlight >}}

**PSDNET-1068. Неправильне відтворення шару з режимом змішування Linear Dodge (Add)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Шар заповнення візерунком видає виняток при оновленні після завантаження**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}
