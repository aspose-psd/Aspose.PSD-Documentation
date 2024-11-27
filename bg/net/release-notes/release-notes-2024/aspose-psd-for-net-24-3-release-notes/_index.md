---
title: Aspose.PSD за .NET 24,3 - Бележки към версията
type: docs
weight: 100
url: /bg/net/aspose-psd-za-net-24-3-belejki-kam-versiyata/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки към версията за [Aspose.PSD за .NET 24,3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}


| **Ключ**    | **Резюме**                                                           | **Категория**     |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI Формат] Намаляване на времето за зареждане на големи многостранични AI изображения | Усъвършенстване |
| PSDNET-1905 | PSD файл след конвертирането от 8 бита на 16 бита стана непрочетим   | Грешка       |
| PSDNET-1906 | PSD файл след конвертирането от 8 бита на 32 бита стана непрочетим   | Грешка       |
| PSDNET-1921 | [AI Формат] Оправяне на извеждането на къса крива в AI файл          | Грешка       |

## **Промени в публичното API**
# **Добавени API:**
- Няма

# **Премахнати API:**
- Няма

## **Примери за използване:**

**PSDNET-1905. PSD файл след конвертирането от 8 бита на 16 бита стана непрочетим**

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
        // е ок
    }
    else
    {
        throw new Exception("Грешен глобален ресурс, първият ресурс трябва да бъде Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. PSD файл след конвертирането от 8 бита на 32 бита стана непрочетим**

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
        // е ок
    }
    else
    {
        throw new Exception("Грешен глобален ресурс, първият ресурс трябва да бъде Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI Формат] Оправяне на извеждането на къса крива в AI файл**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
