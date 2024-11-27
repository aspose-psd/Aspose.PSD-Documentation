---
title: Aspose.PSD за .NET 22.10 - Забележки за изданието
type: docs
weight: 30
url: /bg/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа забележки за изданието на [Aspose.PSD за .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Това издание има регресия в случая на експортиране с 16 бита, затова препоръчваме внимание при използването на тази функционалност в това издание.
Моля, не актуализирайте Aspose.PSD до версии 22.9-22.10, ако обработката на изображения с 16 бита е вашата основна функционалност.

Работим по решения на тези проблеми.

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-1287|Премахване на остарелите свойства в Lfx2Resource|Подобрение|
|PSDNET-1071|Aspose.PSD не може да отвори PSD (RGB/16bit) с ZipWithoutPrediction компресия|Проблем|
|PSDNET-1257|Ефектите на времевата линия изчезват и се показват по странен начин. (в Photoshop)|Проблем|
|PSDNET-1278|Прозрачността не работи за ефекта на чертежа с позиция отвътре|Проблем|
|PSDNET-1279|Регресия: Грешка при отварянето на файл PSD|Проблем|
|PSDNET-1284|Актуализацията на текста се проваля с някои азиатски символи. Грешка при парсирането на конкретен символ|Проблем|
|PSDNET-1291|Актуализацията на текста се проваля с някои азиатски символи. Грешка при рендирането на конкретен символ|Проблем|
|PSDNET-1292|Грешка при отварянето на експортирания файл от Photoshop след записване на конкретни азиатски символи|Проблем|


## **Промени в общественото API**
# **Добавени API:**
- Няма


# **Премахнати API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Примери за използване:**

**PSDNET-1071. Aspose.PSD не може да отвори PSD (RGB/16bit) с ZipWithoutPrediction компресия**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Ефектите на времевата линия изчезват и се показват по странен начин. (в Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Създаване на времева линия с няколко кадъра.
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

**PSDNET-1278. Прозрачността не работи за ефекта на чертежа с позиция отвътре**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Регресия: Грешка при отварянето на файл PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Актуализацията на текста се проваля с някои азиатски символи. Грешка при парсирането на конкретен символ**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // изберете проблемния символ

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Премахване на остарелите свойства в Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Актуализирайте опцията за режим на смесване на ефекта
    effect.BlendMode = BlendMode.Darken;

    // Актуализирайте опцията за непрозрачност на ефекта
    effect.Opacity = 128; // 50%

    // Актуализирайте опцията за попълване на цветовия ефект на черта
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Актуализацията на текста се проваля с някои азиатски символи. Грешка при рендирането на конкретен символ**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // изберете проблемните символи

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Грешка при отварянето на експортирания файл от Photoshop след записване на конкретни азиатски символи**

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
