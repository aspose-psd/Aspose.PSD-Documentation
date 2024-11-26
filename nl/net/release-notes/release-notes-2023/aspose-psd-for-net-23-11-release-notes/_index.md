---
title: Aspose.PSD voor .NET 23.11 - Release-opmerkingen
type: docs
weight: 20
url: /nl/net/aspose-psd-voor-net-23-11-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 23.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel** | **Samenvatting** | **Categorie** |
|:------------|:-----------------|:--------|
| PSDNET-412 | Ondersteuning van LMskResource | Functie |
| PSDNET-1669 | [AI-formaat] Toevoegen van de mogelijkheid om een PDF-gebaseerd AI-bestand te renderen met Aspose.PSD | Functie |
| PSDNET-1702 | [AI-formaat] Toevoegen van ondersteuning voor de "cm" PostScript-operator | Functie |
| PSDNET-1752 | Nieuwe soorten warp toevoegen: Golf, schelp omhoog, schelp omlaag | Functie |
| PSDNET-1797 | Ondersteuning toevoegen voor verticale warp | Functie |
| PSDNET-1756 | System.ArgumentNullException: 'Waarde kan niet null zijn. (Parameter 'key')' bij het oproepen van TextLayer.GetFonts() | Fout |


## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- M:Aspose.PSD.FontSettings.RemoveFontCacheFile
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorSpace
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent1
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent3
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent4
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Flag
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.CMYK
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.Lab
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.GrayScale


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**
**PSDNET-412. Ondersteuning van LMskResource**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "bronBestand.psd");
string uitvoerPsd = Path.Combine(uitvoerMap, "bronBestand_output.psd");

void AssertAreEqual(object verwacht, object werkelijk)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception("Objecten zijn niet gelijk.");
    }
}

// Laad 16-bits afbeelding.
using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand))
{
    // Zoek LmskResource.
    LmskResource lmskResource = new LmskResource();
    foreach (var res in afbeelding.GlobalLayerResources)
    {
        if (res is LmskResource)
        {
            lmskResource = (LmskResource)res;
            break;
        }
    }

    // Controleer LmskResource eigenschappen.
    AssertAreEqual(lmskResource.ColorSpace, PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB);
    AssertAreEqual(lmskResource.ColorComponent1, (ushort)65535);
    AssertAreEqual(lmskResource.ColorComponent2, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent3, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent4, (ushort)0);
    AssertAreEqual(lmskResource.Opacity, (short)45);
    AssertAreEqual(lmskResource.Flag, (byte)128);

    // Wijzig LmskResource eigenschappen.
    lmskResource.ColorSpace = PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB;
    lmskResource.ColorComponent1 = 7854;
    lmskResource.ColorComponent2 = 10;
    lmskResource.ColorComponent3 = 15484;
    lmskResource.Opacity = 85;

    // Sla de afbeelding op.
    afbeelding.Save(uitvoerPsd);
}
{{< /highlight >}}

**PSDNET-1669. [AI-formaat] Toevoegen van de mogelijkheid om een PDF-gebaseerd AI-bestand te renderen met Aspose.PSD**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "ai_one.ai");
string uitvoerPng = Path.Combine(uitvoerMap, "ai_one_output.png");

// Laad de PDF-gebaseerde AI-afbeelding.
using (AiImage afbeelding = (AiImage)Image.Load(bronBestand))
{
    // Sla de AI-afbeelding op als een PNG-afbeelding.
    afbeelding.Save(uitvoerPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1702. [AI-formaat] Toevoegen van ondersteuning voor de "cm" PostScript-operator**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "ai_two.ai");
string uitvoerPng = Path.Combine(uitvoerMap, "ai_two_output.png");

// Laad de AI-afbeelding.
using (AiImage afbeelding = (AiImage)Image.Load(bronBestand))
{
    // Sla de AI-afbeelding op als een PNG-afbeelding.
    afbeelding.Save(uitvoerPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1752. Nieuwe soorten warp toevoegen: Golf, schelp omhoog, schelp omlaag**

{{< highlight csharp >}}
var laadOpties = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var opslaanOpties = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string bronBestandVis = Path.Combine(basisMap, "1752_warp_fish.psd");
string bronBestandRise = Path.Combine(basisMap, "1752_warp_rise.psd");
string bronBestandGolf = Path.Combine(basisMap, "1752_warp_wave.psd");

string uitvoerBestandVis = Path.Combine(uitvoerMap, "1752_output_fish.png");
string uitvoerBestandRise = Path.Combine(uitvoerMap, "1752_output_rise.png");
string uitvoerBestandGolf = Path.Combine(uitvoerMap, "1752_output_wave.png");

using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandVis, laadOpties))
{
    psdAfbeelding.Save(uitvoerBestandVis, opslaanOpties);
}

using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandRise, laadOpties))
{
    psdAfbeelding.Save(uitvoerBestandRise, opslaanOpties);
}

