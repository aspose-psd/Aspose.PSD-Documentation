---
title: Примітки до версій Aspose.PSD для .NET 22.10
type: docs
weight: 30
url: /uk/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до версії [Aspose.PSD для .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- У цьому випуску є регресія у випадку експорту з обробкою 16-бітових даних, тому ми рекомендуємо бути обережними при використанні цієї функції в цьому випуску. Будь ласка, не оновлюйте Aspose.PSD до версій 22.9-22.10, якщо обробка зображень з 16-бітовим кольором є вашою основною функціональністю.

Ми працюємо над вирішенням цих проблем.

{{% /alert %}}

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-1287|Видалення застарілих властивостей в Lfx2Resource|Покращення|
|PSDNET-1071|Aspose.PSD не може відкрити PSD (RGB/16 біт) зі стисненням ZipWithoutPrediction|Помилка|
|PSDNET-1257|Ефекти в часовій шкалі зникають і показуються у дивний спосіб. (в Photoshop)|Помилка|
|PSDNET-1278|Прозорість не працює для ефекту обводки з внутрішнім положенням|Помилка|
|PSDNET-1279|Регресія: Помилка при відкритті файлу PSD|Помилка|
|PSDNET-1284|Оновлення тексту невдається з деякими азійськими символами. Помилка при обробці конкретного символу|Помилка|
|PSDNET-1291|Оновлення тексту невдається з деякими азійськими символами. Помилка при візуалізації конкретного символу|Помилка|
|PSDNET-1292|Помилка при відкритті експортованого файлу у Photoshop після збереження конкретних азійських символа|Помилка|


## **Зміни у загальнодоступному API**
# **Додані API:**
- Немає


# **Вилучені API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Приклади використання:**

**PSDNET-1071. Aspose.PSD не може відкрити PSD (RGB/16 біт) зі стисненням ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Ефекти в часовій шкалі зникають і показуються у дивний спосіб. (в Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Створення часової шкали з декількома кадрами.
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

**PSDNET-1278. Прозорість не працює для ефекту обводки з внутрішнім положенням**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Регресія: Помилка при відкритті файлу PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Оновлення тексту невдається з деякими азійськими символами. Помилка при обробці конкретного символу**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // вибір проблемного символу

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Видалення застарілих властивостей в Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Оновлення параметра BlendMode в ефекті
    effect.BlendMode = BlendMode.Darken;

    // Оновлення параметра Opacity в ефекті
    effect.Opacity = 128; // 50%

    // Оновлення параметру fill Color в ефекті обводки
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Оновлення тексту невдається з деякими азійськими символами. Помилка при візуалізації конкретного символу**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // вибір проблемних символів

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Помилка при відкритті експортованого файлу у Photoshop після збереження конкретних азійських символів**

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
