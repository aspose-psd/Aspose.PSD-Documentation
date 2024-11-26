---
title: Notatki dotyczące wersji Aspose.PSD dla .NET 22.7
type: docs
weight: 60
url: /pl/net/aspose-psd-dla-net-22-7-notatki-o-wersji/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wersji [Aspose.PSD dla .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-482|Wsparcie dla zasobu sekcji obrazu #4000-4999 Zasób Plug-In|Nowa funkcja|
|PSDNET-875|Wystąpienie nieobsłużonego wyjątku typu "System.OutOfMemoryException" w Aspose.PSD.dll|Błąd|
|PSDNET-1050|Po wyeksportowaniu pliku PSD, wynikowy plik jest znacznie większy niż plik źródłowy|Błąd|
|PSDNET-1083|Niepoprawne analizowanie danych dla XmpResource|Błąd|
|PSDNET-1205|Po eksporcie rozmiar plików PSD z podfolderami wzrósł|Błąd|


## **Zmiany w API publicznym**
# **Dodane API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.SaveData(Aspose.PSD.StreamContainer)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.KeyName
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.AnimatedDataSection
- M:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.SaveData(Aspose.PSD.StreamContainer)


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-482. Wsparcie dla zasobu sekcji obrazu #4000-4999 Zasób Plug-In**

{{< highlight csharp >}}
// Poniższy kod demonstruje, jak ustawić/aktualizować czas opóźnienia w ramce klatki czasowej animowanych danych.
string plikŹródłowy = "3_animated.psd";
string plikWyjściowyPsd = "output_3_animated.psd";

T ZnajdźStrukturę<T>(IEnumerable<OSTypeStructure> struktury, string nazwaKlucza) where T : OSTypeStructure
{
    foreach (var struktura in struktury)
    {
        if (struktura.KeyName.ClassName == nazwaKlucza)
        {
            return struktura as T;
        }
    }

    return null;
}

OSTypeStructure[] DodajLubZamieńStrukturę(IEnumerable<OSTypeStructure> struktury, OSTypeStructure nowaStruktura)
{
    List<OSTypeStructure> listaStruktur = new List<OSTypeStructure>(struktury);

    for (int i = 0; i < listaStruktur.Count; i++)
    {
        OSTypeStructure struktura = listaStruktur[i];
        if (struktura.KeyName.ClassName == nowaStruktura.KeyName.ClassName)
        {
            listaStruktur.RemoveAt(i);
            break;
        }
    }

    listaStruktur.Add(nowaStruktura);

    return listaStruktur.ToArray();
}

using (PsdImage obraz = (PsdImage)Image.Load(plikŹródłowy))
{
    foreach (var zasóbObrazu in obraz.ImageResources)
    {
        if (zasóbObrazu is AnimatedDataSectionResource)
        {
            var daneAnimowane =
            (AnimatedDataSectionStructure) (zasóbObrazu as AnimatedDataSectionResource).AnimatedDataSection;
            var listaKlatek = ZnajdźStrukturę<ListStructure>(daneAnimowane.Items, "FrIn");

            var klatka1 = (DescriptorStructure)listaKlatek.Types[1];

            // Tworzy rekord opóźnienia klatki o wartości 100 centysekund równych 1 sekundzie.
            var opóźnienieKlatki = new IntegerStructure(new ClassID("FrDl"));
            opóźnienieKlatki.Value = 100; // ustaw czas w centysekundach.

            klatka1.Struktury = DodajLubZamieńStrukturę(klatka1.Struktury, opóźnienieKlatki);

            break;
        }
    }

    obraz.Save(plikWyjściowyPsd);
}
{{< /highlight >}}

**PSDNET-875. Wystąpienie nieobsłużonego wyjątku typu "System.OutOfMemoryException" w Aspose.PSD.dll**

{{< highlight csharp >}}
string srcFile = "001-.psd";
string jpgFilePath = "T_0003.jpg";
string outputFilePath = "output_newPsd.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    using (FileStream fs = new FileStream(jpgFilePath, FileMode.Open))
    {
        var nowaWarstwa = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        nowaWarstwa.DisplayName = "NowaWarstwa";

        im.AddLayer(nowaWarstwa);

        im.Save(outputFilePath, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Po wyeksportowaniu pliku PSD, wynikowy plik jest znacznie większy niż plik źródłowy**

{{< highlight csharp >}}
string źródło = "ShimadzuLetterhead100.psd";
string wynik = "output.psd";
using (var img = (PsdImage)Image.Load(źródło))
{
    img.Save(wynik);
}

double rozmiarWynikuMb = new FileInfo(wynik).Length / 1024d / 1024d;
if (rozmiarWynikuMb > 6)
{
    throw new Exception("Plik wynikowy jest większy niż powinien być.");
}
{{< /highlight >}}

**PSDNET-1083. Nieprawidłowe parsowanie danych dla XmpResource**

{{< highlight csharp >}}
string ścieżkaObrazuŹródłowegoPsd = @"input.psd";
string zapisanaŚcieżkaObrazuPsd = @"saved.psd";

bool czyOryginałZawiera = false;
bool czyZapisanaZawiera = false;

// Znajdź podklucz XMP w pliku źródłowym
using (PsdImage obraz = (PsdImage)Image.Load(ścieżkaObrazuŹródłowegoPsd))
{
    foreach (var pakiet in obraz.XmpData.Packages)
    {
        foreach (var paczka in pakiet)
        {
            if (paczka.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)paczka.Value;

                string wartośćXml = xmpArray.GetXmlValue();

                if (wartośćXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    czyOryginałZawiera = true;
                    break;
                }
            }
        }

        if (czyOryginałZawiera)
        {
            break;
        }
    }
    obraz.Save(zapisanaŚcieżkaObrazuPsd);
}

// Znajdź podklucz XMP w zapisanym pliku
using (PsdImage obraz = (PsdImage)Image.Load(zapisanaŚcieżkaObrazuPsd))
{
    foreach (var pakiet in obraz.XmpData.Packages)
    {
        foreach (var paczka in pakiet)
        {
            if (paczka.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)paczka.Value;

                string wartośćXml = xmpArray.GetXmlValue();

                if (wartośćXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    czyZapisanaZawiera = true;
                    break;
                }
            }
        }

        if (czyZapisanaZawiera)
        {
            break;
        }
    }
    obraz.Save(zapisanaŚcieżkaObrazuPsd);
}

if (czyOryginałZawiera && czyZapisanaZawiera)
{
    // Wszystko jest w porządku!
}
else
{
    throw new Exception("To nie działa");
}
{{< /highlight >}}

**PSDNET-1205. Po eksporcie rozmiar plików PSD z podfolderami wzrósł**

{{< highlight csharp >}}
string[] plikiŹródłowe = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var nazwaPliku in plikiŹródłowe)
{
    string ścieżkaPlikuŹródłowego = nazwaPliku;
    string ścieżkaPlikuWyjściowego = "output_" + nazwaPliku;

    using (PsdImage obraz = (PsdImage)Image.Load(ścieżkaPlikuŹródłowego))
    {
        obraz.Save(ścieżkaPlikuWyjściowego);
    }

    double rozmiarWynikuMb = new FileInfo(ścieżkaPlikuWyjściowego).Length / 1024d / 1024d;
    if (rozmiarWynikuMb > 1.9)
    {
        throw new Exception("Plik wynikowy jest większy niż powinien być.");
    }
}
{{< /highlight >}}
