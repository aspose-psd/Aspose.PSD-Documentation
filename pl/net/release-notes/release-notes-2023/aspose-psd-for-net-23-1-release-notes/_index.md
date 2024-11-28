---
title: Aspose.PSD dla .NET 23.1 - Notatki dotyczące wydania
type: docs
weight: 120
url: /pl/net/aspose-psd-dla-net-23-1-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-401|Wsparcie vstkResource|Funkcja|
|PSDNET-1346|Dodano edytowalną właściwość BaselineDirection/IsStandardVerticalRomanAlignmentEnabled do interfejsu IText|Funkcja|
|PSDNET-181|PSD nie jest poprawnie konwertowany do JPEG|Błąd|
|PSDNET-958|PSB do PDF nie działa dla dużych plików|Błąd|
|PSDNET-1171|Dodanie procesowania maski ograniczającej do warstwy korekty|Błąd|
|PSDNET-1252|Po zmianie rozmiaru całego obrazu, a następnie po zmianie rozmiaru określonej warstwy Aspose.PSD zgłasza wyjątek przy zapisywaniu warstwy|Błąd|


## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleMiterLimit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineJoinType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleScaleLock
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleStrokeAdjust
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleBlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleOpacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleResolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleContent
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashSet
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Levels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.TypeToolKey


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-181. PSD nie jest poprawnie konwertowany do JPEG**

{{< highlight csharp >}}
string srcFile = "helikopter.psd";
string outputJpg = "wyjscie.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. Wsparcie vstkResource**

{{< highlight csharp >}}
string srcFile = "TestKształtuSkoków1.psd";
string dstFile = "TestKształtuSkoków2.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile))
{
    Layer layer = image.Layers[1];
    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is VstkResource)
        {
            VstkResource zasóbVstk = (VstkResource)resource;
            zasóbVstk.StrokeStyleLineAlignment = StrokePosition.Outside;
            zasóbVstk.StrokeStyleLineWidth = 20;
        }
    }

    image.Save(dstFile);
}
{{< /highlight >}}

**PSDNET-958. PSB do PDF nie działa dla dużych plików**

{{< highlight csharp >}}
string ścieżkaWejściowa = "SteveKohli-SamochódTOP.psb";
string ścieżkaWyjściowa ="wyjście.pdf";

using (var obraz = Image.Load(ścieżkaWejściowa))
{
    obraz.Save(ścieżkaWyjściowa, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. Dodanie procesowania maski ograniczającej do warstwy korekty**

{{< highlight csharp >}}
string srcFile = "helikopter_czesc.psd";
string outputJpg = "wyjście.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. Po zmianie rozmiaru całego obrazu, a następnie po zmianie rozmiaru określonej warstwy Aspose.PSD zgłasza wyjątek przy zapisywaniu warstwy**

{{< highlight csharp >}}
string plikŹródłowy = "źródło.psd";
string imgPlik1 = "img1.png";
string imgPlik2 = "img2.png";

var opcjeŁadowania = new PsdLoadOptions()
{
    TrybTylkoDoOdczytu = false,
    ŁadowanieZasobówEfektów = true
};

using (var obraz = (PsdImage)Image.Load(plikŹródłowy, opcjeŁadowania))
{
    // Najpierw zmieniamy rozmiar całego obrazu
    obraz.Resize(110, 90);
    var warstwy = obraz.Layers;

    var warstwaOk = warstwy[0];
    warstwaOk.Resize(100, 80);

    var warstwaWyjątek = warstwy[1];
    warstwaWyjątek.Resize(100, 80);

    // Tutaj wszystko będzie w porządku
    warstwaOk.Save(imgPlik1, new PngOptions() { TypKoloru = PngColorType.PrawdziwykolorZAlfa });

    // Teraz tutaj wszystko będzie w porządku
    warstwaWyjątek.Save(imgPlik2, new PngOptions() { TypKoloru = PngColorType.PrawdziwykolorZAlfa });                
}
{{< /highlight >}}

**PSDNET-1346. Dodano edytowalną właściwość BaselineDirection/IsStandardVerticalRomanAlignmentEnabled do interfejsu IText**

{{< highlight csharp >}}
// Poniższy kod demonstruje możliwość edycji nowej właściwości IsStandardVerticalRomanAlignmentEnabled.
// Nie wpływa to na renderowanie, ale pozwala jedynie edytować wartość właściwości.

string źródło = "1346test.psd";
string wyjście = "wyjscie_1346test.psd";

using (var obraz = (PsdImage)Image.Load(źródło))
{
    var warstwaTekstowa = obraz.Layers[1] as TextLayer;
    var częśćTekstu = warstwaTekstowa.TextData.Items[0];
    if (częśćTekstu.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Poprawne odczytywanie
    }
    else
    {
        throw new Exception("Niepoprawne odczytywanie wartości właściwości IsStandardVerticalRomanAlignmentEnabled");
    }

    częśćTekstu.Style.IsStandardVerticalRomanAlignmentEnabled = false;
    warstwaTekstowa.TextData.UpdateLayerData();

    obraz.Save(wyjście);
}

using (var obraz = (PsdImage)Image.Load(wyjście))
{
    var warstwaTekstowa = obraz.Layers[1] as TextLayer;
    var częśćTekstu = warstwaTekstowa.TextData.Items[0];
    if (!częśćTekstu.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Poprawne odczytywanie
    }
    else
    {
        throw new Exception("Niepoprawne odczytywanie wartości właściwości IsStandardVerticalRomanAlignmentEnabled");
    }
}
{{< /highlight >}}
