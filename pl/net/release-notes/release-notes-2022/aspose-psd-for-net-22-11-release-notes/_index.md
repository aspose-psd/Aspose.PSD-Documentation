---
title: Notatki do wersji Aspose.PSD dla .NET 22.11
type: docs
weight: 20
url: /pl/net/aspose-psd-dla-net-22-11-notatki-ko%C5%84cowe/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki do wersji [Aspose.PSD dla .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- W tej wersji występuje regresja w przypadku eksportu 16-bitowego, dlatego zalecamy ostrożność przy korzystaniu z tej funkcji w tej wersji.
Prosimy nie aktualizować Aspose.PSD do wersji 22.9-22.11, jeśli przetwarzanie obrazów 16-bitowych stanowi podstawową funkcjonalność.

Pracujemy nad rozwiązaniami tych problemów.

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-1320|Nie można eksportować nadzwyczaj dużych plików PSB|Ulepszenie|
|PSDNET-659|Możliwość przesunięcia środka gradientu radialnego|Funkcja|
|PSDNET-1330|Niedopuszczalna metoda kompresji ZipWithoutPrediction dla określonych plików|Funkcja|
|PSDNET-735|Po użyciu metody transformacji tylko dla warstwy, zapisana warstwa ma nieprawidłowy obszar ograniczający|Błąd|
|PSDNET-1234|Wyjątek podczas wczytywania obrazu PSD z wzorem|Błąd|
|PSDNET-1244|Błąd eksportu obrazu (IndexOutOfRangeException) podczas zapisywania pliku PSD z symbolami chińskimi|Błąd|
|PSDNET-1303|TimeLine ActiveFrame stosuje się nieprawidłowo|Błąd|
|PSDNET-1307|Regresja 22.7: nieprawidłowe renderowanie tekstu z arabskimi znakami|Błąd|
|PSDNET-1321|Maska wektorowa na warstwie grupy działa nieprawidłowo. Ostateczny obraz ma czarną dziurę, ale nie powinien|Błąd|


## **Zmiany w API publicznym**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-659. Możliwość przesunięcia środka gradientu radialnego**

{{< highlight csharp >}}
string plikZrodlowy = "psdnet659.psd";
string plikWyjsciowy = "wyjscie.png";

using (var obrazPsd = (PsdImage)Image.Load(plikZrodlowy))
{
    FillLayer warstwaRadialna = (FillLayer)obrazPsd.Layers[5];
    GradientFillSettings ustawienia = (GradientFillSettings)warstwaRadialna.FillSettings;

    // Aktualizacja punktu przesunięcia
    ustawienia.HorizontalOffset = 10;
    ustawienia.VerticalOffset = -25;

    obrazPsd.Save(plikWyjsciowy, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Po użyciu metody transformacji tylko dla warstwy, zapisana warstwa ma nieprawidłowy obszar ograniczający**

{{< highlight csharp >}}
string nazwaPlikuZrodlowego = @"TextLayer.psd";
string plikWyjsciowy = "TextLayerResized_output.psd";

using (PsdImage obraz = (PsdImage)Image.Load(nazwaPlikuZrodlowego, new PsdLoadOptions()))
{
    TextLayer warstwaTekstu = (TextLayer)obraz.Layers[1];

    // Ustawia nowy rozmiar warstwy tekstowej
    const int NowaSzerokosc = 250;
    const int NowaWysokosc = 250;

    // Ustawia mechanizm, w jaki funkcja zmiany rozmiaru będzie zmieniać warstwę (wartość domyślna)
    ResizeType typZmianyRozmiaru = ResizeType.NearestNeighbourResample;

    // Nowy mechanizm zmiany rozmiaru warstwy tekstowej
    // Zmieni się nie tylko warstwa, ale również macierz transformacji warstwy tekstowej
    warstwaTekstu.Resize(NowaSzerokosc, NowaWysokosc, typZmianyRozmiaru);

    obraz.Save(plikWyjsciowy, new PsdOptions(obraz));
}

using (PsdImage obraz = (PsdImage)Image.Load(plikWyjsciowy, new PsdLoadOptions()))
{
    TextLayer warstwaTekstu = (TextLayer)obraz.Layers[1];

    // Powód różnicy - inna domyślna czcionka
    if (warstwaTekstu.TransformMatrix[4] >= 65 
        && warstwaTekstu.TransformMatrix[4] <= 67
        && warstwaTekstu.TransformMatrix[5] >= 234
        && warstwaTekstu.TransformMatrix[5] <= 237)
    {
        // Wszystko w porządku
    }
    else
    {
        throw new Exception("Punkt lokalizacji jest nieprawidłowy");
    }
}
{{< /highlight >}}

**PSDNET-1234. Wyjątek podczas wczytywania obrazu PSD z wzorem**

{{< highlight csharp >}}
string plikSrc = "test.psd";
string wyjscie = "output1234.png";

using (PsdImage obrazPsd = (PsdImage)PsdImage.Load(plikSrc,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions opcjePng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    obrazPsd.Save(wyjscie, opcjePng);
}
{{< /highlight >}}

**PSDNET-1244. Błąd eksportu obrazu (IndexOutOfRangeException) podczas zapisywania pliku PSD z symbolami chińskimi**

{{< highlight csharp >}}
string plikZrodlowy = "input.psd";
string sciezkaWyjsciowa = "output.psd";

var opcjeWczytywania = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var obraz = (PsdImage)Image.Load(plikZrodlowy, opcjeWczytywania))
{
    foreach (var warstwa in obraz.Layers)
    {
        if (warstwa.Name == "1")
        {
            var warstwaTekstowa = (TextLayer)warstwa;

            warstwaTekstowa.UpdateText("测试测试");
        }
    }

    // Tutaj nie powinno być wyjątku.
    obraz.Save(sciezkaWyjsciowa, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame stosuje się nieprawidłowo**

{{< highlight csharp >}}
string zrodlo = "timeline1303.psd";
string wyjscie = "out_timeline.psd";

using (var obrazPsd = (PsdImage)Image.Load(zrodlo))
{
    TimeLine timeLine = TimeLine.InitializeFrom(obrazPsd);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(obrazPsd);

    obrazPsd.Save(wyjscie);
}
{{< /highlight >}}

**PSDNET-1307. Regresja 22.7: nieprawidłowe renderowanie tekstu z arabskimi znakami**

{{< highlight csharp >}}
string testowyFolderCzcionek = "Czcionki";
FontSettings.SetFontsFolder(testowyFolderCzcionek);
FontSettings.UpdateFonts();

string sciezkaPlikuZrodlowego = "sarbarg.fin12.psd";
string sciezkaPlikuWyjsciowego = "result.tiff";

using (var obrazPsd = (PsdImage)Image.Load(sciezkaPlikuZrodlowego))
{
    obrazPsd.Save(sciezkaPlikuWyjsciowego, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Nie można eksportować nadzwyczaj dużych plików PSB**

{{< highlight csharp >}}
string plikZrodlowy = "hf-mim-liman-han-guc-art-kuvvet.psb";
string sciezkaEksportuPsd = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var obraz = (PsdImage)Image.Load(plikZrodlowy, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    obraz.Save(sciezkaEksportuPsd, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Maska wektorowa na warstwie grupy działa nieprawidłowo. Ostateczny obraz ma czarną dziurę, ale nie powinien**

{{< highlight csharp >}}
string plikZrodlowy = "demo.psd";
string wyjscie = "demo_net.png";

using (PsdImage obraz = (PsdImage)PsdImage.Load(plikZrodlowy))
{
    PngOptions opcjePng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    obraz.Save(wyjscie, opcjePng);
}
{{< /highlight >}}

**PSDNET-1330. Niedopuszczalna metoda kompresji ZipWithoutPrediction dla określonych plików**

{{< highlight csharp >}}
string plikZrodlowy = "20221017_220706_0000.psd";
string plikWyjsciowy = "20221017_220706_0000.jpg";

using (var obraz = (PsdImage)Image.Load(plikZrodlowy, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase opcjePodstawowe = new JpegOptions() { Quality = 80 };
    obraz.Save(plikWyjsciowy, opcjePodstawowe);
}
{{< /highlight >}}
