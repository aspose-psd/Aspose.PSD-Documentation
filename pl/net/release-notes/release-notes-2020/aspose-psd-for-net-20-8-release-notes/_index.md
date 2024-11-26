---
title: Aspose.PSD dla .NET 20.8 - Notatki dotyczące wersji
type: docs
weight: 50
url: /pl/net/aspose-psd-dla-net-20-8-notatki-o-wydaniu/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-390|Wsparcie dla PlLdResource (zasób warstwy umieszczonej dla warstwy obiektu inteligentnej warstwy)|Funkcja|
|PSDNET-400|Wsparcie dla SoLdResource (zasób danych warstwy obiektu inteligentnej warstwy)|Funkcja|
|PSDNET-693|Dodano obsługę struktur tablicy obiektów i tablicy jednostek: sygnatury ObAr / UnFl|Funkcja|
|PSDNET-600|Naprawa zapisywania zmodyfikowanego obrazu PSD z trybem koloru CMYK 16 bitów na kanał|Poprawka|
|PSDNET-664|Podkreślenie i przekreślenie zostają utracone po skoncentrowaniu tekstu w pliku zapisanym za pomocą Aspose.PSD|Poprawka|
|PSDNET-710|Regresja: Aspose.PSD 20.7.0 zmienia rozmiary czcionek w starszych plikach|Poprawka|

## **Zmiany w API publicznym**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
(...)

## **Przykłady użycia:**
**PSDNET-390. Wsparcie dla PlLdResource (zasób warstwy umieszczonej dla warstwy obiektu inteligentnej warstwy)**
{{< highlight csharp >}}
        void SprawdzCzySąRówne(object rzeczywistaWartość, object oczekiwanaWartość)
        {
            var sąRówne = object.Equals(rzeczywistaWartość, oczekiwanaWartość);
            if (!sąRówne && rzeczywistaWartość is Array && oczekiwanaWartość is Array)
            {
                var rzeczywistaTablica = (Array)rzeczywistaWartość;
                var oczekiwanaTablica = (Array)rzeczywistaWartość;
                if (rzeczywistaTablica.Length == oczekiwanaTablica.Length)
                {
                    for (int i = 0; i < rzeczywistaTablica.Length; i++)
                    {
                        if (!object.Equals(rzeczywistaTablica.GetValue(i), oczekiwanaTablica.GetValue(i)))
                        {
                            break;
                        }
                    }

                    sąRówne = true;
                }
            }

            if (!sąRówne)
            {
                throw new FormatException(
                    string.Format("Rzeczywista wartość {0} nie jest równa oczekiwanej {1}.", rzeczywistaWartość, oczekiwanaWartość));
            }
        }
        
        (...)
{{< /highlight >}}
(...)
(...)
**PSDNET-400. Wsparcie dla SoLdResource (zasób danych warstwy obiektu inteligentnej warstwy)**
{{< highlight csharp >}}
       (...)
{{< /highlight >}}
**PSDNET-693. Dodano obsługę struktur tablicy obiektów i tablicy jednostek: sygnatury ObAr / UnFl**
{{< highlight csharp >}}
       (...)
{{< /highlight >}}
**PSDNET-600. Naprawa zapisywania zmodyfikowanego obrazu PSD z trybem koloru CMYK 16 bitów na kanał**
{{< highlight csharp >}}
       (...)
{{< /highlight >}}
**PSDNET-664. Podkreślenie i przekreślenie zostają utracone po skoncentrowaniu tekstu w pliku zapisanym za pomocą Aspose.PSD**
{{< highlight csharp >}}
       (...)
{{< /highlight >}}
**PSDNET-710. Regresja: Aspose.PSD 20.7.0 zmienia rozmiary czcionek w starszych plikach**
{{< highlight csharp >}}
       (...)
{{< /highlight >}}