using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandGolf, laadOpties))
{
    psdAfbeelding.Save(uitvoerBestandGolf, opslaanOpties);
}
{{< /highlight >}}

**PSDNET-1756. System.ArgumentNullException: 'Waarde kan niet null zijn. (Parameter 'key')' bij het oproepen van TextLayer.GetFonts()**

{{< highlight csharp >}}
string bron = Path.Combine(basisMap, "SimpleText.psd");

FontSettings.RemoveFontCacheFile();

using (var psdAfbeelding = (PsdImage)Image.Load(bron))
{
    foreach (var laag in psdAfbeelding.Layers)
    {
        if (laag is TextLayer tekstlaag)
        {
            tekstlaag.GetFonts();
        }
    }
}
{{< /highlight >}}

**PSDNET-1797. Verticale warp-ondersteuning toevoegen**

{{< highlight csharp >}}
var laadOpties = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var opslaanOpties = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string bronBestandBoogOnder = Path.Combine(basisMap, "1797_warp_arc_lower_v.psd");
string bronBestandBoogBoven = Path.Combine(basisMap, "1797_warp_arc_upper_v.psd");
string bronBestandBoog = Path.Combine(basisMap, "1797_warp_arch_v.psd");
string bronBestandBolling = Path.Combine(basisMap, "1797_warp_bulge_v.psd");
string bronBestandVlag = Path.Combine(basisMap, "1797_warp_flag_v.psd");
string bronBestandVis = Path.Combine(basisMap, "1797_warp_fish_v.psd");
string bronBestandRise = Path.Combine(basisMap, "1797_warp_rise_v.psd");
string bronBestandGolf = Path.Combine(basisMap, "1797_warp_wave_v.psd");

string uitvoerBestandBoogOnder = Path.Combine(uitvoerMap, "1797_warp_arc_lower_v.png");
string uitvoerBestandBoogBoven = Path.Combine(uitvoerMap, "1797_warp_arc_upper_v.png");
string uitvoerBestandBoog = Path.Combine(uitvoerMap, "1797_warp_arch_v.png");
string uitvoerBestandBolling = Path.Combine(uitvoerMap, "1797_warp_bulge_v.png");
string uitvoerBestandVlag = Path.Combine(uitvoerMap, "1797_warp_flag_v.png");
string uitvoerBestandVis = Path.Combine(uitvoerMap, "1797_output_fish_v.png");
string uitvoerBestandRise = Path.Combine(uitvoerMap, "1797_output_rise_v.png");
string uitvoerBestandGolf = Path.Combine(uitvoerMap, "1797_output_wave_v.png");

using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandBoogOnder, laadOpties)) { psdAfbeelding.Save(uitvoerBestandBoogOnder, opslaanOpties); }
using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandBoogBoven, laadOpties)) { psdAfbeelding.Save(uitvoerBestandBoogBoven, opslaanOpties); }
using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandBoog, laadOpties)) { psdAfbeelding.Save(uitvoerBestandBoog, opslaanOpties); }
using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandBolling, laadOpties)) { psdAfbeelding.Save(uitvoerBestandBolling, opslaanOpties); }
using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandVlag, laadOpties)) { psdAfbeelding.Save(uitvoerBestandVlag, opslaanOpties); }
using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandVis, laadOpties)) { psdAfbeelding.Save(uitvoerBestandVis, opslaanOpties); }
using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandRise, laadOpties)) { psdAfbeelding.Save(uitvoerBestandRise, opslaanOpties); }
using (var psdAfbeelding = (PsdImage)Image.Load(bronBestandGolf, laadOpties)) { psdAfbeelding.Save(uitvoerBestandGolf, opslaanOpties); }
{{< /highlight >}}
