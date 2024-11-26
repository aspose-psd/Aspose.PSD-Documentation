---
title: Aspose.PSD dla .NET 20.3 - Notatki wydania
type: docs
weight: 100
url: /pl/net/aspose-psd-dla-net-20-3-notatki-wydania/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-188|Wsparcie dla .Net Core|Funkcja|
|PSDNET-523|Konwersja plików Adobe Illustrator do formatu PDF|Funkcja|
|PSDNET-212|Dodanie możliwości renderowania różnych stylów na jednej warstwie tekstowej|Funkcja|
|PSDNET-144|Wsparcie dla warstwy regulacji Czarno-Białej|Funkcja|
|PSDNET-233|Dodanie obsługi eksportu formatu AI (Wersja 8) do innych formatów|Funkcja|
|PSDNET-540|Wsparcie dla przetwarzania trybu mieszania PassThrough (używane tylko dla grup warstw).|Funkcja|
|PSDNET-539|Wyjątek: Ładowanie obrazu nie powiodło się podczas ładowania obrazu z pustymi nazwami alfa Unicode|Błąd|
|PSDNET-541|Nieprawidłowe wyjście po zmianie widoczności GrupyWarstw|Błąd|
|PSDNET-516|Wyjątek podczas ładowania obrazu PSD: Sekcja koloru (Zasób DropShadow) musi zawierać 3 składniki koloru dla RGB lub 4 składniki koloru dla CMYK|Błąd|
|PSDNET-536|Wyjątek przy próbie rysowania na nowo utworzonej warstwie, jeśli używana jest prosta wersja konstruktora|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **Usunięte API:**
- None

## **Przykłady użycia:**
**PSDNET-523. Konwersja plików Adobe Illustrator do formatu PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Dodanie możliwości renderowania różnych stylów na jednej warstwie tekstowej**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // edytuj styl tekstu "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // edytuj styl tekstu "2\r"

    newPortions[2].Style.FauxBold = true; // edytuj styl tekstu "Bold"

    newPortions[3].Style.FauxItalic = true; // edytuj styl tekstu "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // edytuj styl tekstu "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // edytuj styl tekstu "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Dodanie obsługi eksportu formatu AI (Wersja 8) do innych formatów**

{{< highlight java >}}

 // Przykład eksportu pliku AI do formatu PSD i PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Wsparcie dla przetwarzania trybu mieszania PassThrough (Używane tylko dla grup warstw).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Brak 23. warstwy.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "23. warstwa nie jest grupą warstw.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Nazwa 23. warstwy nie jest 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Warstwa AdjustmentGroup powinna mieć tryb mieszania 'pass through'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Aktualizacja tekstu warstwy tekstowej powoduje wyjątek**

{{< highlight java >}}

 // Aktualizacja tekstu warstwy tekstowej powoduje wyjątek

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. Zapis obrazu PSD po operacji RotateFlip powoduje uszkodzony plik, który nie może być otwarty.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Powinno zostać wykonane bez wyjątków

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Nie rób nic

}

{{< /highlight >}}

**PSDNET-539. Wyjątek: Ładowanie obrazu nie powiodło się podczas ładowania obrazu z pustymi nazwami alfa Unicode**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Tutaj nie powinno być wyjątków

{

    // nie rób nic

}

{{< /highlight >}}

**PSDNET-541. Nieprawidłowe wyjście po zmianie widoczności GrupyWarstw**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// dokonaj zmian w nazwach warstw i zapisz je

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Wyłącz wszystko wewnątrz grupy

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Wyjątek podczas ładowania obrazu PSD: Sekcja koloru (Zasób DropShadow) musi zawierać 3 składniki koloru dla RGB lub 4 składniki koloru dla CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Tutaj nie powinno być wyjątków

{

    // nie rób nic

}

{{< /highlight >}}

**PSDNET-536. Wyjątek jeśli spróbujesz rysować na nowo utworzonej warstwie, jeśli używana jest prosta wersja konstruktora**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // narysuj prostokąt za pomocą narzędzia Pióro

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // narysuj kolejny prostokąt z pędzlem Solid Brush w kolorze niebieskim

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}
