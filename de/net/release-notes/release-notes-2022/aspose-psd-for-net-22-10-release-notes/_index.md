---
title: Aspose.PSD für .NET 22.10 - Versionshinweise
type: docs
weight: 30
url: /de/net/aspose-psd-fur-net-22-10-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Diese Version hat einen Rückschritt im Fall von 16-Bit-Exporten, daher empfehlen wir Vorsicht bei der Verwendung dieses Features in dieser Version. Bitte aktualisieren Sie Aspose.PSD nicht auf 22.9-22.10, wenn die Verarbeitung von 16-Bit-Bildern Ihre Hauptfunktionalität ist.

Wir arbeiten an Lösungen für diese Probleme.

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1287|Veraltete Eigenschaften in Lfx2Resource entfernen|Verbesserung|
|PSDNET-1071|Aspose.PSD kann PSD (RGB/16-Bit) mit ZipWithoutPrediction-Komprimierung nicht öffnen|Fehler|
|PSDNET-1257|Timeline-Effekte verschwinden und werden seltsam angezeigt. (in Photoshop)|Fehler|
|PSDNET-1278|Transparenz funktioniert nicht für den Strich-Effekt mit Innenposition|Fehler|
|PSDNET-1279|Regression: Fehler beim Öffnen der PSD-Datei|Fehler|
|PSDNET-1284|Das Aktualisieren des Texts schlägt mit einigen asiatischen Symbolen fehl. Fehler beim Parsen eines bestimmten Symbols|Fehler|
|PSDNET-1291|Das Aktualisieren des Texts schlägt mit einigen asiatischen Symbolen fehl. Fehler beim Rendern eines bestimmten Symbols|Fehler|
|PSDNET-1292|Fehler beim Öffnen der exportierten Datei durch Photoshop nach dem Speichern bestimmter asiatischer Symbole|Fehler|


## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- Keine


# **Entfernte APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Beispiele für die Verwendung:**

**PSDNET-1071. Aspose.PSD kann PSD (RGB/16-Bit) mit ZipWithoutPrediction-Komprimierung nicht öffnen**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Timeline-Effekte verschwinden und werden seltsam angezeigt. (in Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Timeline mit einigen Frames erstellen.
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

**PSDNET-1278. Transparenz funktioniert nicht für den Strich-Effekt mit Innenposition**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regression: Fehler beim Öffnen der PSD-Datei**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Das Aktualisieren des Texts schlägt mit einigen asiatischen Symbolen fehl. Fehler beim Parsen eines bestimmten Symbols**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // Das problematische Symbol auswählen

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Veraltete Eigenschaften in Lfx2Resource entfernen**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // BlendMode-Option des Effekts aktualisieren
    effect.BlendMode = BlendMode.Darken;

    // Opacity-Option des Effekts aktualisieren
    effect.Opacity = 128; // 50%

    // Füllfarbenoption des Strich-Effekts aktualisieren
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Das Aktualisieren des Texts schlägt mit einigen asiatischen Symbolen fehl. Fehler beim Rendern eines bestimmten Symbols**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // Die problematischen Symbole auswählen

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Fehler beim Öffnen der exportierten Datei durch Photoshop nach dem Speichern bestimmter asiatischer Symbole**

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
