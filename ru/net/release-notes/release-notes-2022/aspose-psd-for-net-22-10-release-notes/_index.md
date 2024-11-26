---
title: Aspose.PSD для .NET 22.10 - Примечания к выпуску
type: docs
weight: 30
url: /ru/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к версии [Aspose.PSD для .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- В этом выпуске имеется ошибка в случае экспорта 16-битных изображений, поэтому мы рекомендуем быть осторожными при использовании этой функции в этом релизе.
Пожалуйста, не обновляйте Aspose.PSD до версии 22.9-22.10, если работа с 16-битной обработкой изображений является вашей основной функциональностью.

Мы работаем над решением этих проблем.

{{% /alert %}}

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-1287|Удаление устаревших свойств в Lfx2Resource|Улучшение|
|PSDNET-1071|Aspose.PSD не может открыть PSD (RGB/16 бит) с сжатием ZipWithoutPrediction|Ошибка|
|PSDNET-1257|Эффекты времени пропадают и отображаются странным образом. (в Photoshop)|Ошибка|
|PSDNET-1278|Прозрачность не работает для эффекта обводки с положением Inside|Ошибка|
|PSDNET-1279|Регрессия: Ошибка при открытии файла PSD|Ошибка|
|PSDNET-1284|Обновление текста не работает с некоторыми азиатскими символами. Ошибка при обработке конкретного символа|Ошибка|
|PSDNET-1291|Обновление текста не работает с некоторыми азиатскими символами. Ошибка при отображении конкретного символа|Ошибка|
|PSDNET-1292|Ошибка при открытии экспортированного файла в Photoshop после сохранения конкретных азиатских символов|Ошибка|


## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет


# **Удаленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Примеры использования:**

**PSDNET-1071. Aspose.PSD не может открыть PSD (RGB/16 бит) с сжатием ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Эффекты времени пропадают и отображаются странным образом. (в Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Создание временной шкалы с несколькими кадрами.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. Прозрачность не работает для эффекта обводки с положением Inside**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Регрессия: Ошибка при открытии файла PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Обновление текста не работает с некоторыми азиатскими символами. Ошибка при обработке конкретного символа**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // выбрать проблемный символ

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Удаление устаревших свойств в Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Обновление настроек BlendMode для эффекта
    effect.BlendMode = BlendMode.Darken;

    // Обновление настроек Opacity для эффекта
    effect.Opacity = 128; // 50%

    // Обновление цвета заливки эффекта обводки
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Обновление текста не работает с некоторыми азиатскими символами. Ошибка при отрисовке конкретных символов**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // выбрать проблемные символы

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Ошибка при открытии экспортированного файла в Photoshop после сохранения конкретных азиатских символов**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}
