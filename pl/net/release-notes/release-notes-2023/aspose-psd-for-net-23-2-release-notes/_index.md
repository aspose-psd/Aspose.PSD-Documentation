---
title: Aspose.PSD dla .NET 23.2 - Notatki dotyczące wydania
type: dokumentacja
weight: 110
url: /pl/net/aspose-psd-dla-net-23-2-notatki-dotyczace-wydania/
---

{{% alert kolor="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-1359|Praca nad renderowaniem tekstu w celu poprawy pozycjonowania, renderowania i obsługi|Usprawnienie|
|PSDNET-1270|Dodanie możliwości przetwarzania efektu Warp za pomocą publicznego API|Funkcja|
|PSDNET-1391|Dodanie obsługi trybów wiodących Od do Do i Do Do góry z ustawień akapitu|Funkcja|
|PSDNET-912|Zmiana czcionki i koloru dla warstwy tekstu PSD|Błąd|
|PSDNET-1022|Niepoprawne eksportowanie tekstu w teście TextUpdateTests, brak tekstu|Błąd|
|PSDNET-1221|Brak dodatkowo małego tekstu po zmianie rozmiaru większego obrazu PSD|Błąd|
|PSDNET-1301|Aspose.Psd dla .NET textLayer.UpdateText() drukuje '-' (myślnik) jako podkreślnik w losowy sposób dla różnych zestawów danych|Błąd|
|PSDNET-1379|Ustawienia rozdzielczości nie są stosowane podczas eksportowania z PSD do PDF|Błąd|


## **Zmiany w publicznym API**
# **Dodane API:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **Usunięte API:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Przykłady użycia:**

**PSDNET-912. Zmiana czcionki i koloru dla warstwy tekstu PSD**

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

**PSDNET-1022. Niepoprawne eksportowanie tekstu w teście TextUpdateTests, brak tekstu**

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
            layer.UpdateText("Tekst został zaktualizowany");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
