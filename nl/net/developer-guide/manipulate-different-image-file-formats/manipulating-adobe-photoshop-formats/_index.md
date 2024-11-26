---
title: Bewerking van Adobe Photoshop-indelingen
type: docs
weight: 20
url: /nl/beheren-adobe-photoshop-indelingen/
---

## **Samenvoegen van PSD-lagen in Andere lagen**

## **Afbeelding exporteren naar PSD**
PSD, PhotoShop-document, is het standaard bestandsformaat dat wordt gebruikt door Adobe Photoshop voor het werken met afbeeldingen. Aspose.PSD stelt u in staat om bestanden te laden, bewerken en opslaan naar PSD, zodat ze kunnen worden geopend en bewerkt in Photoshop. Dit artikel laat zien hoe u een bestand kunt opslaan naar PSD met Aspose.PSD, en het bespreekt ook enkele van de instellingen die kunnen worden gebruikt bij het opslaan naar dit formaat. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) is een gespecialiseerde klasse in de [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace die wordt gebruikt om afbeeldingen naar PSD te exporteren. Om naar PSD te exporteren, maakt u een instantie van de Image-klasse, geladen vanuit een bestaand afbeeldingsbestand (bijvoorbeeld miniaturen) of maakt u een nieuwe vanaf het begin. Dit artikel legt uit hoe. In de onderstaande voorbeelden wordt een afbeelding vanaf het begin gemaakt. Nadat het is gemaakt en de pixelgegevens zijn ingevuld, slaat u de afbeelding op met behulp van de Save-methode van de Image-klasse en geeft u een PsdOptions-object op als het tweede argument. Voor geavanceerde conversie kunnen verschillende eigenschappen van de PsdOptions-klasse worden ingesteld. Enkele eigenschappen zijn ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) en Versie. Aspose.PSD ondersteunt de volgende compressiemethoden via de Compressio... 

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-AfbeeldingenWijzigenConverteren-PSD-AfbeeldingExporterenNaarPSD-AfbeeldingExporterenNaarPSD.cs" >}}
## **Afbeelding importeren naar PSD-laag**
Dit artikel toont het gebruik van Aspose.PSD om een afbeelding toe te voegen of te importeren naar een PSD-laag. Aspose.PSD-API's hebben efficiŽnte en eenvoudig te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD heeft de [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage)-methode van de Layer-klasse blootgelegd om een afbeelding toe te voegen/importeren in een PSD-bestand. De DrawImage-methode heeft locatie- en afbeeldingswaarden nodig om een afbeelding toe te voegen/importeren in een PSD-bestand. De stappen om een afbeelding in te voeren in een PSD-laag zijn zo eenvoudig als hieronder:

- Laad een PSD-bestand als een afbeelding met behulp van de fabrieksmethode Load blootgesteld door de Image-klasse.
- Maak een instantie van de Layer-klasse vanuit de stream met Png, Jpeg, Tiff, Gif, Bmp, Psd of j2k-bestand
- Voeg de Laag toe aan de Psd met behulp van de AddLayer-methode
- Sla de resultaten op.


De volgende codefragment toont u hoe u de afbeelding naar de PSD-laag importeert.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Openen-LadenAfbeeldingVanStream-LadenAfbeeldingVanStream.cs" >}}
## **Kleurvervanging in PSD-lagen**
D...