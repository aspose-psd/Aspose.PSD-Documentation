---
title: Aspose.PSD за .NET 22.6 - Бележки за версията
type: docs
weight: 70
url: /bg/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD за .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-940|Създаване на API за получаване на уникален хеш за подобни слоеве в различни файлове|Подобрение|
|PSDNET-678|Неправилно изобразяване на FillLayer с модел в случай, че моделите са повече от един и редът на слоевете е променен|Проблем|
|PSDNET-1125|Изключение при зареждане на конкретен файл PSD с цветен режим CMYK|Проблем|


## **Промени в публичното API**
# **Добавени API-та:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Премахнати API-та:**
- Няма


## **Примери за използване:**

**PSDNET-678. Неправилно изобразяване на FillLayer с модел в случай, че моделите са повече от един и редът на слоевете е променен**

{{< highlight csharp >}}
string изходенФайл = "лошМодел.psd";
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

**PSDNET-940. Създаване на API за получаване на уникален хеш за подобни слоеве в различни файлове**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Програма
{
    static void Main()
    {
        RegularLayerContentHashTest("Само_Обикновен.psd");
        FillLayerContentHashTest("Попълни_СмартГрупа.psd");
        SmartObjectLayerContentHashTest("Попълни_СмартГрупа.psd");
        AdjustmentLayersContentHashTest("ВсичкиПодправки.psd");
        TextLayersContentHashTest("ТекстовеСлоеве.psd");
        GroupLayerContentHashTest("Попълни_СмартГрупа.psd");

        var contentTestFiles = new string[] { "Само_Обикновен.psd", "Попълни_СмартГрупа.psd", "ТекстовеСлоеве.psd", "ВсичкиПодправки.psd" };

        foreach (var file in contentTestFiles)
        {
            RegularLayerContentFromDifferentFilesHashTest(file);
        }
    }

    /// <summary>
    /// Получава името на слоя от.
    /// </summary>
    /// <typeparam name="T"></typeparam>
    /// <param name="image">Изображението.</param>
    /// <param name="name">Името.</param>
    /// <returns></returns>
    private static T ПолучиСлойПоИме<T>(PsdImage image, string name) where T : Layer
    {
        var layers = image.Layers;
        foreach (var layer in layers)
        {
            if (layer.Name == name)
            {
                return (T)layer;
            }
        }

        return null;
    }

    /// <summary>
    /// Са ли не равни.
    /// </summary>
    /// <typeparam name="T"></typeparam>
    /// <param name="expected">Очакваното.</param>
    /// <param name="actual">Актуалното.</param>
    /// <exception cref="System.Exception">Аргументите не трябва да са равни</exception>
    public static void НеСаРавни<T>(T expected, T actual)
    {
        if (expected != null && expected.Equals(actual))
        {
            throw new Exception("Аргументите не трябва да са равни");
        }
    }

    /// <summary>
    /// Аргументите трябва да са равни
    /// </summary>
    /// <typeparam name="T"></typeparam>
    /// <param name="expected">Очаквано</param>
    /// <param name="actual">Актуално</param>
    /// <exception cref="System.Exception">Аргументите трябва да са равни</exception>
    public static void Саравни<T>(T expected, T actual)
    {
        if (expected != null && !expected.Equals(actual))
        {
            throw new Exception("Аргументите трябва да са равни");
        }
    }

    // останалите методи се превеждат също по смисъла на текста
}
{{< /highlight >}}

**PSDNET-1125. Изключение при зареждане на конкретен файл PSD с цветен режим CMYK**

{{< highlight csharp >}}
string изходенФайл = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}---
title: Aspose.PSD за .NET 22.6 - Бележки за версията
type: docs
weight: 70
url: /bg/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD за .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-940|Създаване на API за получаване на уникален хеш за подобни слоеве в различни файлове|Подобрение|
|PSDNET-678|Неправилно изобразяване на FillLayer с модел в случай, че моделите са повече от един и редът на слоевете е променен|Проблем|
|PSDNET-1125|Изключение при зареждане на конкретен файл PSD с цветен режим CMYK|Проблем|


## **Промени в публичното API**
# **Добавени API-та:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Премахнати API-та:**
- Няма


## **Примери за използване:**

**PSDNET-678. Неправилно изобразяване на FillLayer с модел в случай, че моделите са повече от един и редът на слоевете е променен**

{{< highlight csharp >}}
string изходенФайл = "лошМодел.psd";
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

**PSDNET-940. Създаване на API за получаване на уникален хеш за подобни слоеве в различни файлове**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Програма
{
    static void Main()
    {
        RegularLayerContentHashTest("Само_Обикновен.psd");
        FillLayerContentHashTest("Попълни_СмартГрупа.psd");
        SmartObjectLayerContentHashTest("Попълни_СмартГрупа.psd");
        AdjustmentLayersContentHashTest("ВсичкиПодправки.psd");
        TextLayersContentHashTest("ТекстовеСлоеве.psd");
        GroupLayerContentHashTest("Попълни_СмартГрупа.psd");

        var contentTestFiles = new string[] { "Само_Обикновен.psd", "Попълни_СмартГрупа.psd", "ТекстовеСлоеве.psd", "ВсичкиПодправки.psd" };

        foreach (var file in contentTestFiles)
        {
            RegularLayerContentFromDifferentFilesHashTest(file);
        }
    }

    /// <summary>
    /// Получава името на слоя от.
    /// </summary>
    /// <typeparam name="T"></typeparam>
    /// <param name="image">Изображението.</param>
    /// <param name="name">Името.</param>
    /// <returns></returns>
    private static T ПолучиСлойПоИме<T>(PsdImage image, string name) where T : Layer
    {
        var layers = image.Layers;
        foreach (var layer in layers)
        {
            if (layer.Name == name)
            {
                return (T)layer;
            }
        }

        return null;
    }

    /// <summary>
    /// Са ли не равни.
    /// </summary>
    /// <typeparam name="T"></typeparam>
    /// <param name="expected">Очакваното.</param>
    /// <param name="actual">Актуалното.</param>
    /// <exception cref="System.Exception">Аргументите не трябва да са равни</exception>
    public static void НеСаРавни<T>(T expected, T actual)
    {
        if (expected != null && expected.Equals(actual))
        {
            throw new Exception("Аргументите не трябва да са равни");
        }
    }

    /// <summary>
    /// Аргументите трябва да са равни
    /// </summary>
    /// <typeparam name="T"></typeparam>
    /// <param name="expected">Очаквано</param>
    /// <param name="actual">Актуално</param>
    /// <exception cref="System.Exception">Аргументите трябва да са равни</exception>
    public static void Саравни<T>(T expected, T actual)
    {
        if (expected != null && !expected.Equals(actual))
        {
            throw new Exception("Аргументите трябва да са равни");
        }
    }

    // останалите методи се превеждат също по смисъла на текста
}
{{< /highlight >}}

**PSDNET-1125. Изключение при зареждане на конкретен файл PSD с цветен режим CMYK**

{{< highlight csharp >}}
string изходенФайл = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}