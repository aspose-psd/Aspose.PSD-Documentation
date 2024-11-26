---
title: Notatki dotyczące wydania Aspose.PSD for .NET 23.8
type: docs
weight: 50
url: /pl/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD for .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                            | **Kategoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Dodanie nowego typu zakrzywienia (Flaga) | Funkcja |
| PSDNET-1621 | Dodanie nowych typów zakrzywień: łuk w górę, łuk w dół, sfera | Funkcja |
| PSDNET-1682 | Implementacja nowej metody PsdImage.AddPosterizeAdjustmentLayer do dodawania nowej warstwy Plakatyzacji | Funkcja |
| PSDNET-913  | Utracone informacje PSD po prostym otwarciu i zapisaniu | Błąd     |
| PSDNET-1352 | Błąd podczas wczytywania obrazka | Błąd     |
| PSDNET-1553 | Błąd podczas wczytywania obrazka: Nie można rzutować obiektu typu UnknownStructure na typ DescriptorStructure | Błąd     |
| PSDNET-1631 | Plik zmieniony w bibliotece zewnętrznej uszkadza plik PSD, ale można go otworzyć w Photoshopie | Błąd     |


## **Zmiany w Publicznych API**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-913. Brakujące informacje PSD po prostym otwarciu i zapisaniu**

{{< highlight csharp >}}
string src = "PlikOryginalny.psd";
string outputPsd = "wyjsciowy_PlikOryginalny.psd";
string outputPng = "wyjsciowy_PlikOryginalny.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Błąd podczas wczytywania obrazka**

{{< highlight csharp >}}
string srcFile1 = "test_tekst.psd";
string srcFile2 = "test_inteligentny_obiekt.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Błąd podczas wczytywania obrazka: Nie można rzutować obiektu typu UnknownStructure na typ DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Powinno wczytać się poprawnie
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Plik zmieniony w bibliotece zewnętrznej uszkadza plik PSD, ale można go otworzyć w Photoshopie**

{{< highlight csharp >}}
string sourceFile = "wyjscie.psd";
string outputFile = "eksport.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Dodanie nowego typu zakrzywienia (Flaga)**

{{< highlight csharp >}}
string sourceFile = "flaga_zakrzywienie.psd";
string outputFile = "flaga_eksport.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Dodanie nowych typów zakrzywień: łuk w górę, łuk w dół, sfera**

{{< highlight csharp >}}
string sourceFileArcUpper = "zakrzywienie_luka_w_gore.psd";
string sourceFileArcLower = "zakrzywienie_luka_w_dol.psd";
string sourceFileBulge =  "zakrzywienie_sfera.psd";

string outputFileArcUpper ="eksport_LukWGore.png";
string outputFileArcLower = "eksport_LukWDol.png";
string outputFileBulge = "eksport_Sfera.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Implementacja nowej metody PsdImage.AddPosterizeAdjustmentLayer do dodawania nowej warstwy plakatyzacji**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Sprawdzenie zapisanych zmian
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Obiekty nie są równe.");
    }
}
{{< /highlight >}}
