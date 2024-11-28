---
title: Aspose.PSD для .NET 22.9 - Примечания к выпуску
type: docs
weight: 40
url: /ru/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску для [Aspose.PSD для .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- В этом релизе есть ошибка в случае экспорта 16-битных изображений, поэтому рекомендуем быть осторожными при использовании этой функции в этом релизе.
Пожалуйста, не обновляйте Aspose.PSD до 22.9, если обработка изображений с глубиной цвета 16 бит является вашей основной функциональностью.
- Для нескольких версий Photoshop пользователи могут столкнуться с окном с ошибкой чтения слоя, это не повлияет на работу с файлом PSD.

Мы работаем над решением этих проблем.

{{% /alert %}}

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-1237|Создание внутренней модели LayerStyleFX, которая будет содержать эффекты и сопутствующие данные для использования одной модели в ресурсах эффектов Lfx2, lmfx и mlst|Улучшение|
|PSDNET-1227|Добавление чтения и записи структур 'Lefx' с информацией об эффектах для состояний слоев в моделях TimeLine|Функция|
|PSDNET-1230|Применение состояния слоя TimeLine к слою в PsdImage|Функция|
|PSDNET-1072|Некорректная прозрачность при сохранении файла PSD (RGB/16 бит) при экспорте в 8 бит|Ошибка|
|PSDNET-1140|Исключение при загрузке шага глобальных ресурсов слоев при открытии документа PSB|Ошибка|
|PSDNET-1266|Утечка памяти при обработке конкретных файлов|Ошибка|


## **Изменения в общедоступном API**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **Удаленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Примеры использования:**

**PSDNET-1072. Некорректная прозрачность при сохранении файла PSD (RGB/16 бит) при экспорте в 8 бит**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // 16-битные параметры сохранения
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // Сохранение изображения с 16-битными цветами
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Исключение при загрузке шага глобальных ресурсов слоев при открытии документа PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // Здесь не должно быть исключения.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Добавление чтения и записи структур 'Lefx' с информацией об эффектах для состояний слоев в моделях TimeLine**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var layerStateEffects11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    layerStateEffects11.AddDropShadow();
    layerStateEffects11.AddGradientOverlay();

    var layerStateEffects21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    layerStateEffects21.AddStroke(FillType.Color);
    layerStateEffects21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. Применение состояния слоя TimeLine к слою в PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_animated.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // Изменение активного кадра с 0 на 1 для активации применения LayerState к Layer.
    timeLine.ActiveFrame = 1;

    // Применение изменений к PsdImage.
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Утечка памяти при обработке конкретных файлов**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Общее количество использованных байтов перед тестом: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // Проверка открытия и сохранения.
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Общее количество использованных байтов после теста: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "Найдена утечка памяти в основной функциональности!");
{{< /highlight >}}
