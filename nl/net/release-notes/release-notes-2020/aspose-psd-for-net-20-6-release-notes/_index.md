---
title: Aspose.PSD voor .NET 20.6 - Release-opmerkingen
type: docs
weight: 70
url: /nl/net/aspose-psd-voor-net-20-6-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Belangrijkste**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-606 |Ondersteuning van LnkE-bron|Functie|
|PSDNET-386 |Ondersteuning van britResource (Bron van Helderheid/Contrast Aanpassingslaag)|Functie|
|PSDNET-219|Verplaatsing van instelling DefaultReplacementFont naar ImageOptionsBase-class|Verbetering|
|PSDNET-596|Lagengroep met niet PassThrough-Mengmodus wordt niet weergegeven|Fout|
|PSDNET-610|NullReference-uitzondering bij het converteren van een specifiek Psd-bestand naar afbeelding|Fout|
|PSDNET-636|Het vergroten/verkleinen van PSD-bestanden werkt incorrect als er een masker is in de aanpassingslaag met lege grenzen|Fout|
|PSDNET-611|OverflowException bij het openen van een bepaald Psd-bestand|Fout|
|PSDNET-565|Psd-afbeelding met RGB-modus 16 bit/kanaal werkt lagen alleen bij voorbeeldwerk bij|Fout|
|PSDNET-652|Uitzondering bij laden van specifiek PSD-bestand met de samengestelde LnkE-bron en adobeStockLicenseState-eigenschap|Fout|
|PSDNET-640|Wijzigingen in PSD-laagmaskers worden niet opgeslagen|Fout|
|PSDNET-593|Opslaan van AI-bestand naar Jpeg2000-indeling werkt niet|Fout|
|PSDNET-638|Onjuiste volgorde van lagen nadat u een lagengroep toevoegt aan een lege lagengroep|Fout|

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.MaskRectangle
- P:Aspose.PSD.ImageOptionsBase.DefaultReplacementFont
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Type
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileCreator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.ChildDocId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetModTime
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetLockedState
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.IsLibraryLink
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.HasFileOpenDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Length
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.None
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFD
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFE
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFA
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.Date
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileSize
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FullPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.RelativePath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementRef
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockLicenseState
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.IsEmpty
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.DataSourceCount
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.StringStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String)
# **Verwijderde API's:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Gebruik voorbeelden:**
**PSDNET-606. Ondersteuning van LnkE-bron**

{{< highlight java >}}

 string bericht = "Voorbeeld van ondersteuning van LnkE-bron werkt onjuist.";

void AssertIsTrue(bool voorwaarde)

{

    if (!voorwaarde)

    {

        throw new FormatException(bericht);

    }

}

void AssertAreEqual(object werkelijk, object verwacht)

{

    if (!object.Equals(werkelijk, verwacht))

    {

        throw new FormatException(bericht);

    }

}

// Dit voorbeeld laat zien hoe u eigenschappen van de Photoshop Psd LnkE-bron kunt ophalen en instellen die informatie bevat over een extern gekoppeld bestand.

void VoorbeeldVanLnkEResourceOndersteuning(

    string bestandsPad,

    int lengte,

    int lengte2,

    int lengte3,

    int lengte4,

    string volledigPad,

    string datum,

    double assetModTijd,

    string childDocId,

    bool vergrendeld,

    string uid,

    string naam,

    string origineleBestandsNaam,

    string bestandsType,

    long grootte)

{

    string bestandsNaam = Path.GetFileName(bestandsPad);

    string uitvoerPad = @"Output\" + bestandsNaam;

    using (PsdImage afbeelding = (PsdImage)Image.Load(bestandsPad))

    {

        LnkeResource lnkeResource = null;

        foreach (var bron in afbeelding.GlobalLayerResources)

        {

            lnkeResource = bron as LnkeResource;

            if (lnkeResource != null)

            {

                AssertAreEqual(lnkeResource.Length, lengte);

                AssertAreEqual(lnkeResource.UniqueId, new Guid(uid));

                AssertAreEqual(lnkeResource.FullPath, volledigPad);

                AssertAreEqual(lnkeResource.Date.ToString(CultureInfo.InvariantCulture), datum);

                AssertAreEqual(lnkeResource.AssetModTime, assetModTijd);

                AssertAreEqual(lnkeResource.AssetLockedState, vergrendeld);

                AssertAreEqual(lnkeResource.FileName, naam);

                AssertAreEqual(lnkeResource.FileSize, grootte);

                AssertAreEqual(lnkeResource.ChildDocId, childDocId);

                AssertAreEqual(lnkeResource.Version, 7);

                AssertAreEqual(lnkeResource.FileType, bestandsType);

                AssertAreEqual(lnkeResource.FileCreator, string.Empty);

                AssertAreEqual(lnkeResource.OriginalFileName, origineleBestandsNaam);

                AssertAreEqual(lnkeResource.CompId, -1);

                AssertAreEqual(lnkeResource.OriginalCompId, -1);

                AssertIsTrue(lnkeResource.HasFileOpenDescriptor);

                AssertIsTrue(!lnkeResource.IsEmpty);

                AssertIsTrue(lnkeResource.Type == LinkResourceType.liFE);

                lnkeResource.FullPath = @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png";

                AssertAreEqual(lnkeResource.Length, lengte2);

                lnkeResource.FileName = "rgb8_2x23.png";

                AssertAreEqual(lnkeResource.Length, lengte3);

                lnkeResource.ChildDocId = Guid.NewGuid().ToString();

                AssertAreEqual(lnkeResource.Length, lengte4);

                lnkeResource.Date = DateTime.Now;

                lnkeResource.AssetModTime = double.MaxValue;

                lnkeResource.FileSize = long.MaxValue;

                lnkeResource.FileType = "test";

                lnkeResource.FileCreator = "file";

                lnkeResource.CompId = int.MaxValue;

                break;

            }

        }

        AssertIsTrue(lnkeResource != null);

        afbeelding.Save(uitvoerPad, new PsdOptions(afbeelding));

    }

    using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerPad))

    {

        afbeelding.Save(

            Path.ChangeExtension(uitvoerPad, "png"),

            new PngOptions

            {

                ColorType = PngColorType.TruecolorWithAlpha

            });

    }

}

