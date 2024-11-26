---
title: Notatki wydania Aspose.PSD dla .NET 24.6
type: docs
weight: 70
url: /pl/net/aspose-psd-dla-net-24-6-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                         | **Kategoria** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | Wprowadzenie obsługi warstwy mapy gradientów                                                                               | Funkcja      |
| PSDNET-1670 | [Format AI] Dodanie obsługi metadanych XPacket do formatu AI                                                                               | Funkcja      |
| PSDNET-1831 | Wprowadzenie wsparcia dla typów deformacji: Rozciąganie, Uciskanie i Zwijanie                                                                               | Funkcja      |
| PSDNET-1653 | Tryby RGB i Lab nie mogą zawierać mniej niż 3 kanałów i więcej niż 4 kanałów w plikach z warstwami ArtBoard                                                                               | Błąd      |
| PSDNET-1775 | Górna część obszaru przetwarzania musi być dodatnia. (Parametr 'areaToProcess') podczas przetwarzania konkretnego pliku                                                                               | Błąd      |
| PSDNET-2052 | Rozszerzony obraz poza płótnem jest przycinany po zapisaniu. Dane są tracone, ale podgląd wygląda poprawnie                                                                               | Błąd      |

## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDNET-1450. Wprowadzenie obsługi warstwy mapy gradientów**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // Dodaj warstwę dostosowania mapy gradientu.
    GradientMapLayer warstwa = im.AddGradientMapAdjustmentLayer();
    warstwa.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// Sprawdź zapisane zmiany
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer warstwaMapyGradientu = im.Layers[1] as GradientMapLayer;
    GradientFillSettings ustawieniaGradientu = (GradientFillSettings)warstwaMapyGradientu.GradientSettings;

    AssertAreEqual(0.0, ustawieniaGradientu.Angle);
    AssertAreEqual((short)4096, ustawieniaGradientu.Interpolation);
    AssertAreEqual(true, ustawieniaGradientu.Reverse);
    AssertAreEqual(false, ustawieniaGradientu.AlignWithLayer);
    AssertAreEqual(false, ustawieniaGradientu.Dither);
    AssertAreEqual(GradientType.Linear, ustawieniaGradientu.GradientType);
    AssertAreEqual(100, ustawieniaGradientu.Scale);
    AssertAreEqual(0.0, ustawieniaGradientu.HorizontalOffset);
    AssertAreEqual(0.0, ustawieniaGradientu.VerticalOffset);
    AssertAreEqual("Custom", ustawieniaGradientu.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Obiekty nie są równe.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [Format AI] Dodanie obsługi metadanych XPacket do formatu AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Obiekty nie są równe.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("Obiekt testowy jest nullem.");
    }
}

string kluczCreatorTool = ":CreatorTool";
string kluczNPages = "xmpTPg:NPages";
string kluczUnit = "stDim:unit";
string kluczHeight = "stDim:h";
string kluczWidth = "stDim:w";

string oczekiwanyCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string oczekiwaneNPages = "1";
string oczekiwanyUnit = "Piksele";
double oczekiwanaWysokość = 768;
double oczekiwanaSzerokość = 1366;

using (AiImage obraz = (AiImage)Image.Load(sourceFile))
{
    // Metadane Xmp zostały dodane.
    var xmpMetaData = obraz.XmpData;

    AssertIsNotNull(xmpMetaData);

    // Teraz można uzyskać dostęp do pakietów Xmp plików AI.
    var podstawowyPakiet = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var pakiet = xmpMetaData.Packages[4];

    // I mamy dostęp do zawartości tych pakietów.
    var creatorTool = podstawowyPakiet[kluczCreatorTool].ToString();
    var nPages = pakiet[kluczNPages];
    var unit = pakiet[kluczUnit];
    var height = double.Parse(pakiet[kluczHeight].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(pakiet[kluczWidth].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, oczekiwanyCreatorTool);
    AssertAreEqual(nPages, oczekiwaneNPages);
    AssertAreEqual(unit, oczekiwanyUnit);
    AssertAreEqual(height, oczekiwanaWysokość);
    AssertAreEqual(width, oczekiwanaSzerokość);
}
{{< /highlight >}}

**PSDNET-1831. Wprowadzenie wsparcia dla typów deformacji: Rozciąganie, Uciskanie i Zwijanie**

{{< highlight csharp >}}
string[] pliki = { "Zwijanie", "Uciskanie", "Uciskanie_vert", "Rozciąganie" };

foreach (string prefix in pliki)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var obrazPsd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        obrazPsd.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Tryby RGB i Lab nie mogą zawierać mniej niż 3 kanałów i więcej niż 4 kanałów w plikach z warstwami ArtBoard**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage obraz = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // Tutaj nie powinno być wyjątku
    obraz.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. Górna część obszaru przetwarzania musi być dodatnia. (Parametr 'areaToProcess') podczas przetwarzania konkretnego pliku**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions opcjePsdLoad = new PsdLoadOptions();
opcjePsdLoad.LoadEffectsResource = true;
opcjePsdLoad.AllowWarpRepaint = true;
using (PsdImage obraz = (PsdImage)PsdImage.Load(sourceFile, opcjePsdLoad))
{
    obraz.Save(outputFile);
    // Nie powinien być wyjątek
}
{{< /highlight >}}

**PSDNET-2052. Rozszerzony obraz poza płótnem jest przycinany po zapisaniu. Dane są tracone, ale Podgląd wygląda poprawnie**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions opcjeOdczytu = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var obrazPsd = (PsdImage)Image.Load(sourceFile, opcjeOdczytu))
{
    // Tutaj nie powinien być błąd
    obrazPsd.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var obrazPsd = (PsdImage)Image.Load(outputFile, opcjeOdczytu))
{
    obrazPsd.Resize(obrazPsd.Width / 10, obrazPsd.Height / 10);

    // Tutaj nie powinno być błędu
    obrazPsd.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
