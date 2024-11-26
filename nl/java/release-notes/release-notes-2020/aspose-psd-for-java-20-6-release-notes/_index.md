---
title: Aspose.PSD voor Java 20.6 - Release-opmerkingen
type: docs
weight: 50
url: /nl/java/aspose-psd-voor-java-20-6-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose-psd-voor-java-20.6/) {{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDJAVA-216|Ondersteuning van LnkEResource (Resource van Slim Object laag)|Mogelijkheid|
|PSDJAVA-219|Ondersteuning van britResource (Resource van Helderheid/Contrast Aanpassingslaag)|Mogelijkheid|
|PSDJAVA-222|Verplaatsing van de standaardvervangingslettertype-instelling naar de ImageOptionsBase-klasse|Verbetering|
|PSDJAVA-217|Het formaat wijzigen van PSD-bestanden werkt niet correct als er een masker in de aanpassingslaag is met lege grenzen|Fout|
|PSDJAVA-218|Psd-afbeelding met RGB-modus 16 bit/kanaal werkt lagen alleen bij voorbeeld bijwerken|Fout|
|PSDJAVA-220|PSD-laagmaskerwijzigingen worden genegeerd bij opslaan|Fout|
|PSDJAVA-221|Incorrecte laagvolgorde nadat u een lege laaggroep toevoegt aan een lege laaggroep|Fout|
|PSDJAVA-223|Uitzondering bij het laden van een specifiek PSD-bestand met de samengestelde LnkE-bron en adobeStockLicenseState-eigenschap|Fout|
|PSDJAVA-224|Opslaan van AI-bestand naar Jpeg2000-indeling werkt niet|Fout|
|PSDJAVA-225|Laaggroep met niet Doorgeven Samenvoegingsmodus wordt niet weergegeven|Fout|
|PSDJAVA-226|NullReference-uitzondering bij het proberen een bepaald Psd-bestand naar afbeelding te converteren|Fout|
|PSDJAVA-227|OverflowException bij het proberen een bepaald Psd-bestand te openen|Fout|

# **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources```java
.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **Verwijderde API's:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
```

**Gebruik voorbeelden:**

**PSDJAVA-216: Ondersteuning van LnkEResource (Resource van Slim Object laag)**

{{< highlight java >}}

 // Een voorbeeld van het koppelen van verschillende soorten assets (rasterafbeeldingen, CC-bibliotheken) aan PSD.

// Ook wordt de API van LnkeResource overwogen.

// Een klasse die methoden in de lokale scope houdt

class LocalScopeExtension

{

    void assertIsTrue(boolean conditie)

    {

        if (!conditie)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport werkt incorrect.");

        }

    }

    void assertAreEqual(Object daadwerkelijk, Object verwacht)

    {

        assertIsTrue(daadwerkelijk != null && daadwerkelijk.equals(verwacht));

    }

    // Dit voorbeeld laat zien hoe u eigenschappen van de Photoshop Psd LnkE kunt krijgen en instellen

    // Resource dat informatie bevat over een extern gekoppeld bestand.

    void exampleOfLnkEResourceSupport(

            String bestandsnaam,

            int lengte,

            int lengte2,

            int lengte3,

            int lengte4,

            String volledigPad,

            String datum,

            double assetModTijd,

            String childDocId,

            boolean vergrendeld,

            String uid,

            String naam,

            String origineleBestandsnaam,

            String bestandstype,

            lang size)

    {

        String outputPad = "out_" + bestandsnaam;

        // Laad een vooraf gedefinieerde PSD

        PsdImage afbeelding = (PsdImage)Image.load(bestandsnaam);

        probeer

        {

            // Zoek LnkeResource tussen de globale resources

            LnkeResource lnkeResource = null;

            voor (LayerResource resource : afbeelding.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Controleer of de eigenschappen van LnkeResource juist zijn gelezen

                    assertAreEqual(lnkeResource.getLength(), lengte);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), volledigPad);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), datum);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTijd);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), vergrendeld);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), naam);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), grootte);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), bestandstype);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), origineleBestandsnaam);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // Update LnkeResource eigenschappen

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), lengte2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), lengte3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), lengte4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    breken;

                }

            }

            // Zorg ervoor dat LnkeResource wordt ondersteund

            assertIsTrue(lnkeResource != null);

            // Sla een kopie van de geladen PSD op

            afbeelding.save(outputPad, nieuwe PsdOptions(afbeelding));

        }

        eindelijk

        {

            afbeelding.dispose();

        }

        // Laad de opgeslagen kopie

        PsdImage afbeelding1 = (PsdImage)Image.load(outputPad);

        probeer

        {

            // Converteer PSD naar PNG-bestandsindeling (met alfakanaal voor transparantie)

            PngOptions pngOpties = nieuwe PngOptions();

            pngOpties.setColorType(PngColorType.TruecolorWithAlpha);

            afbeelding1.save(Path.changeExtension(outputPad, "png"), pngOpties);

        }

        eindelijk

        {

            afbeelding1.dispose();

        }

    }

}

LocalScopeExtension $ = nieuwe LocalScopeExtension();

// Dit voorbeeld laat zien hoe u eigenschappen van de Psd LnkE-bron kunt krijgen en instellen

// die informatie bevat over extern gekoppeld JPEG-bestand.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Dit voorbeeld laat zien hoe u eigenschappen van de PSD LnkE-bron kunt krijgen en instellen

// dat informatie bevat over een extern gekoppeld PNG-bestand.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Dit voorbeeld laat zien hoe u eigenschappen van de Photoshop Psd LnkE-bron

// die informatie bevat over een extern gekoppeld CC-bibliothekenasset.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Functie is beschikbaar in Photoshop CC 2015)",

        "01/01/0001 00:00:00",

        1588890915488.0d,

        "",

        false,

        "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

        "rgb8_2x2_linked",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0);


{{< /highlight >}}

**PSDJAVA-219: Ondersteuning van britResource (Resource van Helderheid/Contrast Aanpassingslaag)**

{{< highlight java >}}

 // Dit Voorbeeld toont hoe u programmatisch de Helderheid/Contrast Aanpassingslaag Resource - BritResource kunt wijzigen. Dit is een Low-Level Aspose.PSD API.

// U kunt de Helderheid/Contrast Aanpassingslaag gebruiken via de API, wat veel eenvoudiger zal zijn,

// maar directe bewerking van fotoshop-resources geeft u meer controle over de inhoud van het PSD-bestand.

String srcPad = "BrightnessContrastPS6.psd";

String dstPad = "BrightnessContrastPS6_output.psd";

// Laad een Photoshop-document met een Helderheid/Contrast aanpassingslaag

PsdImage psdAfbeelding = (PsdImage)Image.load(srcPad);

probeer

{

    // Zoeken naar BritResource

    voor (Laag laag : psdAfbeelding.getLayers())

    {

        if (laag instanceof HelderheidContrastLaag)

        {

            voor (LayerResource layerResource : laag.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Controleer resource-eigenschappen

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw nieuwe RuntimeException("BritResource is verkeerd gelezen");

                    }

                    // Update resource-eigenschappen

                    resource.setBrightness((kort)25);

                    resource.setContrast((kort)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((kort)200);

                    // Sla een kopie op van de bijgewerkte PSD

                    psdAfbeelding.save(dstPad, nieuwe PsdOptions());

                    breken;

                }

            }

        }

    }

}

eindelijk

{

    psdAfbeelding.dispose();

}

{{< /highlight >}}

**PSDJAVA-217: Het formaat wijzigen van PSD-bestanden werkt niet correct als er een masker in de aanpassingslaag is met lege grenzen**

{{< highlight java >}}

 // Een voorbeeld van het formaat wijzigen van een afbeelding die een aanpassingslaagmasker heeft met lege grenzen.

// Het programma laadt een vooraf gedefinieerde PSD alleen om te controleren of er geen uitzonderingen zijn.

definitieve schaal = 2; // willekeurige coëfficiënt

String[] namen = {

        "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

        "LevelsLayerWithLayerMaskRgb",

        "LevelsLayerWithLayerMaskCmyk",

};

voor (String naam : namen)

{

    String srcBestandsPad = naam + ".psd";

    String dstBestandsPad = "output_" + srcBestandsPad;

    String dstPngBestandsPad = "output_" + naam + ".png";

    // Laad een vooraf gedefinieerde PSD met een aanpassingslaagmasker met lege grenzen

    PsdLoadOpties psdLaadOpties = nieuwe PsdLaadOpties();

    psdLaadOpties.setLoadEffectsResource(true);

    PsdImage afbeelding = (PsdImage)Image.load(srcBestandsPad, psdLaadOpties);

    probeer

    {

        // Wijzig het formaat van de afbeelding

        afbeelding.formaat afbeelding(image.getWidth() * schaal, afbeelding.getHeight() * schaal);

        // Sla een kopie op van de geladen PSD

        afbeelding.save(dstBestandsPad, nieuwe PsdOpties());

        // Exporteer PSD naar PNG-bestandsindeling (met alfakanaal voor transparantie)

        PngOpties pngOpties = nieuwe PngOpties();

        pngOpties.setColorType(PngColorType.TruecolorWithAlpha);

        afbeelding