---
title: Aspose.PSD pro .NET 22.10 - Poznámky k vydání
type: docs
weight: 30
url: /cs/net/aspose-psd-pro-net-22-10-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Toto vydání má regresi ve případě exportů 16 bitů, proto doporučujeme opatrnost při používání této funkce v tomto vydání.
Prosím, neaktualizujte Aspose.PSD na verzi 22.9-22.10, pokud je zpracování obrazu s 16 bity vaší primární funkcionalitou.

Pracujeme na řešení těchto problémů.

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1287|Odebrání zastaralých vlastností v Lfx2Resource|Vylepšení|
|PSDNET-1071|Aspose.PSD nemůže otevřít PSD (RGB/16bit) s kompresí ZipWithoutPrediction|Chyba|
|PSDNET-1257|Časové osy zmizí a zobrazí se divným způsobem. (v Photoshopu)|Chyba|
|PSDNET-1278|Průhlednost nefunguje pro efekt postavy se zapuštěnou pozicí uvnitř|Chyba|
|PSDNET-1279|Regrese: Chyba při otevírání souboru PSD|Chyba|
|PSDNET-1284|Aktualizace textu selže s některými asijskými symboly. Chyba při analýze konkrétního symbolu|Chyba|
|PSDNET-1291|Aktualizace textu selže s některými asijskými symboly. Chyba při vykreslování konkrétního symbolu|Chyba|
|PSDNET-1292|Chyba při otevírání exportovaného souboru v programu Photoshop po uložení konkrétních asijských symbolů|Chyba|


## **Změny ve veřejném API**
# **Přidaná API:**
- žádné


# **Odebraná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Příklady použití:**

**PSDNET-1071. Aspose.PSD nemůže otevřít PSD (RGB/16bit) s kompresí ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Časové osy zmizí a zobrazí se divným způsobem. (v Photoshopu)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Vytvořte časovou osu s několika snímky.
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

**PSDNET-1278. Průhlednost nefunguje pro efekt postavy se zapuštěnou pozicí uvnitř**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regrese: Chyba při otevírání souboru PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Aktualizace textu selže s některými asijskými symboly. Chyba při analýze konkrétního symbolu**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // vyberte problematický symbol

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Odebrání zastaralých vlastností v Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Aktualizovat možnost BlendMode efektu
    effect.BlendMode = BlendMode.Darken;

    // Aktualizovat možnost Opacity efektu
    effect.Opacity = 128; // 50%

    // Aktualizovat možnost vyplnění barvy efektu Stroke
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Aktualizace textu selže s některými asijskými symboly. Chyba při vykreslování konkrétního symbolu**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // vyberte problematické symboly

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Chyba při otevírání exportovaného souboru v programu Photoshop po uložení konkrétních asijských symbolů**

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
