---
title: Aspose.PSD dla .NET 22.9 - Notatki dotyczące wydania
type: docs
weight: 40
url: /pl/net/aspose-psd-dla-net-22-9-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- To wydanie ma regresję w przypadku eksportu 16-bitowego, dlatego zalecamy ostrożność przy korzystaniu z tej funkcji w tym wydaniu. Prosimy nie aktualizować Aspose.PSD do wersji 22.9, jeśli przetwarzanie obrazu 16-bitowego jest główną funkcjonalnością.
- Dla kilku wersji programu Photoshop użytkownicy mogą napotkać okno z błędem odczytu warstwy, co nie wpłynie na pracę z plikiem PSD.

Pracujemy nad rozwiązaniami tych problemów.

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-1237|Utwórz wewnętrzny model LayerStyleFX, który będzie zawierał efekty i związane dane do użycia pojedynczego modelu w zasobach efektów Lfx2, lmfx i mlst|Udoskonalenie|
|PSDNET-1227|Dodaj czytanie i zapisywanie struktur „Lefx” z informacjami o efektach dla stanów warstw w modelach TimeLine|Funkcja|
|PSDNET-1230|Zastosowanie stanu warstwy TimeLine do warstwy w obrazie Psd|Funkcja|
|PSDNET-1072|Niepoprawna przezroczystość podczas zapisywania pliku PSD (RGB/16-bit) podczas eksportu do 8-bit|Błąd|
|PSDNET-1140|Wyjątek podczas wczytywania kroków globalnych zasobów warstwy podczas otwierania dokumentu PSB|Błąd|
|PSDNET-1266|Wyciek pamięci podczas przetwarzania określonych plików|Błąd|


## **Zmiany w publicznym interfejsie API**
# **Dodane interfejsy:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **Usunięte interfejsy:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Przykłady użycia:**

**PSDNET-1072. Niepoprawna przezroczystość podczas zapisywania pliku PSD (RGB/16-bit) podczas eksportu do 8-bit**

{{< highlight csharp >}}
string inputPlikPsd    = "8bitZPrzezroczystoscia.psd";
string outputPlikPsd   = "16bitZPrzezroczystoscia.psd";
string outputPlikObrazu = "WyjscieZPrzezroczystoscia.png";

using (var img = Image.Load(inputPlikPsd))
{
    // opcje zapisywania 16 bitów
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPlikPsd, p16);
}
using (var img = Image.Load(outputPlikPsd))
{
    // Zapisz obrazek z 16-bitowymi kolorami
    img.Save(outputPlikObrazu, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Wyjątek podczas wczytywania kroków globalnych zasobów warstwy podczas otwierania dokumentu PSB**

{{< highlight csharp >}}
string plikZrodlowyPsd = "wejsciowy.psb";
string plikWyjsciowyObrazu = "wyjsciowy.png";

using (var obraz = (PsdImage)Image.Load(plikZrodlowyPsd))
{
    // Tutaj nie powinien być wyjątek.
    obraz.Save(plikWyjsciowyObrazu, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Dodaj czytanie i zapisywanie struktur „Lefx” z informacjami o efektach dla stanów warstw w modelach TimeLine**

{{< highlight csharp >}}
string plikZrodlowy = "4_animowany.psd";
string plikWyjsciowy = "wyjsciowy.psd";

using (var obrazPsd = (PsdImage)Image.Load(plikZrodlowy))
{
    TimeLine timeLine = TimeLine.InitializeFrom(obrazPsd);
    int[] identyfikatoryWarstw = timeLine.IdentyfikatoryWarstw;

    var efektyStanuWarstwy11 = timeLine.Klatki[1].StanyWarstw[identyfikatoryWarstw[1]].EfektyStanu;

    efektyStanuWarstwy11.AddDropShadow();
    efektyStanuWarstwy11.AddGradientOverlay();

    var efektyStanuWarstwy21 = timeLine.Klatki[2].StanyWarstw[identyfikatoryWarstw[1]].EfektyStanu;
    efektyStanuWarstwy21.AddStroke(FillType.Color);
    efektyStanuWarstwy21.IsVisible = false;

    timeLine.ZastosujDo(obrazPsd);

    obrazPsd.Save(plikWyjsciowy);
}
{{< /highlight >}}

**PSDNET-1230. Zastosowanie stanu warstwy TimeLine do warstwy w obrazie Psd**

{{< highlight csharp >}}
string plikZrodlowy = "3_animowany.psd";
string plikWyjsciowyPsd = "wyjsciowy.psd";
string plikWyjsciowyPng = "wyjsciowy.png";

using (var obrazPsd = (PsdImage)Image.Load(plikZrodlowy, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(obrazPsd);
    var identyfikatoryWarstw = timeLine.IdentyfikatoryWarstw;

    var stanWarstwy11 = timeLine.Klatki[1].StanyWarstw[identyfikatoryWarstw[1]];

    timeLine.Klatki[1].StanyWarstw[identyfikatoryWarstw[1]].EfektyStanu.AddPatternOverlay();
    stanWarstwy11.TrybMieszania = BlendMode.Multiply;

    // Zmień aktywną klatkę z 0 na 1, aby aktywować zastosowanie LayerState do Layer
    timeLine.AktywnaKlatka = 1;

    // Zastosuj zmiany do PsdImage
    timeLine.ZastosujDo(obrazPsd);

    obrazPsd.Save(plikWyjsciowyPsd);
    obrazPsd.Save(plikWyjsciowyPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Wyciek pamięci podczas przetwarzania określonych plików**

{{< highlight csharp >}}
string[] plikiDoWczytania = new string[] { "testowyPsd0.psd", "testowyPsd1.psd", "testowyPsd2.psd" };
int numerWejsciowy = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(numerWejsciowy, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double iloscPamieci = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Całkowita liczba użytych bajtów przed testem: {0:N2} MiB", iloscPamieci);

double maksymalna = iloscPamieci;

for (int i = 0; i < 50; i++)
{
    int indeksPliku = i % numerWejsciowy;
    string plikZrodlowy = Path.Combine(folderBazy, plikiDoWczytania[indeksPliku]);

    // Sprawdź OtwieranieZapisywanie
    using (MemoryStream strumienWyjsciowy = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(plikZrodlowy, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(strumienWyjsciowy, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(numerWejsciowy, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    iloscPamieci = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    maksymalna = Math.Max(maksymalna, iloscPamieci);
}

iloscPamieci = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Całkowita liczba użytych bajtów po teście: {0:N2} MiB", iloscPamieci);
Assert.IsTrue(Math.Abs(iloscPamieci - maksymalna) < 20, "Wyciek pamięci został znaleziony w podstawowej funkcjonalności!");
{{< /highlight >}}
