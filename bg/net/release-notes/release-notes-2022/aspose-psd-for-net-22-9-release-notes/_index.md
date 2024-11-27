---
title: Aspose.PSD за .NET 22.9 - Бележки за изданието
type: docs
weight: 40
url: /bg/net/aspose-psd-za-net-22-9-belejki-za-izdanieto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- В това издание има регресия при 16-битовите експорти, затова препоръчваме внимание при използването на тази функционалност в това издание. Моля, не актуализирайте Aspose.PSD до версия 22.9, ако обработката на изображения от 16 бита е вашата основна функционалност.
- За някои версии на Photoshop, потребителите може да се сблъскат с прозорец с грешка при четене на слой, което няма да се отрази на работата с PSD файла.

Работим по решенията на тези проблеми.

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-1237|Създаване на вътрешната модел LayerStyleFX, която ще съдържа ефекти и свързани данни за използването на единичния модел в ефектите ресурси Lfx2, lmfx и mlst|Подобрение|
|PSDNET-1227|Добавяне на четене и запис на структури 'Lefx' с информация за ефектите за състояния на слоеве в моделите за времева линия|Функция|
|PSDNET-1230|Прилагане на състоянието на слоя от времевата линия към слой в PsdImage|Функция|
|PSDNET-1072|Неправилна прозрачност при запазване на PSD файл (RGB/16битов) при експортиране към 8битов|Проблем|
|PSDNET-1140|Изключение при зареждане на стъпката с глобални ресурси на слой при отваряне на PSB документ|Проблем|
|PSDNET-1266|Изтичане на памет при обработката на конкретни файлове|Проблем|


## **Промени в общественото API**
# **Добавени API:**
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


# **Премахнати API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Примери за използване:**

**PSDNET-1072. Неправилна прозрачност при запазване на PSD файл (RGB/16битов) при експортиране към 8битов**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // Опции за запазване на 16 битове
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // Запазване на изображение с 16-битови цветове
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Изключение при зареждане на стъпката с глобални ресурси на слой при отваряне на PSB документ**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // Тук не би трябвало да има изключение.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Добавяне на четене и запис на структури 'Lefx' с информация за ефектите за състояния на слоеве в моделите за времева линия**

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

**PSDNET-1230. Прилагане на състоянието на слоя от времевата линия към слой в PsdImage**

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

    // Промяна на активния кадър от 0 на 1, за да се активира прилагането на LayerState към Layer
    timeLine.ActiveFrame = 1;

    // Прилагане на промените към PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Изтичане на памет при обработката на конкретни файлове**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Общо използвани байтове преди тест: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // CheckOpenSaving
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
Console.WriteLine("Общо използвани байтове след теста: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "Изтичане на памет в основната функционалност!");
{{< /highlight >}}
