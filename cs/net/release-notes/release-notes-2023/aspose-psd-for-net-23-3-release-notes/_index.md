---
title: Aspose.PSD pro .NET 23.3 - Poznámky k vydání
type: docs
weight: 100
url: /cs/net/aspose-psd-pro-net-23-3-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-146|Podpora vrstvy úpravy Posterize|Funkce|
|PSDNET-1366|Implementovat podporu VscgResource|Funkce|
|PSDNET-1437|Přidat podporu zdroje PostResource pro data vrstvy úpravy Posterize|Funkce|
|PSDNET-931|Nesprávný export do vrstvy PNG s úpravou křivek a barevným režimem CMYK|Chyba|
|PSDNET-1403|Styl odstavce chybí po uložení souboru a aktualizaci souboru pomocí PS|Chyba|
|PSDNET-1453|Porušené vykreslování efektů záře a stínu na textu|Chyba|


## **Změny ve veřejném API**
# **Přidané API:**
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


# **Odebraná API:**
- Nic


## **Příklady použití:**

**PSDNET-146. Podpora vrstvy úpravy Posterize**

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

**PSDNET-931. Nesprávný export do vrstvy PNG s úpravou křivek a barevným režimem CMYK**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // the ', new PsdOptions()' provocating a bug.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Implementovat podporu VscgResource**

{{< highlight csharp >}}
string sourceFile = "StrokeInternalFill_src.psd";
string outputFile = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"Hodnoty nejsou stejné.\nOčekáváno:{expected}\nVýsledek:{current}\nRozdíl:{expected - current}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // Červená
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // Zelená
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // Modrá

    image.Save(outputFile);
}

// kontrola změn
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Styl odstavce chybí po uložení souboru a aktualizaci souboru pomocí PS**

{{< highlight csharp >}}
string sourceFile = "PSDTest3.psd";
string outputFile = "output.psd";

string[] newText = new string[]
{
    "Název \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer layer2 = image.AddTextLayer("Nová vrstva", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var textDataTL = layer2.TextData;

    ITextStyle defaultStyleTL = textDataTL.ProducePortion().Style;

    ITextParagraph defaultParagraphTL = textDataTL.ProducePortion().Paragraph;
    ITextPortion[] newPortionsTL = textDataTL.ProducePortions(newText, defaultStyleTL, defaultParagraphTL);

    newPortionsTL[0].Style.FontSize = 14;
    newPortionsTL[0].Style.FontName = "TwCenMT-Bold";

    newPortionsTL[1].Style.Leading = 20;
    newPortionsTL[1].Style.FontSize = 10;
    newPortionsTL[1].Style.FontName = "TwCenMT-Bold";

    // Odebrání starého textu
    textDataTL.RemovePortion(0);

    // Přidání nových textových částí
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

    string key0 = @" >> /6 0 >> >> /1 "; // prefix pro délku odstavce 0
    string key1 = @" >> /6 1 >> >> /1 "; // prefix pro délku odstavce 1
    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    string lenPar0 = txt2Data.Substring(index0 + key0.Length, 1);
    string lenPar1 = txt2Data.Substring(index1 + key1.Length, 3);

    string expected0 = newText[0].Length.ToString();
    string expected1 = (newText[1].Length + 1).ToString();

    if (lenPar0 != expected0 || lenPar1 != expected1)
    {
        throw new Exception(
            $"Délka odstavců je nesprávná.\nOčekáváno: {expected0} a {expected1}\nVýsledek: {lenPar0} a {lenPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Přidat podporu zdroje PostResource pro data vrstvy úpravy Posterize**

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

**PSDNET-1453. Porušené vykreslování efektů záře a stínu na textu**

{{< highlight csharp >}}
string outputPsd = "efekt_chyba.psd";
string outputPng = "efekt_chyba.png";

using (var psdImage = new PsdImage(500, 500))
{
    // Přidání textových vrstev
    Aspose.PSD.Rectangle textArea1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle textArea2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle textArea3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer textLayer1 = psdImage.AddTextLayer("Text s efekty", textArea1);
    TextLayer textLayer2 = psdImage.AddTextLayer("Text s efekty", textArea2);
    TextLayer textLayer3 = psdImage.AddTextLayer("Text s efekty", textArea3);

    // Úprava textových vrstev
    textLayer1.TextData.Items[0].Style.FontSize = 150;
    textLayer1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer1.TextData.UpdateLayerData();

    textLayer2.TextData.Items[0].Style.FontSize = 150;
    textLayer2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer2.TextData.UpdateLayerData();

    textLayer3.TextData.Items[0].Style.FontSize = 150;
    textLayer3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer3.TextData.UpdateLayerData();

    // Přidání efektů
    OuterGlowEffect glow = textLayer1.BlendingOptions.AddOuterGlow(); // praskne
    glow.Spread = 15;
    ((ColorFillSettings)glow.FillColor).Color = Color.Red;

    var shadow = textLayer2.BlendingOptions.AddDropShadow(); // praskne s dlouhým textem
    shadow.Distance = 25;
    shadow.Color = Color.DarkBlue;

    var innerShadow = textLayer3.BlendingOptions.AddInnerShadow(); // praskne s dlouhým textem
    innerShadow.UseGlobalLight = false;
    innerShadow.Angle = -179;
    innerShadow.Distance = 10;
    innerShadow.Size = 8;
    innerShadow.Color = Color.HotPink;

    // export
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}