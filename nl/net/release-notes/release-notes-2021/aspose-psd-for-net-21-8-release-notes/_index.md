---
title: Aspose.PSD voor .NET 21.8 - Release-opmerkingen
type: docs
weight: 50
url: /nl/net/aspose-psd-voor-net-21-8-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-698|Ondersteuning van compressiemethoden ZipWithPrediction|Functie|
|PSDNET-663|De tekstafstand is onjuist in gegenereerde PSD-bestanden|Bug|
|PSDNET-685|Uitzondering bij het opslaan van PSD-bestand|Bug|
|PSDNET-927|Onjuiste afstand tussen regels en symbolen in Aspose.PSD bij gebruik zonder licentie|Bug|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-663. De tekstafstand is onjuist in gegenereerde PSD-bestanden**

{{< highlight csharp >}}
            string bronBestandsnaam = "bron.psd";
            string uitvoerBestandsnaam = "uitvoer.png";

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsnaam))
            {
                afbeelding.Save(uitvoerBestandsnaam, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Uitzondering bij het opslaan van PSD-bestand**

{{< highlight csharp >}}
            string bronBestandsnaam = "Bestand.psd";
            string uitvoerBestandsnaam = "Bestand2.psd";

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsnaam))
            {
                var laag1 = (TextLayer)afbeelding.Layers[1];
                laag1.TextData.UpdateLayerData();

                afbeelding.Save(uitvoerBestandsnaam);
            }
{{< /highlight >}}

**PSDNET-698. Ondersteuning van compressiemethoden ZipWithPrediction**

{{< highlight csharp >}}
            string invoerBestandsPad = "zipTest698.psd";

            string uitvoerPng = "uitvoer.png";
            string uitvoerRaw = "uit_Raw.psd";
            string uitvoerZip = "uit_Zip.psd";

            using (Image afbeelding = Image.Load(invoerBestandsPad))
            {
                afbeelding.Save(uitvoerPng, new PngOptions());

                afbeelding.Save(uitvoerRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                afbeelding.Save(uitvoerZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Onjuiste afstand tussen regels en symbolen in Aspose.PSD bij gebruik zonder licentie**

{{< highlight csharp >}}
            bool[] licentieStatussen = new bool[] { false, true };
            for (int i = 0; i < licentieStatussen.Length; i++)
            {
                bool testLicentie = licentieStatussen[i];
                if (testLicentie)
                {
                    License licentie = new License();
                    licentie.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string bronBestand = "psdnetTest927.psd";
                string uitvoerBestand = "uit_" + testLicentie.ToString() + "_psdnetTest927.png";

                using (var afbeelding = (PsdImage)Image.Load(bronBestand))
                {
                    afbeelding.Save(uitvoerBestand, new PngOptions());
                }
            }
{{< /highlight >}}