// Dit voorbeeld toont hoe u eigenschappen van de Psd LnkE-bron kunt ophalen en instellen die informatie bevat over extern gekoppelde JPEG-bestand.

this.VoorbeeldVanLnkEResourceOndersteuning(

    @"..\..\..\Issues\IMAGINGNET-2375\photooverlay_5_new.psd",

    0x21c,

    0x26c,

    0x274,

    0x27c,

    @"file:///C:/Users/cvallejo/Desktop/photo.jpg",

    "05/09/2017 22:24:51",

    0,

    "F062B9DB73E8D124167A4186E54664B0",

    false,

    "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

    "photo.jpg",

    "photo.jpg",

    "JPEG",

    0x1520d);

// Dit voorbeeld toont hoe u eigenschappen van de Photoshop Psd LnkE-bron kunt ophalen en instellen die informatie bevat over een externe gekoppelde PNG-afbeelding.

this.VoorbeeldVanLnkEResourceOndersteuning(

    "rgb8_2x2_linked.psd",

    0x284,

    0x290,

    0x294,

    0x2dc,

    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

    "04/14/2020 14:23:44",

    0,

    "",

    false,

    "5867318f-3174-9f41-abca-22f56a75247e",

    "rgb8_2x2.png",

    "rgb8_2x2.png",

    "png",

    0x53);

// Dit voorbeeld toont hoe u eigenschappen van de Photoshop Psd LnkE-bron kunt ophalen en instellen die informatie bevat over een extern gekoppelde CC Libraries Asset.

this.VoorbeeldVanLnkEResourceOndersteuning(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Functie beschikbaar in Photoshop CC 2015)",

    "01/01/0001 00:00:00",

    1588890915488.0d,

    "",

    false,

    "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

    "rgb8_2x2_linked",

    "rgb8_2x2.png",

    "png",

    0);

{{< /highlight >}}

**PSDNET-201. Ondersteuning voor documentconversievoortgang**

{{< highlight java >}}

 string bronBestandsPad = "Apple.psd";

Stream uitvoerStream = new MemoryStream();

ProgressEventHandler lokaleProgressEventHandler = delegate(ProgressEventHandlerInfo voortgangsInfo)

{

      string bericht = string.Format(

           "{0} {1}: {2} van {3}",

           voortgangsInfo.Omschrijving,

           voortgangsInfo.GebeurtenisType,

           voortgangsInfo.Waarde,

           voortgangsInfo.MaxValue);

      Console.WriteLine(bericht);

};

Console.WriteLine("---------- Laden van Apple.psd ----------");

var laadOpties = new PsdLoadOptions() { ProgressEventHandler = lokaleProgresseventHandler };

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsPad, laadOpties))

{

      Console.WriteLine("---------- Opslaan van Apple.psd naar PNG-indeling ----------");

      afbeelding.Save(

           uitvoerStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = lokaleProgressEventHandler

           });

      Console.WriteLine("---------- Opslaan van Apple.psd naar PSD-indeling ----------");

      afbeelding.Save(

           uitvoerStream,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = lokaleProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-386. Ondersteuning van britResource (Bron van Helderheid/Contrast Aanpassingslaag)**

{{< highlight java >}}

 /* Dit voorbeeld toont hoe u programmatisch de PSD-afbeelding Helderheid/Contrast-laagbron - BritResource kunt wijzigen

   Dit is een low-level Aspose.PSD API. U kunt de Helderheid/Contrast-laag gebruiken via de API, wat veel eenvoudiger zal zijn, 

   maar directe bewerking van Photoshop-bronnen geeft u meer controle over de inhoud van het PSD-bestand.  */

string pad = @"BrightnessContrastPS6.psd";

string uitvoerPad = @"BrightnessContrastPS6_output.psd";

using (PsdImage afbeelding = (PsdImage)Image.Load(pad))

{

    foreach (var laag in afbeelding.Layers)

    {

        if (laag is BrightnessContrastLayer)

        {

            foreach (var laagBron in laag.Resources)

            {

                if (laagBron is BritResource)

                {

                    var bron = (BritResource)laagBron;

                    isRequiredResourceFound = true;

                    if (bron.Brightness != -40 ||

                        bron.Contrast != 10 ||

                        bron.LabColor != false ||

                        bron.MeanValueForBrightnessAndContrast != 127)

                    {

                        throw new Exception("BritResource is fout gelezen");

                    }

                    // Test bewerken en opslaan

                    bron.Brightness = 25;

                    bron.Contrast = -14;

                    bron.LabColor = true;

                    bron.MeanValueForBrightnessAndContrast = 200;

                    afbeelding.Save(uitvoerPad, new PsdOptions());

                    break;

                }

            }

        }

    }

}

{{< /highlight >}}

**PSDNET-596. Lagengroep met niet PassThrough-Mengmodus wordt niet weergegeven**

{{< highlight java >}}

 string bronBestandsPad = "MaskTestNormalBlendMaskOnGroup.psd";

string uitvo