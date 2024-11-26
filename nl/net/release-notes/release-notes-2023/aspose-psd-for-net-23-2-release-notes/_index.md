---
title: Aspose.PSD voor .NET 23.2 - Release-opmerkingen
type: docs
weight: 110
url: /nl/net/aspose-psd-voor-net-23-2-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-1359|Herwerken van tekstweergave om tekstpositionering, weergave en ondersteuning te verbeteren|Verbetering|
|PSDNET-1270|Toevoegen van mogelijkheid om Warp-effect te verwerken via de openbare API|Functie|
|PSDNET-1391|Toevoegen van ondersteuning voor Leidingsmodi Van onder naar onder en Van boven naar boven vanuit Alinea-instellingen|Functie|
|PSDNET-912|Lettertype en kleur wijzigen voor TextLayer PSD|Fout|
|PSDNET-1022|Onjuiste export van tekst bij test TextUpdateTests, tekst ontbreekt|Fout|
|PSDNET-1221|Extra kleine tekst ontbreekt na het verkleinen van de grotere PSD-afbeelding|Fout|
|PSDNET-1301|Aspose.Psd voor .NET textLayer.UpdateText() print '-' (streepje) als underscore op willekeurige wijze voor verschillende datasets|Fout|
|PSDNET-1379|ResolutionSettings worden niet toegepast bij exporteren van PSD naar PDF|Fout|


## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **Verwijderde API's:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Gebruik voorbeelden:**

**PSDNET-912. Lettertype en kleur wijzigen voor TextLayer PSD**

{{< highlight csharp >}}
string fontsFolder = "Fonts";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "result.psd";
string outputPng = "result.png";

FontSettings.SetFontsFolder(fontsFolder);

using (var image = (PsdImage)Image.Load(srcFile))
{
    TextLayer nameLayer = (TextLayer)image.Layers[9];
    var textPortion = nameLayer.TextData.Items[0];

    textPortion.Text = "MODESTO SR";
    textPortion.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textPortion.Style.FillColor = Color.Red;

    nameLayer.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Onjuiste export van tekst bij test TextUpdateTests, tekst ontbreekt**

{{< highlight csharp >}}
string srcFile = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var image = (PsdImage)Image.Load(srcFile))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var layer = image.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("Tekst is bijgewerkt");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Extra kleine tekst ontbreekt na het verkleinen van de grotere PSD-afbeelding**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Toevoegen van mogelijkheid om Warp-effect te verwerken via de openbare API**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string pngWarpedExport = "warped.png";
string psdWarpedExport = "warpFile.psd";

var warpLoadOptions = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(sourceFile, warpLoadOptions))
{
    image.Save(pngWarpedExport, new PngOptions());
    image.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd voor .NET textLayer.UpdateText() print '-' (streepje) als underscore op willekeurige wijze voor verschillende datasets**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "NAAM":
                    textLayer.UpdateText("Dhr. Jack Smith");
                    break;
                case "IDNR":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "FUNCTIE":
                    textLayer.UpdateText("AMBTENAAR-001");
                    break;
                case "BLOEDGROEP":
                    textLayer.UpdateText("AB-");
                    break;
                case "ADRES":
                    textLayer.UpdateText("BLOK-A, STRAAT-7, WONING NR - 047, SECTOR-024");
                    break;
                case "PERMADRES":
                    textLayer.UpdateText("HUIS NR - 42, LANE -025, PALM GREENS VIEW HOUSING SOCIETY, SECTOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. ResolutionSettings worden niet toegepast bij exporteren van PSD naar PDF**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var image = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting resolutionSetting = new ResolutionSetting(300, 300);

    image.Save(output, new PdfOptions()
    {
        ResolutionSettings = resolutionSetting
    });
}
{{< /highlight >}}

**PSDNET-1391. Toevoegen van ondersteuning voor Leidingsmodi Van onder naar onder en Van boven naar boven vanuit Alinea-instellingen**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var textPortion in text1.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.TopToTop; // LeidingsType waarde wijzigen   
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var textPortion in text2.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.BottomToBottom; // LeidingsType waarde wijzigen   
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}
