---
title: Aspose.PSD dla .NET 22.3 - Notatki wydania
type: docs
weight: 100
url: /pl/net/aspose-psd-dla-net-22-3-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-210|Dodaj właściwość IsOpen dla grupy warstw|Funkcja|
|PSDNET-643|Obraz PSD z maskami warstw rastrów odrzuca maski podczas zapisywania do obrazu PSD o głębi 16 bitów|Błąd|
|PSDNET-899|Tryb mieszania Rozpuszczanie nie jest stosowany do folderu z maską|Błąd|
|PSDNET-1047|Konkretny plik nie może zostać otwarty przez Photoshop po zapisaniu w Aspose.PSD 21.11|Błąd|
|PSDNET-1068|Nieprawidłowe renderowanie warstwy z trybem mieszania Linearna Ściema (Dodawanie)|Błąd|
|PSDNET-1069|Warstwa wypełnienia wzorem zgłasza wyjątek podczas aktualizacji po załadowaniu|Błąd|


## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-210. Dodaj właściwość IsOpen dla grupy warstw**

{{< highlight csharp >}}


// Przykład odczytywania i zapisywania właściwości IsOpen w czasie wykonywania.
string nazwaPlikuZrodlowego = "OtwórzZamknijGrupę.psd";
string nazwaPlikuWyjściowego = "Wynik" + nazwaPlikuZrodlowego;

using (var obraz = (PsdImage)Image.Load(nazwaPlikuZrodlowego))
{
    foreach (var warstwa in obraz.Layers)
    {
        if (warstwa is LayerGroup && warstwa.Name == "Grupa 1")
        {
            bool jestOtwartaGrupa1 = ((LayerGroup)warstwa).IsOpen;
            ((LayerGroup)warstwa).IsOpen = !jestOtwartaGrupa1;
        }

        if (warstwa is LayerGroup && warstwa.Name == "Grupa 2")
        {
            bool jestOtwartaGrupa2 = ((LayerGroup)warstwa).IsOpen;           
            ((LayerGroup)warstwa).IsOpen = !jestOtwartaGrupa2;
        }
    }

    obraz.Save(nazwaPlikuWyjściowego);
}
{{< /highlight >}}


**PSDNET-643. Obraz PSD z maskami warstw rastrów odrzuca maski podczas zapisywania do obrazu PSD o głębi 16 bitów**

{{< highlight csharp >}}
        string ścieżkaDoPlikuŹródłowego = "JedenZwykłyIOdMaską.psd";
        string ścieżkaDoPlikuWyjściowego = "out_JedenZwykłyIOdMaską.psd";

        using (PsdImage obraz = (PsdImage)Image.Load(ścieżkaDoPlikuŹródłowego))
        {
            obraz.Save(ścieżkaDoPlikuWyjściowego, new PsdOptions(obraz)
            {
                ChannelBitsCount = 16
            });
        }
{{< /highlight >}}


**PSDNET-899. Tryb mieszania Rozpuszczanie nie jest stosowany do folderu z maską**

{{< highlight csharp >}}
        string plikŹródłowy = "psdnet899.psd";
        string plikPng = "out_psdnet899.png";

        using (PsdImage obraz = (PsdImage) Image.Load(plikŹródłowy))
        {
            obraz.Save(plikPng, new PngOptions());
        }
{{< /highlight >}}


**PSDNET-1047. Konkretny plik nie może zostać otwarty przez Photoshop po zapisaniu w Aspose.PSD 21.11**

{{< highlight csharp >}}
        string plikŹródłowy = "psdnet1047.psd";
        string plikPsd = "out_psdnet1047.psd";

        using (PsdImage obraz = (PsdImage) Image.Load(plikŹródłowy))
        {
            obraz.Save(plikPsd);
        }

        // Konieczne jest ręczne otwarcie pliku PSD przez Photoshop.

        using (PsdImage obraz = (PsdImage) Image.Load(plikPsd))
        {
            // brak wyjątku.
        }
{{< /highlight >}}


**PSDNET-1068. Nieprawidłowe renderowanie warstwy z trybem mieszania Linearna Ściema (Dodawanie)**

{{< highlight csharp >}}

        string plikŹródłowy = "zepsuty.psd";
        string plikPng = "out_zepsuty.psd.png";

        using (var obrazPsd = (PsdImage) Image.Load(plikŹródłowy))
        {
            obrazPsd.Save(plikPng, new PngOptions() {ColorType = PngColorType.Truecolor});
        }
{{< /highlight >}}


**PSDNET-1069. Warstwa wypełnienia wzorem zgłasza wyjątek podczas aktualizacji po załadowaniu**

{{< highlight csharp >}}
        string plikŹródłowy = "PsdWszytkieRodzajeWarstw.psd";

        using (var obraz = (PsdImage) Image.Load(plikŹródłowy))
        {
            var warstwaWypełnienia = (FillLayer)obraz.Layers[9];
            warstwaWypełnienia.Update();
        }
{{< /highlight >}}
