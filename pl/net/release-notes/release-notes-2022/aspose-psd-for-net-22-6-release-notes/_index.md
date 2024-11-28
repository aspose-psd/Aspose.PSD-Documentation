---
title: Notatki do wersji Aspose.PSD dla .NET 22.6
type: docs
weight: 70
url: /pl/net/aspose-psd-dla-net-22-6-notatki-do-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki do wersji [Aspose.PSD dla .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-940|Utwórz interfejs API pozwalający uzyskać unikalny skrót dla podobnych warstw w różnych plikach|Usprawnienie|
|PSDNET-678|Nieprawidłowe renderowanie warstwy wypełnienia z wzorem w przypadku, gdy wzory są więcej niż jeden i zmieniony jest porządek warstw|Błąd|
|PSDNET-1125|Wyjątek podczas wczytywania określonego pliku PSD w trybie kolorów CMYK|Błąd|


## Zmiany w API publicznym
# **Dodane API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-678. Nieprawidłowe renderowanie warstwy wypełnienia z wzorem w przypadku, gdy wzory są więcej niż jeden i zmieniony jest porządek warstw**

{{< highlight csharp >}}
string plikŹródłowy = "zły_wzór.psd";
string plikPng = "wyjscie_678.png";

using (var obrazPsd = (PsdImage)Image.Load(plikŹródłowy))
{
    FillLayer warstwa1 = (FillLayer)obrazPsd.Layers[1];
    FillLayer warstwa2 = (FillLayer)obrazPsd.Layers[2];

    warstwa1.Update();
    warstwa2.Update();

    obrazPsd.Save(plikPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Utwórz interfejs API pozwalający uzyskać unikalny skrót dla podobnych warstw w różnych plikach**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    static void Main()
    {
        // Implementacja testów
    }

    // Metody pomagające wykonanie testów
}
{{< /highlight >}}

**PSDNET-1125. Wyjątek podczas wczytywania określonego pliku PSD w trybie kolorów CMYK**

{{< highlight csharp >}}
string plikŹródłowy = "02_kanały-alfa.psd";
string plikPng = "wyjście_1125.png";

using (PsdImage obraz = (PsdImage)Image.Load(plikŹródłowy))
{
    obraz.Save(plikPng, new PngOptions());
}
{{< /highlight >}}