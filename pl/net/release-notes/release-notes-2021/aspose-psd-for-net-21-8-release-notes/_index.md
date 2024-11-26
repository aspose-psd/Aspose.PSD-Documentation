---
title: Notatki wydania Aspose.PSD dla .NET 21.8
type: docs
weight: 50
url: /pl/net/aspose-psd-dla-net-21-8-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-698|Wsparcie dla metod kompresji ZipWithPrediction|Funkcja|
|PSDNET-663|Niewłaściwe odstępy między tekstami w generowanym pliku PSD|Błąd|
|PSDNET-685|Wyjątek podczas zapisywania pliku PSD|Błąd|
|PSDNET-927|Niewłaściwy odstęp między liniami i symbolami w Aspose.PSD gdy używamy go bez licencji|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- Brak

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDNET-663. Niewłaściwe odstępy między tekstami w generowanym pliku PSD**

{{< highlight csharp >}}
            string nazwaPlikuZrodlowego = "plikZrodlowy.psd";
            string nazwaPlikuWyjsciowego = "wyjscie.png";

            using (PsdImage obraz = (PsdImage)Image.Load(nazwaPlikuZrodlowego))
            {
                obraz.Save(nazwaPlikuWyjsciowego, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Wyjątek podczas zapisywania pliku PSD**

{{< highlight csharp >}}
            string nazwaPlikuZrodlowego = "Plik.psd";
            string nazwaPlikuWyjsciowego = "Plik2.psd";

            using (PsdImage obraz = (PsdImage)Image.Load(nazwaPlikuZrodlowego))
            {
                var warstwa1 = (TextLayer)obraz.Layers[1];
                warstwa1.TextData.UpdateLayerData();

                obraz.Save(nazwaPlikuWyjsciowego);
            }
{{< /highlight >}}

**PSDNET-698. Wsparcie dla metod kompresji ZipWithPrediction**

{{< highlight csharp >}}
            string sciezkaWejsciowa = "zipTest698.psd";

            string wyjsciePng = "wyjscie.png";
            string wyjscieRaw = "wyjscie_Raw.psd";
            string wyjscieZip = "wyjscie_Zip.psd";

            using (Image obraz = Image.Load(sciezkaWejsciowa))
            {
                obraz.Save(wyjsciePng, new PngOptions());

                obraz.Save(wyjscieRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                obraz.Save(wyjscieZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Niewłaściwy odstęp między liniami i symbolami w Aspose.PSD gdy używamy go bez licencji**

{{< highlight csharp >}}
            bool[] stanyLicencji = new bool[] { false, true };
            for (int i = 0; i < stanyLicencji.Length; i++)
            {
                bool testLicencji = stanyLicencji[i];
                if (testLicencji)
                {
                    License licencja = new License();
                    licencja.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string plikZrodlowy = "psdnetTest927.psd";
                string plikWyjsciowy = "wyj_" + testLicencji.ToString() + "_psdnetTest927.png";

                using (var obraz = (PsdImage)Image.Load(plikZrodlowy))
                {
                    obraz.Save(plikWyjsciowy, new PngOptions());
                }
            }
{{< /highlight >}}
