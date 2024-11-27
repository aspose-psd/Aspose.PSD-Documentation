---
title: Aspose.PSD pro .NET 22.12 - Poznámky k vydání
type: docs
weight: 10
url: /cs/net/aspose-psd-pro-net-22-12-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- V této verzi byla opravena regrese s exportem 16bitového obrázku.

{{% /alert %}}

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1336|Přidat editovatelnou vlastnost TextOrientation k rozhraní IText|Funkce|
|PSDNET-725|Změna velikosti určeného souboru PSD s maskou vrstvy vytváří nesprávnou masku|Chyba|
|PSDNET-1277|Přidat schopnost uložit a načíst masku pro 16 obrázků|Chyba|
|PSDNET-1281|Nesprávná průhlednost při ukládání 16bitového obrázku do 16 nebo 8 bitového obrázku|Chyba|
|PSDNET-1375|Oprava CMYK ve 16bitové barvě|Chyba|


## **Změny ve veřejném API**
# **Přidaná API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Odebraná API:**
- Žádná


## **Příklady použití:**

**PSDNET-725. Změna velikosti určeného souboru PSD s maskou produkuje nesprávnou masku**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Otevře zdrojový soubor PSD
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // Provede změnu velikosti
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Otevře soubor PSD po změně velikosti
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Převede na PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Přidání schopnosti uložit a načíst masku pro 16 obrázků**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Volby umožňují uložit 16bitovou barvu
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Soubor PSD se uloží s průhledností
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. Nesprávná průhlednost při ukládání 16bitového obrázku do 16 nebo 8 bitového obrázku**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// 16bitový barevný soubor PSD (s průhledností) bude otevřen a uložen ve 16bitové barvě
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// Uložený soubor PSD ve 16bitové barvě bude renderován do png souboru s průhledností
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Přidat editovatelnou vlastnost TextOrientation k rozhraní IText**

{{< highlight csharp >}}
// Následující kód demonstruje schopnost editovat novou vlastnost TextOrientation.
// Toto v současné době neovlivní kreslení, ale pouze vám umožní editovat hodnotu vlastnosti.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Správné čtení
    }
    else
    {
        throw new Exception("Nesprávné čtení hodnoty vlastnosti TextOrientation");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Správné čtení
    }
    else
    {
        throw new Exception("Nesprávné čtení hodnoty vlastnosti TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Oprava CMYK ve 16bitové barvě**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Nastaví konverzní možnosti
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Převede a uloží
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// Otevře konvertovaný soubor a vyrendruje do PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
