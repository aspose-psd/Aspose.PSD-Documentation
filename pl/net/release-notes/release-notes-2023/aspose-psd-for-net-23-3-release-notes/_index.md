---
title: Notatki wydania Aspose.PSD dla .NET 23.3
type: docs
weight: 100
url: /pl/net/aspose-psd-dla-net-23-3-notatki-o-wydaniu/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-146|Wsparcie dla Warstwy Dostosowania Posterize|Funkcja|
|PSDNET-1366|Wdrożenie obsługi VscgResource|Funkcja|
|PSDNET-1437|Dodanie obsługi zasobu PostResource dla danych Warstwy Dostosowania Posterize|Funkcja|
|PSDNET-931|Niepoprawny eksport na warstwę PNG z dostosowaniem krzywych i trybem kolorów CMYK|Błąd|
|PSDNET-1403|Styl akapitu zaginął po zapisaniu pliku i aktualizacji pliku przez PS|Błąd|
|PSDNET-1453|Uszkodzone renderowanie efektów świetlnych i cieni na tekście|Błąd|


## **Zmiany w API publicznym**
# **Nowe interfejsy API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **Usunięte interfejsy API:**
- Brak


## **Przykłady użycia:**

**PSDNET-146. Wsparcie dla Warstwy Dostosowania Posterize**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    foreach (Layer layer in image.Layers)
    {
        if (layer is PosterizeLayer)
        {
            ((PosterizeLayer)layer).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Niepoprawny eksport na warstwę PNG z dostosowaniem krzywych i trybem kolorów CMYK**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // ', new PsdOptions()' wywołuje błąd.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Wdrożenie obsługi VscgResource**

{{< highlight csharp >}}
string sourceFile = "StrokeInternalFill_src.psd";
string outputFile = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"Wartości nie są równe.\nOczekiwano:{expected}\nWynik:{current}\nRóżnica:{expected - current}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // Czerwony
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // Zielony
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // Niebieski

    image.Save(outputFile);
}

// Sprawdzenie zmian
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Styl akapitu zaginął po zapisaniu pliku i aktualizacji pliku przez PS**

{{< highlight csharp >}}
string sourceFile = "PSDTest3.psd";
string outputFile = "output.psd";

string[] newText = new string[]
{
    "Tytuł \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer layer2 = image.AddTextLayer("Nowa warstwa", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var textDataTL = layer2.TextData;

    ITextStyle defaultStyleTL = textDataTL.ProducePortion().Style;

    ITextParagraph defaultParagraphTL = textDataTL.ProducePortion().Paragraph;
    ITextPortion[] newPortionsTL = textDataTL.ProducePortions(newText, defaultStyleTL, defaultParagraphTL);

    newPortionsTL[0].Style.FontSize = 14;
    newPortionsTL[0].Style.FontName = "TwCenMT-Bold";

    newPortionsTL[1].Style.Leading = 20;
    newPortionsTL[1].Style.FontSize = 10;
    newPortionsTL[1].Style.FontName = "TwCenMT-Bold";

    // Usunięcie starego tekstu
    textDataTL.RemovePortion(0);

    // Dodanie nowych fragmentów tekstu
    foreach (var newPortion in newPortionsTL)
    {
        textDataTL.AddPortion(newPortion);
    }

    textDataTL.UpdateLayerData();

    image.Save(outputFile);
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(outputFile))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Data += (char)bytes[i];
    }

    string key0 = @" >> /6 0 >> >> /1 "; // prefiks do długości akapitu 0
    string key1 = @" >> /6 1 >> >> /1 "; // prefiks do długości akapitu 1
    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    string lenPar0 = txt2Data.Substring(index0 + key0.Length, 1);
    string lenPar1 = txt2Data.Substring(index1 + key1.Length, 3);

    string expected0 = newText[0].Length.ToString();
    string expected1 = (newText[1].Length + 1).ToString();

    if (lenPar0 != expected0 || lenPar1 != expected1)
    {
        throw new Exception(
            $"Długość akapitów jest niepoprawna.\nOczekiwano: {expected0} i {expected1}\nWynik: {lenPar0} i {lenPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Dodanie obsługi zasobu PostResource dla danych Warstwy Dostosowania Posterize**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];

    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is PostResource)
        {
            ((PostResource)resource).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Uszkodzone renderowanie efektów świetlnych i cieni na tekście**

{{< highlight csharp >}}
string outputPsd = "efekt_bug.psd";
string outputPng = "efekt_bug.png";

using (var psdImage = new PsdImage(500, 500))
{
    // Dodaj warstwy tekstu
    Aspose.PSD.Rectangle obszarTekstu1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle obszarTekstu2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle obszarTekstu3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer warstwaTekstu1 = psdImage.AddTextLayer("Tekst z efektami", obszarTekstu1);
    TextLayer warstwaTekstu2 = psdImage.AddTextLayer("Tekst z efektami", obszarTekstu2);
    TextLayer warstwaTekstu3 = psdImage.AddTextLayer("Tekst z efektami", obszarTekstu3);

    // Modyfikuj warstwy tekstu
    warstwaTekstu1.TextData.Items[0].Style.FontSize = 150;
    warstwaTekstu1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    warstwaTekstu1.TextData.UpdateLayerData();

    warstwaTekstu2.TextData.Items[0].Style.FontSize = 150;
    warstwaTekstu2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    warstwaTekstu2.TextData.UpdateLayerData();

    warstwaTekstu3.TextData.Items[0].Style.FontSize = 150;
    warstwaTekstu3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    warstwaTekstu3.TextData.UpdateLayerData();

    // Dodaj efekty
    OuterGlowEffect blask = warstwaTekstu1.BlendingOptions.AddOuterGlow(); // łamie
    blask.Spread = 15;
    ((ColorFillSettings)blask.FillColor).Color = Color.Red;

    var cień = warstwaTekstu2.BlendingOptions.AddDropShadow(); // łamie z długim tekstem
    cień.Distance = 25;
    cień.Color = Color.DarkBlue;

    var wewnętrznyCień = warstwaTekstu3.BlendingOptions.AddInnerShadow(); // łamie z długim tekstem
    wewnętrznyCień.UseGlobalLight = false;
    wewnętrznyCień.Angle = -179;
    wewnętrznyCień.Distance = 10;
    wewnętrznyCień.Size = 8;
    wewnętrznyCień.Color = Color.HotPink;

    // eksport
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}