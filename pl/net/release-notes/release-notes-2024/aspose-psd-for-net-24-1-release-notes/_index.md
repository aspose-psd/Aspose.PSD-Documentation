---
title: Aspose.PSD dla .NET 24.1 - Notatki dotyczące wersji
type: docs
weight: 120
url: /pl/net/aspose-psd-dla-net-24-1-notatki-dotyczace-wersji/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wersji [Aspose.PSD dla .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                  | **Kategoria** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [Format AI] Dodano podstawową obsługę wielostronicowych obrazów AI                               |   Funkcja    |
| PSDNET-718  | Efekt Tekstu zniekształcania nie jest stosowany do tekstu                                           |     Błąd     |
| PSDNET-1620 | Nieprawidłowe renderowanie maski w określonym pliku                                                |     Błąd     |
| PSDNET-1855 | Wyjątek NullReferenceException w Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor |     Błąd     |
| PSDNET-1883 | [Format AI] Poprawa zużycia pamięci w AiExporterUtils                                              |     Błąd     |



## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-718. Efekt Tekstu zniekształcania nie jest stosowany do tekstu**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Nieprawidłowe renderowanie maski w określonym pliku**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [Format AI] Dodanie podstawowej obsługi wielostronicowych obrazów AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Wczytaj obraz AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Domyślnie ActivePageIndex to 0.
    // Jeśli więc zapiszesz obraz AI bez zmiany tej właściwości, pierwsza strona zostanie wyrenderowana i zapisana.
    image.Save(firstPageOutputPng, new PngOptions());

    // Zmień indeks aktywnej strony na drugą stronę.
    image.ActivePageIndex = 1;

    // Zapisz drugą stronę obrazu AI jako obraz PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Zmień indeks aktywnej strony na trzecią stronę.
    image.ActivePageIndex = 2;

    // Zapisz trzecią stronę obrazu AI jako obraz PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. Wyjątek NullReferenceException w Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [Format AI] Poprawa zużycia pamięci w AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Wczytaj obraz AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Zapisz pierwszą stronę obrazu AI jako obraz PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // Zmień indeks aktywnej strony na drugą stronę.
    image.ActivePageIndex = 1;

    // Zapisz drugą stronę obrazu AI jako obraz PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Zmień indeks aktywnej strony na trzecią stronę.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Zużycie pamięci jest zbyt duże. " + memoryUsed + " zamiast " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
