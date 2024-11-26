---
title: Ondersteuning voor grote afbeeldingen
type: docs
weight: 40
url: /nl/net/ondersteuning-voor-grote-afbeeldingen/
---

## **Ondersteuning voor grote afbeeldingen**
Aangezien de standaard .NET-bibliotheek beperkingen heeft met betrekking tot de grootte van afbeeldingen die het kan verwerken, hebben we een nieuw mechanisme geïntroduceerd voor de ondersteuning van grote afbeeldingen. De nieuwe benadering overwint de beperkingen, maar vanwege gegevenslimieten zijn de maximale ondersteunde afmetingen voor creatie en laden 2.147.483.647 x 2.147.483.647 pixels.
### **Werken met grote afbeeldingen**
Aspose.PSD heeft verbeterde prestaties en ondersteuning voor grote afbeeldingen. Afbeeldingen van honderden megabytes groot vormen geen probleem meer, dus je kunt ze maken, laden en erover tekenen. Echter, vanwege de gedeeltelijke verwerking en het omgaan met OutOfMemoryException uitzonderingen, kan de prestatie zeer laag zijn bij zeer grote afbeeldingen. Dit komt doordat Aspose.PSD probeert een kleiner bedrag aan gegevens opnieuw toe te wijzen voor verwerking en elke herallocatiestap erg kostbaar is. De voordelen van de nieuwe architectuur zijn duidelijk:

- Er is geen beperking voor de afmeting van de afbeelding.
- Je bent niet beperkt tot het beschikbare geheugen op je pc.

Als je langzame verwerking ervaart, wordt aangeraden om de totale hoeveelheid RAM te verhogen om al je pixels in het geheugen te passen. Als je dit niet doet, is verwerking nog steeds mogelijk maar langzamer. De benadering is als volgt:

- Roep de [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) methode aan met het gewenste rechthoek en delegeer om de gespecificeerde geladen pixels te ontvangen.

Aspose.PSD probeert het hele rechthoek te laden.

- Als er genoeg geheugen is om alle pixels in te passen, worden alle pixels eenvoudigweg teruggegeven aan de beller.
- Als er niet genoeg geheugen is, ontvangt de beller een subset van pixels van binnen de gespecificeerde rechthoek. Wanneer die pixels zijn verwerkt, ontvangt de beller de volgende rechthoek. De verwerking eindigt wanneer de gehele rechthoek is verwerkt.

Aspose.PSD probeert zoveel mogelijk lijnen te extraheren. Als er niet genoeg geheugen is om een enkele lijn van pixels in te passen, wordt een enkele lijn opgesplitst in delen die overeenkomen met de rechthoeken met een hoogte van 1. Je kunt ook tekenen op grote afbeeldingen. Het tekenproces probeert het hele gewenste rechthoek te beïnvloeden. Als er niet genoeg geheugen is, wordt er getekend op gedeeltelijke rechthoeken totdat het hele gebied is getekend. Bovendien ondersteunt Aspose.PSD het opslaan en exporteren van grote afbeeldingen. Sla de bronafbeelding op de schijf op of exporteer deze naar een ander bestandsformaat. Het opslaan of exporteren wordt uitgevoerd door het gebruik van gedeeltelijke rechthoeken indien nodig.
### **Ondersteunde afbeeldingsindelingen**
De volgende formaten worden ondersteund voor de verwerking van grote afbeeldingen:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

De bovenstaande formaten kunnen veilig worden verwerkt door middel van creatie, wijziging, toepassing van tekenbewerkingen, opslaan op de schijf of exporteren ongeacht de grootte van de afbeelding.
