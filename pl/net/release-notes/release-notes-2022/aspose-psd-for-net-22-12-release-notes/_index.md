---
title: Aspose.PSD dla .NET 22.12 - Notatki dotyczące wydania
type: docs
weight: 10
url: /pl/net/aspose-psd-dla-net-22-12-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- W tym wydaniu naprawiono regresję związana z eksportem 16-bitowym.

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-1336|Dodaj edytowalną właściwość TextOrientation do interfejsu IText|Funkcja|
|PSDNET-725|Zmiana rozmiaru określonego pliku PSD z maską warstwy powoduje niepoprawną maskę|Błąd|
|PSDNET-1277|Dodaj możliwość zapisywania i wczytywania maski dla 16 obrazków|Błąd|
|PSDNET-1281|Niepoprawna przejrzystość podczas zapisywania obrazu 16-bitowego do obrazu 16- lub 8-bitowego|Błąd|
|PSDNET-1375|Naprawa koloru CMYK w 16-bitowym kolorze|Błąd|


## **Zmiany w API publicznym**
# **Dodane API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-725. Zmiana rozmiaru określonego pliku PSD z maską warstwy powoduje niepoprawną maskę**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Otwiera plik źródłowy PSD
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Skala = 4;

    int nowaSzerokosc = image.Width * Skala;
    int nowaWysokosc = image.Height * Skala;

    // Dokonuje zmiany rozmiaru
    image.Resize(nowaSzerokosc, nowaWysokosc);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Otwiera plik PSD po zmianie rozmiaru
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Renderuje do formatu PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Dodaj możliwość zapisywania i wczytywania maski dla 16 obrazków**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Opcje pozwalają na zapis koloru 16-bitowego
    PsdOptions opcje16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Plik PSD zostanie zapisany z przejrzystością
    image.Save(output16bitPsdFile, opcje16);
}
{{< /highlight >}}

**PSDNET-1281. Niepoprawna przejrzystość podczas zapisywania obrazu 16-bitowego do obrazu 16- lub 8-bitowego**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// 16-bitowy plik psd koloru (z przejrzystością) zostanie otwarty i zapisany jako kolor 16-bitowy
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions opcje16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, opcje16);
}

// Zapisany jako 16-bitowy plik psd kolor zostanie przekonwertowany na plik png z przejrzystością
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Dodaj edytowalną właściwość TextOrientation do interfejsu IText**

{{< highlight csharp >}}
// Poniższy kod demonstruje możliwość edytowania nowej właściwości TextOrientation.
// Nie wpływa to obecnie na renderowanie, ale pozwala jedynie edytować wartość właściwości.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var warstwaTekstu = image.Layers[1] as TextLayer;
    if (warstwaTekstu.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Prawidłowe odczytywanie
    }
    else
    {
        throw new Exception("Nieprawidłowe odczytywanie wartości właściwości TextOrientation");
    }

    warstwaTekstu.TextData.TextOrientation = TextOrientation.Horizontal;
    warstwaTekstu.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var warstwaTekstu = image.Layers[1] as TextLayer;
    if (warstwaTekstu.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Prawidłowe odczytywanie
    }
    else
    {
        throw new Exception("Nieprawidłowe odczytywanie wartości właściwości TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Naprawa koloru CMYK w 16-bitowym kolorze**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Ustawia opcje konwersji
PsdOptions opcjePsd = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Konwertuje i zapisuje
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(opcjePsd);
    image.Save(exportPath);
}

// Otwiera skonwertowany plik i renderuje do PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
