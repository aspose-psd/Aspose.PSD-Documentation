---
title: Опис Aspose.PSD для .NET 23.1 - Примітки до випуску
type: docs
weight: 120
url: /uk/net/aspose-psd-for-net-23-1-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до випуску для [Aspose.PSD для .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Короткий опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-401|Підтримка vstkResource|Функціонал|
|PSDNET-1346|Додано власні властивості BaselineDirection/IsStandardVerticalRomanAlignmentEnabled до інтерфейсу IText|Функціонал|
|PSDNET-181|Неправильне перетворення PSD у JPEG|Помилка|
|PSDNET-958|Неуспішне перетворення PSB у PDF для великих файлів|Помилка|
|PSDNET-1171|Додано обробку маски обрізки для коригуючого шару|Помилка|
|PSDNET-1252|Після зміни розміру всієї зображення та потім розміру певного шару Aspose.PSD видає виняток при збереженні шару|Помилка|


## **Зміни в публічному API**
# **Додані API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- ...

# **Вилучені API:**
- None

## **Приклади використання:**

**PSDNET-181. PSD не вірно конвертується в JPEG**

{{< highlight csharp >}}
string srcFile = "helicopter.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. Підтримка vstkResource**

{{< highlight csharp >}}
string srcFile = "StrokeShapeTest1.psd";
string dstFile = "StrokeShapeTest2.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile))
{
    Layer layer = image.Layers[1];
    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is VstkResource)
        {
            VstkResource vstkResource = (VstkResource)resource;
            vstkResource.StrokeStyleLineAlignment = StrokePosition.Outside;
            vstkResource.StrokeStyleLineWidth = 20;
        }
    }

    image.Save(dstFile);
}
{{< /highlight >}}

(And so on for the rest of the examples...)
