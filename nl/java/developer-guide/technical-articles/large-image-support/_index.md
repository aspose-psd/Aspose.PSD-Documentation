---
title: Ondersteuning voor Grote Afbeeldingen
type: docs
weight: 60
url: /nl/java/large-image-support/
---

## **Ondersteuning voor Grote Afbeeldingen**
Aangezien de standaard Java-bibliotheek beperkingen heeft wat betreft de afmetingen van afbeeldingen die het kan verwerken, hebben we een nieuwe mechanisme geïntroduceerd voor de ondersteuning van grote afbeeldingen. De nieuwe aanpak overwint de beperkingen, maar vanwege gegevensgroottebeperkingen zijn de maximale ondersteunde afmetingen voor het maken en laden 2.147.483.647 x 2.147.483.647 pixels.
### **Werken met Grote Afbeeldingen**
Aspose.PSD heeft verbeterde prestaties en ondersteuning voor grote afbeeldingen. Afbeeldingen van honderden megabytes zijn geen probleem meer, zodat je afbeeldingen van die grootte kunt maken, laden en erover kunt tekenen. Vanwege de gedeeltelijke verwerking en behandeling van OutOfMemoryException uitzonderingen, kan de prestatie echter zeer laag zijn bij zeer grote afbeeldingen. Dit komt doordat Aspose.PSD probeert een kleinere hoeveelheid gegevens opnieuw toe te wijzen voor verwerking en elke reallocatiestap zeer kostbaar is. De voordelen van de nieuwe architectuur zijn duidelijk:

- Er is geen beperking qua afmetingen van de afbeelding.
- Je bent niet beperkt tot het beschikbare geheugen op je pc.

Als je langzame verwerking ervaart, is het raadzaam om de totale hoeveelheid RAM te verhogen om al je pixels in het geheugen te passen. Als je dit niet doet, is verwerking nog steeds mogelijk maar trager. De aanpak is als volgt:

- Roep de LoadPartialPixels-methode aan met de gewenste rechthoek en een delegate om de geladen pixels op te halen.

Aspose.PSD probeert de hele rechthoek te laden.

- Als er genoeg geheugen is om alle pixels op te slaan, worden alle pixels eenvoudigweg aan de beller geretourneerd.
- Als er niet genoeg geheugen is, ontvangt de beller een subset van pixels van binnen de gespecificeerde rechthoek. Wanneer deze pixels zijn verwerkt, ontvangt de beller de volgende rechthoek. Verwerking eindigt wanneer de hele rechthoek is verwerkt.

Aspose.PSD probeert zoveel mogelijk regels te extraheren. Als er niet genoeg geheugen is om een enkele lijn met pixels op te slaan, wordt een enkele regel opgesplitst in delen die overeenkomen met de rechthoeken met een hoogte van 1. Je kunt ook tekenen op grote afbeeldingen. Tijdens het tekenproces probeert Aspose.PSD de hele gewenste rechthoek te beïnvloeden. Als er niet genoeg geheugen is, wordt er getekend op gedeeltelijke rechthoeken totdat het hele gebied is getekend. Daarnaast ondersteunt Aspose.PSD het opslaan en exporteren van grote afbeeldingen. Sla de bronafbeelding op schijf op of exporteer deze naar een ander bestandsformaat. Het opslaan of exporteren gebeurt door partiële rechthoeken te gebruiken indien nodig.
### **Ondersteunde Afbeeldingsindelingen**
De volgende indelingen worden ondersteund voor de verwerking van grote afbeeldingen:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

De bovenstaande indelingen kunnen veilig worden verwerkt door creatie, wijziging, toepassing van tekenoperaties, opslaan op schijf of exporteren ongeacht de afmetingen van de afbeelding.
