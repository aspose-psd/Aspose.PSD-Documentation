---
title: Aspose.PSD voor .NET 22.7 - Release-opmerkingen
type: docs
weight: 60
url: /nl/net/aspose-psd-voor-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-482|Ondersteuning van Beeldsectie Resource #4000-4999 Plug-In resource(s)|Functie|
|PSDNET-875|Een niet-afgehandelde uitzondering van het type "System.OutOfMemoryException" treedt op in Aspose.PSD.dll|Fout|
|PSDNET-1050|Na het exporteren van het PSD-bestand is het resultaat veel groter dan het brondocument|Fout|
|PSDNET-1083|Onjuiste parsing van gegevens voor XmpResource|Fout|
|PSDNET-1205|Na exporteren is de grootte van PSD-bestanden met submappen toegenomen|Fout|


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
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


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-482. Ondersteuning van Beeldsectie Resource #4000-4999 Plug-In resource(s)**

{{< highlight csharp >}}
// De volgende code toont hoe de vertragingstijd in de tijdlijnkader van geanimeerde gegevens ingesteld/bijgewerkt kan worden.
string bronBestand = "3_animated.psd";
string uitvoerPsd = "uitvoer_3_animated.psd";

T VindStructuur<T>(IEnumerable<OSTypeStructure> structuren, string keyNaam) where T : OSTypeStructure
{
    foreach (var structuur in structuren)
    {
        if (structuur.KeyName.ClassName == keyNaam)
        {
            return structuur as T;
        }
    }

    return null;
}

OSTypeStructure[] ToevoegenOfVervangenStructuur(IEnumerable<OSTypeStructure> structuren, OSTypeStructure nieuweStructuur)
{
    List<OSTypeStructure> lijstVanStructuren = new List<OSTypeStructure>(structuren);

    for (int i = 0; i < lijstVanStructuren.Count; i++)
    {
        OSTypeStructure structuur = lijstVanStructuren[i];
        if (structuur.KeyName.ClassName == nieuweStructuur.KeyName.ClassName)
        {
            lijstVanStructuren.RemoveAt(i);
            break;
        }
    }

    lijstVanStructuren.Add(nieuweStructuur);

    return lijstVanStructuren.ToArray();
}

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand))
{
    foreach (var afbeeldingsResource in afbeelding.ImageResources)
    {
        if (afbeeldingsResource is AnimatedDataSectionResource)
        {
            var geanimeerdeData =
            (AnimatedDataSectionStructure) (afbeeldingsResource as AnimatedDataSectionResource).AnimatedDataSection;
            var framesLijst = VindStructuur<ListStructure>(geanimeerdeData.Items, "FrIn");

            var kader1 = (DescriptorStructure)framesLijst.Types[1];

            // Maakt het kadervertraging record met waarde 100 centi-seconde dat gelijk is aan 1 seconde.
            var kaderVertraging = new IntegerStructure(new ClassID("FrDl"));
            kaderVertraging.Value = 100; // instellen van tijd in centi-seconden.

            kader1.Structuren = ToevoegenOfVervangenStructuur(kader1.Structuren, kaderVertraging);

            break;
        }
    }

    afbeelding.Save(uitvoerPsd);
}
{{< /highlight >}}

**PSDNET-875. Een niet-afgehandelde uitzondering van het type "System.OutOfMemoryException" treedt op in Aspose.PSD.dll**

{{< highlight csharp >}}
string srcBestand = "001-.psd";
string jpgBestandsPad = "T_0003.jpg";
string uitvoerBestandsPad = "uitvoer_nieuwPsd.psd";

using (var im = (PsdImage)Image.Load(srcBestand))
{
    using (FileStream fs = new FileStream(jpgBestandsPad, FileMode.Open))
    {
        var nieuweLaag = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        nieuweLaag.DisplayName = "NieuweLaag";

        im.AddLayer(nieuweLaag);

        im.Save(uitvoerBestandsPad, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Na het exporteren van het PSD-bestand is het resultaat veel groter dan het brondocument**

{{< highlight csharp >}}
string bron = "ShimadzuLetterhead100.psd";
string uitvoer = "uitvoer.psd";
using (var afb = (PsdImage)Image.Load(bron))
{
    afb.Save(uitvoer);
}

double uitvoerGrootteMb = new FileInfo(uitvoer).Length / 1024d / 1024d;
if (uitvoerGrootteMb > 6)
{
    throw new Exception("Het uitvoerbestand is groter dan zou moeten zijn.");
}
{{< /highlight >}}

**PSDNET-1083. Onjuiste parsing van gegevens voor XmpResource**

{{< highlight csharp >}}
string invoerPsdAfbeeldingPad = @"invoer.psd";
string opgeslagenPsdAfbeeldingPad = @"opgeslagen.psd";

bool isOrigineelBevatten = false;
bool isOpgeslagenBevatten = false;

// Zoek de sub-XMP-sleutel in het invoerbestand.
using (PsdImage img = (PsdImage)Image.Load(invoerPsdAfbeeldingPad))
{
    foreach (var pakket in img.XmpData.Packages)
    {
        foreach (var pak in pakket)
        {
            if (pak.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pak.Value;

                string xmlWaarde = xmpArray.GetXmlValue();

                if (xmlWaarde.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    isOrigineelBevatten = true;
                    break;
                }
            }
        }

        if (isOrigineelBevatten)
        {
            break;
        }
    }
    img.Save(opgeslagenPsdAfbeeldingPad);
}

// Zoek de sub-XMP-sleutel in het opgeslagen bestand.
using (PsdImage img = (PsdImage)Image.Load(opgeslagenPsdAfbeeldingPad))
{
    foreach (var pakket in img.XmpData.Packages)
    {
        foreach (var pak in pakket)
        {
            if (pak.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pak.Value;

                string xmlWaarde = xmpArray.GetXmlValue();

                if (xmlWaarde.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    isOpgeslagenBevatten = true;
                    break;
                }
            }
        }

        if (isOpgeslagenBevatten)
        {
            break;
        }
    }
    img.Save(opgeslagenPsdAfbeeldingPad);
}

if (isOrigineelBevatten && isOpgeslagenBevatten)
{
    // Alles is in orde!
}
else
{
    throw new Exception("Het werkt niet");
}
{{< /highlight >}}

**PSDNET-1205. Na exporteren is de grootte van PSD-bestanden met submappen toegenomen**

{{< highlight csharp >}}
string[] bronBestanden = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var bestandsNaam in bronBestanden)
{
    string bronBestandPad = bestandsNaam;
    string uitvoerBestandPad = "uitvoer_" + bestandsNaam;

    using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandPad))
    {
        afbeelding.Save(uitvoerBestandPad);
    }

    double uitvoerGrootteMb = new FileInfo(uitvoerBestandPad).Length / 1024d / 1024d;
    if (uitvoerGrootteMb > 1.9)
    {
        throw new Exception("Het uitvoerbestand is groter dan zou moeten zijn.");
    }
}
{{< /highlight >}}
