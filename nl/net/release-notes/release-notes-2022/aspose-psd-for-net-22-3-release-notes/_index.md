---
title: Aspose.PSD voor .NET 22.3 - Release-opmerkingen
type: docs
weight: 100
url: /nl/net/aspose-psd-voor-net-22-3-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-210|Toevoegen van de eigenschap IsOpen voor Layer Group|Functie|
|PSDNET-643|PSD-afbeelding met rasterlaagmaskers verliest maskers bij opslaan naar 16-bits PSD-afbeelding|Fout|
|PSDNET-899|Blend-modus Dissolve wordt niet toegepast op de map met masker|Fout|
|PSDNET-1047|Specifiek bestand kan niet geopend worden door Photoshop na het opslaan in Aspose.PSD 21.11|Fout|
|PSDNET-1068|Onjuiste weergave van de laag met Lineaire Doordruk (Toevoegen) blend-modus|Fout|
|PSDNET-1069|Patroonvullingslaag veroorzaakt uitzondering bij bijwerken na laden|Fout|


## **Wijzigingen in de openbare API**
# **Nieuwe API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-210. Toevoegen van de eigenschap IsOpen voor Layer Groep**

{{< highlight csharp >}}
// Voorbeeld van het lezen en schrijven van de eigenschap IsOpen tijdens runtime.
string bronBestandsnaam = "LayerGroupOpenClose.psd";
string uitvoerBestandsnaam = "Uitvoer" + bronBestandsnaam;

using (var afbeelding = (PsdImage)Image.Load(bronBestandsnaam))
{
    foreach (var laag in afbeelding.Lagen)
    {
        if (laag is LayerGroup && laag.Naam == "Groep 1")
        {
            bool isGroep1Open = ((LayerGroup)laag).IsOpen;
            ((LayerGroup)laag).IsOpen = !isGroep1Open;
        }

        if (laag is LayerGroup && laag.Naam == "Groep 2")
        {
            bool isGroep2Open = ((LayerGroup)laag).IsOpen;           
            ((LayerGroup)laag).IsOpen = !isGroep2Open;
        }
    }

    afbeelding.Opslaan(uitvoerBestandsnaam);
}
{{< /highlight >}}

**PSDNET-643. PSD-afbeelding met rasterlaagmaskers verliest maskers bij opslaan naar 16-bits PSD-afbeelding**

{{< highlight csharp >}}
            string bronBestandspad = "EénRegulierenEénRegulierMetMasker.psd";
            string uitvoerBestandspad = "uit_EénRegulierenEénRegulierMetMasker.psd";

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandspad))
            {
                afbeelding.Opslaan(uitvoerBestandspad, new PsdOpties(afbeelding)
                {
                    KanaalBitsTelling = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Blend-modus Dissolve wordt niet toegepast op de map met masker**

{{< highlight csharp >}}
            string bronBestand = "psdnet899.psd";
            string uitvoerPng = "uit_psdnet899.png";

            using (PsdImage afbeelding = (PsdImage) Image.Load(bronBestand))
            {
                afbeelding.Opslaan(uitvoerPng, new PngOpties());
            }
{{< /highlight >}}

**PSDNET-1047. Specifiek bestand kan niet geopend worden door Photoshop na het opslaan in Aspose.PSD 21.11**

{{< highlight csharp >}}
            string bronBestand = "psdnet1047.psd";
            string uitvoerPsd = "uit_psdnet1047.psd";

            using (PsdImage afbeelding = (PsdImage) Image.Load(bronBestand))
            {
                afbeelding.Opslaan(uitvoerPsd);
            }

            // Moet het uitvoer-PSD-bestand handmatig openen met Photoshop.

            using (PsdImage afbeelding = (PsdImage) Image.Load(uitvoerPsd))
            {
                // geen uitzondering.
            }
{{< /highlight >}}

**PSDNET-1068. Onjuiste weergave van de laag met Lineaire Doordruk (Toevoegen) blend-modus**

{{< highlight csharp >}}
            string bronBestand = "broken.psd";
            string uitvoerPng = "uit_broken.psd.png";

            using (var psdAfbeelding = (PsdImage) Image.Load(bronBestand))
            {
                psdAfbeelding.Opslaan(uitvoerPng, new PngOpties() {KleurType = PngKleurType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Patroonvullingslaag veroorzaakt uitzondering bij bijwerken na laden**

{{< highlight csharp >}}
            string bronBestand = "AllTypesLayerPsd.psd";

            using (var afbeelding = (PsdImage) Image.Load(bronBestand))
            {
                var vulLaag = (VulLaag)afbeelding.Lagen[9];
                vulLaag.Update();
            }
{{< /highlight >}}
