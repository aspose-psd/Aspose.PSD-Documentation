---
title: Aspose.PSD dla .NET 23.9 - Notatki wersji
type: docs
weight: 40
url: /pl/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wersji dla [Aspose.PSD dla .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**     | **Podsumowanie**                                                                                                                | **Kategoria** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Implementacja tworzenia maski dla nowych warstw dostosowujących                                                            | Funkcja |
| PSDNET-1654 | Dodaj obsługę Zmieszanych Warstw obcinanych jako opcję mieszania grupy                                                    | Funkcja |
| PSDNET-1194 | Plik PSD w trybie koloru 16 bitów nie stosuje maski dla warstw dostosowujących                                         | Błąd     |
| PSDNET-1235 | Nieprawidłowe renderowanie nawiasów w warstwie tekstowej                                                                   | Błąd     |
| PSDNET-1559 | Nie można aktualizować stylów w warstwach tekstowych                                                                       | Błąd     |
| PSDNET-1583 | Po wyeksportowaniu pliku PSD z CMYK łamie kolory w wyeksportowanym PSD                                                  | Błąd     |
| PSDNET-1619 | Określony plik PSB powoduje wyjątek "Prostokąt nie ma wspólnego obszaru przetwarzania"                                   | Błąd     |
| PSDNET-1648 | Błąd ładowania obrazu. OverflowException: Operacja arytmetyczna spowodowała przepełnienie                                | Błąd     |


## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **Usunięte API:**
- None


## **Przykłady użycia:**

**PSDNET-1638. Implementacja tworzenia maski dla nowych warstw dostosowujących**

{{< highlight csharp >}}
string srcFile = "zendeya_BW.psd";
string dstFile = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(dstFile);
}

using (var im = (PsdImage)Image.Load(dstFile))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Obiekty nie są równe.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Dodaj obsługę Zmieszanych Warstw obcinanych jako opcję mieszania grupy**

{{< highlight csharp >}}
string sourceFile = "przyklad_zrodlowy.psd";
string outputPsd = "przyklad_wyjsciowy.psd";
string outputPng = "przyklad_wyjsciowy.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. Plik PSD w trybie koloru 16 bitów nie stosuje maski dla warstw dostosowujących**

{{< highlight csharp >}}
string sourceFile = "zrodlo.psd";
string outputPng = "aktualny.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Nieprawidłowe renderowanie nawiasów w warstwie tekstowej**

{{< highlight csharp >}}
string file = "plik1.psd";
string output = "wyjscie_1235.png";

using (var psdImage = (PsdImage)Image.Load(file))
{
    foreach (var layer in psdImage.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = new PsdOptions(psdImage);
    psdImage.Save(output, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. Nie można aktualizować stylów w warstwach tekstowych**

{{< highlight csharp >}}
string sourceFile = "Przyklad_RozmiaruCzcionki.psd";
string outputFile = "wyjscie_Przyklad_RozmiaruCzcionki.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdImage.Layers[4];
    var l2 = (TextLayer)psdImage.Layers[5];

    var textItems1 = l1.TextData.ProducePortions(new string[] { "tekst1", "tekst2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var item in textItems1)
    {
        l1.TextData.AddPortion(item);
    }

    var textItems2 = l2.TextData.ProducePortions(new string[] { "warstwa tekstowa 1", "warstwa tekstowa 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1583. Po wyeksportowaniu pliku PSD z CMYK łamie kolory w wyeksportowanym PSD**

{{< highlight csharp >}}
string sourceFile = "kanion.psd";
string outputFilePng = "wyjscie_kanion.png";

using (var outputStream = new MemoryStream())
{
    using (var psdImage = (PsdImage)Image.Load(sourceFile))
    {
        psdImage.Save(outputStream);
    }

    outputStream.Position = 0;
    using (var psdImage = (PsdImage)Image.Load(outputStream))
    {
        psdImage.Save(outputFilePng, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Określony plik PSB powoduje wyjątek "Prostokąt nie ma wspólnego obszaru przetwarzania"**

{{< highlight csharp >}}
var input = "1619_zrodlo.psb";
var output = "1619_wyjscie.png";
using (PsdImage img = (PsdImage)Image.Load(input, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Błąd ładowania obrazu. OverflowException: Operacja arytmetyczna spowodowała przepełnienie**

{{< highlight csharp >}}
string sourceFile = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    Layer layer = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Obiekty nie są równe.");
    }
}
{{< /highlight >}}
