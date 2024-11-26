---
title: Оголошення про випуск Aspose.PSD для .NET 24.3
type: docs
weight: 100
url: /uk/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить оголошення про випуск [Aspose.PSD для .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Опис**                                                                                            | **Категорія**     |
|:------------|:-----------------------------------------------------------------------------------------------------|:-----------------|
| PSDNET-1914 | [Формат AI] Зменшення часу завантаження великих багатосторінкових AI-зображень                        | Покращення       |
| PSDNET-1905 | Файл PSD після перетворення з 8 біт в 16 біт стає нерозпізнаваним                                    | Помилка          |
| PSDNET-1906 | Файл PSD після перетворення з 8 біт в 32 біт стає нерозпізнаваним                                    | Помилка          |
| PSDNET-1921 | [Формат AI] Виправлення відображення короткої кривої у файлі AI                                       | Помилка          |

## **Зміни в публічному API**
# **Додані API:**
- Немає

# **Вилучені API:**
- Немає

## **Приклади використання:**

**PSDNET-1905. Файл PSD після перетворення з 8 біт в 16 біт стає нерозпізнаваним**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Неправильний глобальний ресурс, перший ресурс має бути Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. Файл PSD після перетворення з 8 біт в 32 біт стає нерозпізнаваним**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Неправильний глобальний ресурс, перший ресурс має бути Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [Формат AI] Виправлення відображення короткої кривої у файлі AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
