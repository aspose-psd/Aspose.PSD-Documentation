---
title: Het maken, openen en opslaan van PSD-bestanden
type: docs
weight: 10
url: /nl/het-maken-openenen-opslaan-van-psd-bestanden/
---

## **Afbeelding exporteren naar PSD**
PSD, Photoshop-document, is het standaard bestandsformaat dat wordt gebruikt door Adobe Photoshop voor het werken met afbeeldingen. Aspose.PSD stelt u in staat om bestanden te laden, bewerken en opslaan naar PSD, zodat ze kunnen worden geopend en bewerkt in Photoshop. Dit artikel toont hoe u een bestand naar PSD kunt opslaan met behulp van Aspose.PSD, en bespreekt ook enkele van de instellingen die kunnen worden gebruikt bij het opslaan in dit formaat. PsdOptions is een gespecialiseerde klasse in de ImageOptions-naamruimte die wordt gebruikt om afbeeldingen naar PSD te exporteren. Om naar PSD te exporteren, maakt u een instantie van de Image-klasse, die ofwel geladen kan worden vanuit een bestaand afbeeldingsbestand (bijvoorbeeld miniaturen) of vanaf nul kan worden gecreëerd. Dit artikel legt uit hoe dit werkt. In de onderstaande voorbeelden wordt een afbeelding vanaf nul gecreëerd. Zodra deze is aangemaakt en de pixelpatronen zijn ingevuld, slaat u de afbeelding op met behulp van de Image-klasse Save-methode, en geeft u een PsdOptions-object mee als tweede argument. Verschillende eigenschappen van de PsdOptions-klasse kunnen worden ingesteld voor geavanceerde conversie. Enkele eigenschappen zijn ColorMode, CompressionMethod en Version. Aspose.PSD ondersteunt de volgende compressiemethoden via de CompressionMethod-enumeratie:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

De volgende kleurmodi worden ondersteund via de ColorModes-enumeratie:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Er kunnen aanvullende bronnen worden toegevoegd, zoals miniaturenbronnen voor PSD v4.0, v5.0 en hoger, of raster- en hulplijnenbronnen voor PSD v4.0 en hoger. De onderstaande code creëert een BMP-bestand vanaf nul, vult de pixels in en slaat het op naar PSD met RLE-compressie en grijswaarden kleurmodus. De onderstaande codesnippet toont u hoe u een afbeelding exporteert naar PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}

## **Afbeelding importeren naar PSD-laag**
Dit artikel demonstreert het gebruik van Aspose.PSD om een afbeelding toe te voegen of te importeren naar een PSD-laag. Aspose.PSD API's hebben efficiënte en eenvoudig te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD heeft de DrawImage-methode van de Layer-klasse blootgelegd om een afbeelding toe te voegen/importeren in een PSD-bestand. DrawImage-methode vereist locatie- en afbeeldingswaarden om een afbeelding toe te voegen/importen in een PSD-bestand. De stappen om een afbeeldingen te importeren naar een PSD-laag zijn als volgt:

- Laad een PSD-bestand als een afbeelding met behulp van de door de Image-klasse blootgelegde factory-methode Load.
- Creeër een instantie van de Layer-klasse en wijs de PSD-afbeeldingslaag eraan toe.
- Laad de afbeelding die moet worden toegevoegd of creeër er een vanaf nul.
- Roep de Layer.DrawImage-methode aan terwijl u locatie en afbeeldingsinstantie specificeert.
- Sla de resultaten op.



De onderstaande code toont u hoe u een afbeelding importeert naar een PSD-laag.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Thumbnail maken van PSD-bestanden**
PSD is het native documentformaat van de applicatie Adobe Photoshop. Adobe Photoshop (versie 5.0 en later) slaat voorbeeldinformatie op voor voorvertoningsweergave in een beeldbronblok dat bestaat uit een initiële kop van 28 bytes, gevolgd door een JFIF-voorbeeld in RGB (rood, groen, blauw) volgorde. Aspose.PSD API biedt een eenvoudig te gebruiken mechanisme om toegang te krijgen tot de bronnen van een PSD-bestand. Deze bronnen omvatten ook de voorbeeldbron die op zijn beurt kan worden opgehaald en opgeslagen op de schijf volgens de behoeften van de applicatie. De onderstaande code toont u hoe u miniaturen kunt maken van PSD-bestanden.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Indexed PSD-bestanden maken**
Aspose.PSD voor Java API kan Indexed PSD-bestanden vanaf nul maken. Dit artikel demonstreert het gebruik van de PsdOptions- en PsdImage-klassen om een Indexed PSD te maken terwijl er enkele vormen over het nieuw gecreëerde canvas worden getekend. De volgende eenvoudige stappen zijn vereist om een Indexed PSD-bestand te maken.

- Creeër een instantie van PsdOptions en stel de bron in.
- Stel de ColorMode-eigenschap van de PsdOptions in op ColorModes.Indexed.
- Creeër een nieuwe palet van kleuren vanuit RGB-ruimte en stel deze in als Eigenschap van Palet van PsdOptions.
- Stel CompressionMethod-eigenschap in op het vereiste compressiealgoritme.
- Creeër een nieuw PSD-afbeelding door de PsdImage.Create-methode aan te roepen.
- Tekenen van grafische afbeeldingen of het uitvoeren van andere bewerkingen zoals vereist.
- Roep de PsdImage.Save-methode aan om alle wijzigingen vast te leggen.



De onderstaande code toont u hoe u indexed PSD-bestanden kunt maken.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **PSD-laag exporteren naar rasterafbeelding**
Aspose.PSD voor Java stelt u in staat om lagen in een PSD-bestand naar rasterafbeeldingen te exporteren. Gebruik alstublieft de Aspose.PSD.FileFormats.Psd.Layers.Layer.Save-methode om de laag naar afbeelding te exporteren. De volgende voorbeeldcode laadt een PSD-bestand en exporteert elke laag ervan naar een PNG-afbeelding met behulp van Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Nadat alle lagen zijn geëxporteerd naar PNG-afbeeldingen, kunt u ze openen met uw favoriete afbeeldingsviewer. De onderstaande code toont u hoe u een PSD-laag naar een rasterafbeelding exporteert.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}
