---
title: Aspose.PSD voor .NET 24.8 - Release-opmerkingen
type: docs
weight: 50
url: /nl/net/aspose-psd-voor-net-24-8-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 24.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Samenvatting**                                                                                    | **Categorie** |
|:------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2091 | [AI-indeling] Toevoegen van verwerking voor XObject-groepen                                           | Verbetering   |
| PSDNET-1754 | Verbeteren van Warp-transformatiecapaciteiten door WarpSettings toe te voegen voor TextLayer en SmartObjectLayer | Kenmerk       |
| PSDNET-1836 | [AI-indeling] Lagen verwerken in contentstroomoperatoren                                              | Kenmerk       |
| PSDNET-2015 | Weergaveresultaat van AI-bestand verschilt sterk in vergelijking met Illustrator-resultaten           | Fout         |
| PSDNET-2093 | Opnieuw koppelen van Smart Object is niet van toepassing op alle Smart Objects in het PSD-bestand    | Fout         |

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-1754. Verbeteren van Warp-transformatiecapaciteiten door WarpSettings toe te voegen voor TextLayer en SmartObjectLayer**

{{< highlight csharp >}}
string bronbestand = Path.Combine(basismap, "smart_zonder_warp.psd");

var opties = nieuwe PsdLaadopties()
{
    LaadEffectenResource = waar,
    StaWarpRepaintToe = waar
};

string[] uitvoerAfbeeldingsbestand = nieuwe string[4];
string[] uitvoerPsdBestand = nieuwe string[4];

voor (int caseIndex = 0; caseIndex < uitvoerAfbeeldingsbestand.Lengte; caseIndex++)
{
    uitvoerAfbeeldingsbestand[caseIndex] = Path.Combine(uitvoermap, "export_" + caseIndex + ".png");
    uitvoerPsdBestand[caseIndex] = Path.Combine(uitvoermap, "export_" + caseIndex + ".psd");

    gebruikend (PsdAfbeelding img = (PsdAfbeelding)Afbeelding.Laden(bronbestand, opties))
    {
        voor elke (Laag laag in img.Lagen)
        {
            als (laag is SmartObjectLayer)
            {
                var slimmeLaag = (SmartObjectLayer)laag;
                slimmeLaag.WarpSettings = GeefWarpInstellingenOpIndex(slimmeLaag.WarpSettings, caseIndex);
            }

            als (laag is TextLayer)
            {
                var tekstlaag = (TextLayer)laag;

                als (caseIndex != 3)
                {
                    tekstlaag.WarpSettings = GeefWarpInstellingenOpIndex(tekstlaag.WarpSettings, caseIndex);
                }
            }
        }

        img.Opslaan(uitvoerPsdBestand[caseIndex], nieuwe PsdOpties());
    }

    gebruikend (PsdAfbeelding img = (PsdAfbeelding)Afbeelding.Laden(uitvoerPsdBestand[caseIndex], opties))
    {
        img.Opslaan(uitvoerAfbeeldingsbestand[caseIndex],
            nieuwe PngOpties() { CompressieNiveau = 9, Kleurtype = PngKleurtype.TruecolorMetAlpha });
    }
}

WarpSettings GeefWarpInstellingenOpIndex(WarpSettings warpParams, int caseIndex)
{
    schakel (caseIndex)
    {
        geval 0:
            warpParams.Stijl = WarpStyles.Rise;
            warpParams.Roteer = WarpRotates.Horizontal;
            warpParams.Waarde = 20;
            doorbraak;
        geval 1:
            warpParams.Stijl = WarpStyles.Rise;
            warpParams.Roteer = WarpRotates.Verticaal;
            warpParams.Waarde = 10;
            doorbraak;
        geval 2:
            warpParams.Stijl = WarpStyles.Flag;
            warpParams.Roteer = WarpRotates.Horizontal;
            warpParams.Waarde = 30;
            doorbraak;
        geval 3:
            warpParams.Stijl = WarpStyles.Aangepast;
            warpParams.MeshPoints[2].Y += 70;
            doorbraak;
    }

    terugkeer warpParams;
}
{{< /highlight >}}

**PSDNET-1836. [AI-indeling] Lagen verwerken in contentstroomoperatoren**

{{< highlight csharp >}}
string bronbestand = Path.Combine(basismap, "Lagen-ZonderPen.ai");
string uitvoerbestand = Path.Combine(uitvoermap, "Lagen-ZonderPen.uitvoer.png");

gebruikend (AiAfbeelding afbeelding = (AiAfbeelding)Afbeelding.Laden(bronbestand))
{
    afbeelding.Opslaan(uitvoerbestand, nieuwe PngOpties());
}

//// Curven van laag met de naam "Pen" moeten verborgen zijn
{{< /highlight >}}

**PSDNET-2015. Weergaveresultaat van AI-bestand verschilt sterk in vergelijking met Illustrator-resultaten**

{{< highlight csharp >}}
string bronbestand = Path.Combine(basismap, "4.ai");
string uitvoerbestandspad = Path.Combine(uitvoermap, "4.png");

gebruikend (AiAfbeelding afbeelding = (AiAfbeelding)Afbeelding.Laden(bronbestand))
{
    afbeelding.Opslaan(uitvoerbestandspad, nieuwe PngOpties());
}
{{< /highlight >}}

**PSDNET-2093. Opnieuw koppelen van Smart Object is niet van toepassing op alle Smart Objects in het PSD-bestand**

{{< highlight csharp >}}
string[] bestanden = { "eenvoudige_test", "w22" };
string wijzigingsbestand = Path.Combine(basismap, "afbeelding(19).png");

string[] bronbestand = nieuwe string[bestanden.Lengte];
string[] uitvoerBestanden = nieuwe string[bestanden.Lengte];

voor (int i = 0; i < bestanden.Lengte; i++)
{
    bronbestand[i] = Path.Combine(basismap, bestanden[i] + ".psd");
    uitvoerBestanden[i] = Path.Combine(uitvoermap, bestanden[i] + "_uitvoer.psd");

    gebruikend (var afbeelding = (PsdAfbeelding)Afbeelding.Laden(bronbestand[i]))
    {
        voor elke (Laag laag in afbeelding.Lagen)
        {
            als (laag is SmartObjectLayer)
            {
                SmartObjectLayer slim = (SmartObjectLayer)laag;

                // Voor de tweede slimme laag was hier een fout
                slim.VervangInhoud(wijzigingsbestand);
            }
        }

        afbeelding.Opslaan(uitvoerBestanden[i]);
    }
}
{{< /highlight >}}
