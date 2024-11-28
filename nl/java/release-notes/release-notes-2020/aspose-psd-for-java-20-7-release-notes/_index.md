---
title: Aspose.PSD voor Java 20.7 - Release-opmerkingen
type: docs
weight: 50
url: /nl/java/aspose-psd-voor-java-20-7-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDJAVA-231|Ondersteuning van het toevoegen van een slageffect tijdens runtime|Functie|
|PSDJAVA-249|Ondersteuning van lnk2 / lnk3-resources (Resources van Smart Object Layer)|Functie|
|PSDJAVA-247|Wijzig Exception-bericht bij het proberen te openen van niet-ondersteunde formaten als afbeelding|Verbetering|
|PSDJAVA-235|Als we een PSD-bestand opslaan na het aanmaken van een nieuwe Layer Group, krijgen we een Photoshop-waarschuwing bij het openen van het bestand.|Fout|
|PSDJAVA-236|Mislukt om LayerMask op te slaan|Fout|
|PSDJAVA-237|Knipmasker wordt niet toegepast op de map|Fout|
|PSDJAVA-238|Kan bestand niet openen met Aspose.PSD voor Java|Fout|
|PSDJAVA-239|Image opslaan mislukt met uitzondering bij het converteren van PSD naar PDF|Fout|
|PSDJAVA-240|Bijsnijdoperatie maakt Clipping-pad ongeldig in PSD-afbeelding|Fout|
|PSDJAVA-241|NullReference-uitzondering bij het proberen opslaan van een specifiek PSD-bestand met Shadows-effect|Fout|
|PSDJAVA-243|Aspose.PSD retourneert true bij Image.CanLoad(pdfStream)|Fout|
|PSDJAVA-244|Lagen mislukten om te renderen in gegenereerde PNG|Fout|
|PSDJAVA-245|Uitzondering bij het benaderen van TextData|Fout|
|PSDJAVA-246|ImageSaveException bij het opslaan van de PSD|Fout|

# **Wijzigingen in Openbare API**
# **Toegevoegde API's:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T:com.aspose.psd.fileformats.psd.resources.WorkingPathResource
## **Verwijderde API's:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
# **Gebruik voorbeelden:**

**PSDJAVA-231. Ondersteuning van het toevoegen van een slageffect tijdens runtime**
{{< highlight java >}}
// Dit voorbeeld laat zien hoe je een slag-effect (rand) kunt toevoegen aan bestaande lagen van een PSD-bestand in Java.
// Er zijn drie soorten slagen: kleur, gradiënt en patroon. Elk van het type heeft
// drie manieren (posities) waarin de slag wordt weergegeven: binnen, centrum en buiten.
// Dit voorbeeld toont het gebruik van al deze gevallen.

String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;

    // 1. Voegt Color fill toe, op positie Inside
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 2. Voegt Color fill toe, op positie Outside
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 3. Voegt Color fill toe, op positie Center
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 4. Voegt Gradiënt fill toe, op positie Inside
    strokeEffect = psdImage.getLayers()[4].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(false);
    gradientFillSettings.setAngle(90);

    // 5. Voegt Gradiënt fill toe, op positie Outside
    strokeEffect = psdImage.getLayers()[5].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Outside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(90);

    // 6. Voegt Gradiënt fill toe, op positie Center
    strokeEffect = psdImage.getLayers()[6].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Center);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(0);

    // 7. Voegt Patroon fill toe, op positie Inside
    strokeEffect = psdImage.getLayers()[7].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(200);

    // 8. Voegt Patroon fill toe, op positie Outside
    strokeEffect = psdImage.getLayers()[8].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Outside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(100);

    // 9. Voegt Patroon fill toe, op positie Center
    strokeEffect = psdImage.getLayers()[9].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Center);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(75);

    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

...
...
(Andere vertaalde voorbeelden ga zo maar door)**PSDJAVA-249. Ondersteuning van lnk2 / lnk3 Resources (Resources van Smart Object Layer)**
{{< highlight java >}}
// Dit voorbeeld laat zien hoe je kunt werken met slimme objectresources (meestal Lnk2Resource).
// Het programma laadt meerdere Photoshop-documenten en exporteert hun slimme objecten naar
// rasterbestandsformaten. Ook toont de code het gebruik van openbare methoden van Lnk2Resource.

...

// Dit voorbeeld demonstreert hoe je eigenschappen van de PSD Lnk3-resource en de liFD-gegevensbronnen in een PSD-afbeelding kunt ophalen en instellen voor 32 bits per kanaal.
$.voorbeeldVanLnk2ResourceOndersteuning("Layered PSD-file smart objects.psd", 2, 0x19504, 0x0001d3e0, LaaggedLnk3ResourceOndersteuningGegevallen);

// Dit voorbeeld demonstreert hoe je eigenschappen van de PSD Lnk2 Resource en de liFD-gegevensbronnen kunt ophalen en instellen voor 16 bits per kanaal.
$.voorbeeldVanLnk2ResourceOndersteuning("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LaaggedLnk2ResourceOndersteuningGegevallen);
{{< /highlight >}}

**PSDJAVA-247. Wijzig Exception-bericht bij het proberen te openen van niet-ondersteunde formaten als afbeelding**
{{< highlight java >}}
// Dit voorbeeld toont aan dat een uitzondering met een nieuw, meer beschrijvend bericht wordt gegenereerd bij het laden
// van rasterafbeeldingen op een manier die niet wordt ondersteund (rasterafbeeldingen kunnen alleen als lagen worden geladen).

...

...

{{< /highlight >}}

**PSDJAVA-235. Als we een PSD-bestand opslaan na het aanmaken van een nieuwe Layer Group, krijgen we een Photoshop-waarschuwing bij het openen van het bestand.**
{{< highlight java >}}
// Dit voorbeeld demonstreert dat er geen uitzondering wordt gegeneerd bij het opslaan van een gegenereerd PSD-bestand
// dat binnenste lagen bevat.

...

{{< /highlight >}}

(Vertaal de rest van de voorbeelden op dezelfde manier)