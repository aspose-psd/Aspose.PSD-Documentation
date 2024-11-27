---
title: Vydání Aspose.PSD pro .NET 23.2
type: docs
weight: 110
url: /cs/net/aspose-psd-pro-net-23-2-release-notes/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1359|Přepracování vykreslování textu pro zlepšení pozicování, vykreslování a podporu|Vylepšení|
|PSDNET-1270|Přidána možnost zpracovat efekt Warping přes veřejné API|Funkce|
|PSDNET-1391|Přidána podpora režimů vodících čar Bottom-to-bottom a Top-to-Top z nastavení odstavce|Funkce|
|PSDNET-912|Změna písma a barvy pro TextLayer PSD|Chyba|
|PSDNET-1022|Nesprávný export textu v testu TextUpdateTests, text chybí|Chyba|
|PSDNET-1221|Po změně velikosti většího obrázku PSD chybí extra malý text|Chyba|
|PSDNET-1301|Aspose.Psd pro .NET textLayer.UpdateText() tiskne '-' (pomlčku) jako podtržítko v náhodném způsobu pro různá data|Chyba|
|PSDNET-1379|Nastavení rozlišení se nepoužívá při exportu z PSD do PDF|Chyba|


## **Změny v veřejném API**
# **Přidaná API:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **Odebraná API:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Příklady použití:**

**PSDNET-912. Změna písma a barvy pro TextLayer PSD**

{{< highlight csharp >}}
string složkaPísem = "Fonts";
string srcSoubor = "M1PDTT26052021001.psd";
string výstupníPsd = "výsledek.psd";
string výstupPng = "výsledek.png";

FontSettings.SetFontsFolder(složkaPísem);

using (var obrázek = (PsdImage)Image.Load(srcSoubor))
{
    TextLayer vlastníNázevVrstvy = (TextLayer)obrázek.Layers[9];
    var textováČást = vlastníNázevVrstvy.TextData.Items[0];

    textováČást.Text = "MODESTO SR";
    textováČást.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textováČást.Style.FillColor = Color.Red;

    vlastníNázevVrstvy.TextData.UpdateLayerData();

    obrázek.Save(výstupníPsd);
    obrázek.Save(výstupPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Nesprávný export textu v testu TextUpdateTests, text chybí**

{{< highlight csharp >}}
string srcSoubor = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var obrázek = (PsdImage)Image.Load(srcSoubor))
{
    for (int i = 0; i < obrázek.Layers.Length; i++)
    {
        var vrstva = obrázek.Layers[i] as TextLayer;

        if (vrstva != null)
        {
            vrstva.UpdateText("Text je aktualizován");
        }
    }

    obrázek.Save(outputPsd);
    obrázek.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Po změně velikosti většího obrázku PSD chybí extra malý text**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdObrázek = (PsdImage)Image.Load(src))
{
    psdObrázek.Resize(30, 30);

    psdObrázek.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Přidání možnosti zpracovat efekt Warping přes veřejné API**

{{< highlight csharp >}}
string zdrojovýSoubor = "source.psd";
string pngWarpedExport = "warped.png";
string psdWarpedExport = "warpFile.psd";

var warpLoadOptions = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var obrázek = (PsdImage)Image.Load(zdrojovýSoubor, warpLoadOptions))
{
    obrázek.Save(pngWarpedExport, new PngOptions());
    obrázek.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd pro .NET textLayer.UpdateText() tiskne '-' (pomlčku) jako podtržítko v náhodném způsobu pro různá data**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdObrázek = (PsdImage)Image.Load(src))
{
    foreach (var vrstva in psdObrázek.Layers.Where(x => x.IsVisible))
    {
        if (vrstva is TextLayer)
        {
            TextLayer textováVrstva = vrstva as TextLayer;
            switch (vrstva.Name.Trim().ToUpper())
            {
                case "JMÉNO":
                    textováVrstva.UpdateText("PAN JACK SMITH");
                    break;
                case "ČÍSLO":
                    textováVrstva.UpdateText("OFF-022/GRP - 016");
                    break;
                case "FUNKCE":
                    textováVrstva.UpdateText("ÚŘADNÍK-001");
                    break;
                case "KREVNÍ SKUPINA":
                    textováVrstva.UpdateText("AB-");
                    break;
                case "ADRESA":
                    textováVrstva.UpdateText("BLOK-A, ULICE-7, APARTMÁN Č. - 047, SEKTOR-024");
                    break;
                case "TRVALÁ ADRESA":
                    textováVrstva.UpdateText("DŮM Č. - 42, ULICE -025, PALM GREENS VIEW HOUSING SOCIETY, SEKTOR - 45");
                    break;
            }
        }
    }

    psdObrázek.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. Nastavení rozlišení se nepoužívá při exportu z PSD do PDF**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var obrázek = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting resolutionSetting = new ResolutionSetting(300, 300);

    obrázek.Save(output, new PdfOptions()
    {
        ResolutionSettings = resolutionSetting
    });
}
{{< /highlight >}}

**PSDNET-1391. Přidání podpory režimů vodících čar Bottom-to-bottom a Top-to-Top z nastavení odstavce**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var psdObrázek = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdObrázek.Layers[1]).TextData;
    foreach (var textováČást in text1.Items)
    {
        textováČást.Paragraph.LeadingType = LeadingType.TopToTop; // Změna hodnoty vodícího režimu
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdObrázek.Layers[2]).TextData;
    foreach (var textováČást in text2.Items)
    {
        textováČást.Paragraph.LeadingType = LeadingType.BottomToBottom; // Změna hodnoty vodícího režimu
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdObrázek.Save(output, new PngOptions());
}
{{< /highlight >}}
