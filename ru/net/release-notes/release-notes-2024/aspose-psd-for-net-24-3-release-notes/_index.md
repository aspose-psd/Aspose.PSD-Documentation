---
title: Aspose.PSD для .NET 24.3 - Примечания к выпуску
type: docs
weight: 100
url: /ru/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к [Aspose.PSD для .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}


| **Ключ**     | **Краткое изложение**                                                 | **Категория** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [Формат AI] Уменьшение времени загрузки больших многостраничных изображений AI |     Улучшение     |
| PSDNET-1905 | PSD-файл после преобразования из 8 бит в 16 бит становится нераспознаваемым |     Ошибка     |
| PSDNET-1906 | PSD-файл после преобразования из 8 бит в 32 бит становится нераспознаваемым |     Ошибка     |
| PSDNET-1921 | [Формат AI] Исправление отображения короткой кривой в файле AI         |     Ошибка     |

## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

## **Примеры использования:**

**PSDNET-1905. PSD-файл после преобразования из 8 бит в 16 бит становится нераспознаваемым**

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
        throw new Exception("Неверный глобальный ресурс, первый ресурс должен быть Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. PSD-файл после преобразования из 8 бит в 32 бит становится нераспознаваемым**

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
        throw new Exception("Неверный глобальный ресурс, первый ресурс должен быть Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [Формат AI] Исправление отображения короткой кривой в файле AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
