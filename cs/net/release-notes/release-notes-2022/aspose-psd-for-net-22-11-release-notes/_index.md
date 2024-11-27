---
title: Vydání Aspose.PSD pro .NET 22.11
type: docs
weight: 20
url: /cs/net/aspose-psd-pro-net-22-11-poznamky-k-vydani
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

{{% alert color="warning" %}}

- Toto vydání má chybu ve funkci exportu 16bitových souborů, proto doporučujeme opatrnost při používání této funkce v této verzi.
Pokud je zpracování obrazu 16 bitů vaší primární funkcí, nedoporučujeme aktualizovat Aspose.PSD na verzi 22.9-22.11.

Pracujeme na řešení těchto problémů.

{{% /alert %}}

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1320|Nelze exportovat extrémně velké soubory PSB|Vylepšení|
|PSDNET-659|Umožnit pohyb středu radiálního průběhu|Funkce|
|PSDNET-1330|Nepodporovaná kompresní metoda ZipWithoutPrediction pro specifické soubory|Funkce|
|PSDNET-735|Po použití metody transformace pouze pro vrstvu má uložená vrstva nesprávný ohraničující obdélník|Chyba|
|PSDNET-1234|Výjimka při načítání obrazu PSD se vzorem|Chyba|
|PSDNET-1244|Selhání exportu obrazu (IndexOutOfRangeException) při ukládání souboru PSD s čínskými symboly|Chyba|
|PSDNET-1303|Aplikace TimeLine ActiveFrame aplikuje nesprávně|Chyba|
|PSDNET-1307|Regrese 22.7: nesprávné vykreslování textu s arabskými znaky|Chyba|
|PSDNET-1321|Vektorová maska na vrstvě skupiny funguje nesprávně. Konečný obraz má černou díru, ale neměl by mít|Chyba|


## **Veřejné změny API**
# **Přidaná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Odebraná API:**
- Žádné


## **Příklady použití:**

**PSDNET-659. Umožnit pohyb středu radiálního průběhu**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "vystup.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // Aktualizace bodu posunu
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Po použití metody transformace pouze pro vrstvu má uložená vrstva nesprávný ohraničující obdélník**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // Nastavení nové velikosti textové vrstvy
    const int NewWidth = 250;
    const int NewHeight = 250;

    // Nastavení mechanismu, jak bude funkce resize měnit velikost vrstvy (výchozí hodnota)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // Nový mechanismus změny velikosti textové vrstvy
    // Budou změněny nejen vrstvy, ale také transformační matice textové vrstvy
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // Důvodem deltou je jiný výchozí font
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // Vše je v pořádku
    }
    else
    {
        throw new Exception("Umístění bodu je nesprávné");
    }
}
{{< /highlight >}}

**PSDNET-1234. Výjimka při načítání obrazu PSD se vzorem**

{{< highlight csharp >}}
string srcFile = "test.psd";
string output = "vystup1234.png";

using (PsdImage psdImage = (PsdImage)PsdImage.Load(srcFile,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdImage.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1244. Selhání exportu obrazu (IndexOutOfRangeException) při ukládání souboru PSD s čínskými symboly**

{{< highlight csharp >}}
string sourceFile = "vstup.psd";
string outputPath = "vystup.psd";

var loadOptions = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    foreach (var layer in image.Layers)
    {
        if (layer.Name == "1")
        {
            var txtLayer = (TextLayer)layer;

            txtLayer.UpdateText("测试测试");
        }
    }

    // Zde by nemělo dojít k výjimce.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. Aplikace TimeLine ActiveFrame aplikuje nesprávně**

{{< highlight csharp >}}
string src = "casovy_ramec1303.psd";
string vystup = "out_timeline.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdImage);

    psdImage.Save(vystup);
}
{{< /highlight >}}

**PSDNET-1307. Regrese 22.7: nesprávné vykreslování textu s arabskými znaky**

{{< highlight csharp >}}
string testovaciSlozkaFontu = "Fonts";
FontSettings.SetFontsFolder(testovaciSlozkaFontu);
FontSettings.UpdateFonts();

string sourceFilePath = "sarbarg.fin12.psd";
string outputFilePath = "vysledek.tiff";

using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
{
    psdImage.Save(outputFilePath, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Nelze exportovat extrémně velké soubory PSB**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321.  Vektorová maska na vrstvě skupiny funguje nesprávně. Konečný obraz má černou díru, ale neměl by mít**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. Nepodporovaná kompresní metoda ZipWithoutPrediction pro specifické soubory**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.PSD";
string outputFile = "20221017_220706_0000.Jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
