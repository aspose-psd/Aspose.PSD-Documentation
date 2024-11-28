---
title: Примечания к выпуску Aspose.PSD для .NET 24.8
type: docs
weight: 50
url: /ru/net/aspose-psd-for-net-24-8-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 24.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                              | **Категория** |
|:------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2091 | [Формат AI] Добавлена обработка групп XObject                                                       | Улучшение   |
| PSDNET-1754 | Улучшить возможности искажения Warp за счет добавления WarpSettings для TextLayer и SmartObjectLayer | Функционал  |
| PSDNET-1836 | [Формат AI] Обработка слоев в операторах потоков содержимого                                         | Функционал  |
| PSDNET-2015 | Результат рендеринга файла AI очень отличается от результатов Illustrator                           | Ошибка      |
| PSDNET-2093 | Переподключение умного объекта не применяется ко всем умным объектам в файле PSD                   | Ошибка      |

## **Изменения в общедоступном API**
# **Добавлены методы:**

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **Удаленные методы:**
- Нет

## **Примеры использования:**

**PSDNET-1754. Улучшить возможности искажения Warp за счет добавления WarpSettings для TextLayer и SmartObjectLayer**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "smart_without_warp.psd");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

string[] outputImageFile = new string[4];
string[] outputPsdFile = new string[4];

for (int caseIndex = 0; caseIndex < outputImageFile.Length; caseIndex++)
{
    outputImageFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".png");
    outputPsdFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".psd");

    using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
    {
        foreach (Layer layer in img.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                var smartLayer = (SmartObjectLayer)layer;
                smartLayer.WarpSettings = GetWarpSettingsByIndex(smartLayer.WarpSettings, caseIndex);
            }

            if (layer is TextLayer)
            {
                var textLayer = (TextLayer)layer;

                if (caseIndex != 3)
                {
                    textLayer.WarpSettings = GetWarpSettingsByIndex(textLayer.WarpSettings, caseIndex);
                }
            }
        }

        img.Save(outputPsdFile[caseIndex], new PsdOptions());
    }

    using (PsdImage img = (PsdImage)Image.Load(outputPsdFile[caseIndex], opt))
    {
        img.Save(outputImageFile[caseIndex],
            new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
    }
}

WarpSettings GetWarpSettingsByIndex(WarpSettings warpParams, int caseIndex)
{
    switch (caseIndex)
    {
        case 0:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 20;
            break;
        case 1:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Vertical;
            warpParams.Value = 10;
            break;
        case 2:
            warpParams.Style = WarpStyles.Flag;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 30;
            break;
        case 3:
            warpParams.Style = WarpStyles.Custom;
            warpParams.MeshPoints[2].Y += 70;
            break;
    }

    return warpParams;
}
{{< /highlight >}}

**PSDNET-1836. [AI Format] Обработка слоев в операторах потоков содержимого**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Layers-NoPen.ai");
string outputFile = Path.Combine(outputFolder, "Layers-NoPen.output.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}

//// Кривые из слоя с именем "Pen" должны быть скрыты
{{< /highlight >}}

**PSDNET-2015. Результат рендеринга файла AI очень отличается от результатов Illustrator**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "4.ai");
string outputFilePath = Path.Combine(outputFolder, "4.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2093. Переподключение умного объекта не применяется ко всем умным объектам в файле PSD**

{{< highlight csharp >}}
string[] files = { "simple_test", "w22" };
string changeFile = Path.Combine(baseFolder, "image(19).png");

string[] sourceFile = new string[files.Length];
string[] outputFiles = new string[files.Length];

for (int i = 0; i < files.Length; i++)
{
    sourceFile[i] = Path.Combine(baseFolder, files[i] + ".psd");
    outputFiles[i] = Path.Combine(outputFolder, files[i] + "_output.psd");

    using (var image = (PsdImage)Image.Load(sourceFile[i]))
    {
        foreach (Layer layer in image.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                SmartObjectLayer smart = (SmartObjectLayer)layer;

                // Для второго умного слоя была ошибка
                smart.ReplaceContents(changeFile);
            }
        }

        image.Save(outputFiles[i]);
    }
}
{{< /highlight >}}
