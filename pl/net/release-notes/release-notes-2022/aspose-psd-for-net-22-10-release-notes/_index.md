---
title: Notatki wydania Aspose.PSD dla .NET 22.10
type: docs
weight: 30
url: /pl/net/aspose-psd-dla-net-22-10-notatki-o-wydaniu/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}


{{% alert color="warning" %}}

- To wydanie zawiera regresję w przypadku eksportu 16-bitowego, dlatego zalecamy ostrożność przy korzystaniu z tej funkcji w tej wersji.
Prosimy nie aktualizować Aspose.PSD do wersji 22.9-22.10, jeśli przetwarzanie obrazów 16-bitowych stanowi podstawową funkcjonalność.

Pracujemy nad rozwiązaniami tych problemów.

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-1287|Usunięcie przestarzałych właściwości w Lfx2Resource|Usprawnienie|
|PSDNET-1071|Aspose.PSD nie może otworzyć pliku PSD (RGB/16-bit) z kompresją ZipWithoutPrediction|Błąd|
|PSDNET-1257|Efekty osi czasu znikały i pokazywały się w dziwny sposób (w Photoshopie)|Błąd|
|PSDNET-1278|Przezroczystość nie działa dla efektu konturu z wewnętrzną pozycją|Błąd|
|PSDNET-1279|Regresja: Błąd podczas otwierania pliku PSD|Błąd|
|PSDNET-1284|Aktualizacja tekstu kończy się niepowodzeniem z niektórymi azjatyckimi symbolami. Błąd podczas analizy konkretnego symbolu|Błąd|
|PSDNET-1291|Aktualizacja tekstu kończy się niepowodzeniem z niektórymi azjatyckimi symbolami. Błąd podczas renderowania konkretnego symbolu|Błąd|
|PSDNET-1292|Błąd podczas otwierania pliku eksportowanego przez Photoshop po zapisaniu konkretnych azjatyckich symboli|Błąd|


## **Publiczne zmiany interfejsu API**
# **Dodane API:**
- Brak


# **Usunięte API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Przykłady użycia:**

**PSDNET-1071. Aspose.PSD nie może otworzyć pliku PSD (RGB/16-bit) z kompresją ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Efekty osi czasu znikały i pokazywały się w dziwny sposób (w Photoshopie)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Utwórz os czasu z kilkoma klatkami.
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

**PSDNET-1278. Przezroczystość nie działa dla efektu konturu z wewnętrzną pozycją**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regresja: Błąd podczas otwierania pliku PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Aktualizacja tekstu kończy się niepowodzeniem z niektórymi azjatyckimi symbolami. Błąd podczas analizy konkretnego symbolu**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // wybierz problematyczny symbol

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Usunięcie przestarzałych właściwości w Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Zaktualizuj opcję trybu mieszania efektu
    effect.BlendMode = BlendMode.Darken;

    // Zaktualizuj opcję przeźroczystości efektu
    effect.Opacity = 128; // 50%

    // Zaktualizuj opcję koloru wypełnienia efektu konturu
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Aktualizacja tekstu kończy się niepowodzeniem z niektórymi azjatyckimi symbolami. Błąd podczas renderowania konkretnego symbolu**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // wybierz problematyczne symbole

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Błąd podczas otwierania pliku eksportowanego przez Photoshop po zapisaniu konkretnych azjatyckich symboli**

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
