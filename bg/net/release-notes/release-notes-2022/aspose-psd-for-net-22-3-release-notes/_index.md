---
title: Aspose.PSD за .NET 22.3 - Бележки към изданието
type: docs
weight: 100
url: /bg/net/aspose-psd-za-net-22-3-belejki-za-izdanie/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки към изданието на [Aspose.PSD за .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-210|Добавяне на свойството IsOpen за Група на слоевете|Функционалност|
|PSDNET-643|PSD изображение с маски за растерни слоеве отхвърля маските при запазване към 16-битово PSD изображение|Грешка|
|PSDNET-899|Режим за смесване Dissolve не се прилага към папката с маска|Грешка|
|PSDNET-1047|Конкретен файл не може да бъде отворен от Photoshop след запазване в Aspose.PSD 21.11|Грешка|
|PSDNET-1068|Неправилно изобразяване на слоя с режим на смесване Линейно изсветляване (Добавяне)|Грешка|
|PSDNET-1069|Слой за попълване с шаблон хвърля грешка при актуализация след зареждане|Грешка|


## **Промени в общественото API**
# **Добавени API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Премахнати API:**
- Нито едно


## **Примери за употреба:**

**PSDNET-210. Добавяне на свойството IsOpen за Група на слоевете**

{{< highlight csharp >}}
// Пример за четене и запис на свойството IsOpen по време на изпълнение.
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

**PSDNET-643. PSD изображение с маски за растерни слоеве отхвърля маските при запазване към 16-битово PSD изображение**

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

**PSDNET-899. Режим за смесване Dissolve не се прилага към папката с маска**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Конкретен файл не може да бъде отворен от Photoshop след запазване в Aspose.PSD 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Необходимо е ръчно да се отвори изходния PSD от Photoshop.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // няма изключение.
            }
{{< /highlight >}}

**PSDNET-1068. Неправилно изобразяване на слоя с режим на смесване Линейно изсветляване (Добавяне)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Слой за попълване с шаблон хвърля грешка при актуализация след зареждане**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}
