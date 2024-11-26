---
title: Bewerken van Photoshop-formaten
type: docs
weight: 10
url: /nl/java/manipuleren-van-photoshop-formaten/
---

## **Kleurvervanging in PSD-lagen**
Aspose.PSD voor Java maakt het mogelijk om de achtergrondkleur van elke laag van een PSD-bestand te wijzigen. Gebruik de Aspose.PSD.FileFormats.Psd.Layers.BackgroundColor-klasse om de achtergrondkleur van de laag in de PSD-laag te wijzigen. Het volgende codefragment laadt een PSD-bestand, krijgt toegang tot de laag, werkt de achtergrondkleur bij en slaat het PSD-bestand op.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.java" >}}
## **Tekstlaag bijwerken in PSD-bestand**
Aspose.PSD voor Java maakt het mogelijk om de tekst in de tekstlaag van een PSD-bestand te manipuleren. Gebruik de Aspose.PSD.FileFormats.Psd.Layers.TextLayer-klasse om tekst in de PSD-laag bij te werken. Het volgende codefragment laadt een PSD-bestand, krijgt toegang tot de tekstlaag, werkt de tekst bij en slaat het PSD-bestand op met een nieuwe naam met behulp van de Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText-methode.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.java" >}}
## **Detecteren van afgevlakte PSD**
Aspose.PSD voor Java maakt het mogelijk om te detecteren of een gegeven PSD-bestand is afgevlakt of niet. De eigenschap IsFlatten is geïntroduceerd in de Aspose.PSD.FileFormats.Psd.PsdImage-klasse om deze functionaliteit te bereiken. Het volgende codefragment laadt een PSD-bestand en krijgt toegang tot de eigenschap IsFlatten.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.java" >}}
## **PSD-lagen samenvoegen**
Dit artikel laat zien hoe lagen kunnen worden samengevoegd in een PSD-bestand tijdens het converteren van een PSD-bestand naar JPG met Aspose.PSD. In het onderstaande voorbeeld wordt een bestaand PSD-bestand geladen door het bestandspad door te geven aan de statische Load-methode van de Image-klasse. Zodra het is geladen, converteer/cast de afbeelding naar PsdImage. Maak een exemplaar van de JpegOptions-klasse aan en stel verschillende eigenschappen ervan in. Roep nu de Save-methode van de PsdImage-instantie aan. Het volgende codefragment laat zien hoe PSD-lagen kunnen worden samengevoegd.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-ModifyingAndConvertingImages-PSD-MergePSDLayers-MergePSDLayers.java" >}}
## **Grijswaardeondersteuning met Alpha voor PSD**
Dit artikel laat zien hoe grijswaarde met alpha kan worden ondersteund voor een PSD-bestand tijdens het converteren van een PSD-bestand naar PNG met Aspose.PSD. In het onderstaande voorbeeld wordt een bestaand PSD-bestand geladen door het bestandspad door te geven aan de statische Load-methode van de Image-klasse. Zodra het is geladen, converteer/cast de afbeelding naar PsdImage. Maak een exemplaar van de PngOptions-klasse aan en stel verschillende eigenschappen ervan in. Stel de ColorType-eigenschap in op TruecolorWithAlpha. Roep nu de Save-methode van de PngOptions-instantie aan. Het volgende codefragment laat zien hoe kan worden omgezet naar Grijswaarde PNG met Alpha.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.java" >}}
## **Ondersteuning van laageffecten voor PSD**
Dit artikel laat zien hoe verschillende effecten zoals **Vervagen**, **Binnenste Gloed**, **Buitenste Gloed** kunnen worden ondersteund voor PSD-laag. Het volgende codefragment laat zien hoe laageffecten kunnen worden ondersteund.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.java" >}}