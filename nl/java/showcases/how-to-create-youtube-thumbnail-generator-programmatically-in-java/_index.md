---
title: Hoe maak je een YouTube-thumbnailgenerator programmeercursus in Java
type: docs
weight: 10
url: /nl/java/hoe-je-youtube-thumbnail-generator-programmeert-in-java/
---

## **Inleiding**
Het doel van dit document is om API-gebruik te demonstreren van enkele samengestelde tools van [Aspose.PSD voor Java](https://products.aspose.com/psd/java) aan de hand van een realistisch voorbeeld. In dit artikel zal **een eenvoudig Java-programma dat YouTube-thumbnails genereert** voor het [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q)-kanaal worden geschreven en uitgelegd. Dit kanaal is gekozen uit de echte wereld omdat de thumbnails vrij standaard zijn en ze het gebruik van een paar populaire samengestelde gereedschappen van Aspose.PSD voor Java illustreren (bijv. drop [schaduweffect](/psd/nl/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), radiale gradiëntvulling, tekst en vormen tekenen):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Hoe het in een notendop werkt**
Een eenvoudig Java-programma neemt als invoer twee argumenten: een onderschrift en een afbeelding. Er wordt **een in-memory Photoshop-document (PSD) gegenereerd** uit die invoer met behulp van Aspose.PSD voor Java. Vervolgens **zet het programma het document om van PSD naar PNG**-bestandsindeling om een YouTube-thumbnail te verkrijgen met een grootte van 1280x720 pixels. De uitvoerafbeelding ziet eruit als volgt:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Technische vereisten**
De volgende technologieën zijn nodig om te slagen bij het uitvoeren van de code in dit artikel:

- Java 6+
- [Aspose.PSD voor Java](/psd/nl/java/installation/) (laatste versie)

## **Aan de slag**
Zoals al eerder vermeld, gebruikt het programma in-memory PSD om een thumbnail te genereren. Laten we dus **een PSD-document maken** om mee te beginnen:

PsdImage psdImage = new PsdImage(1280, 720);

Als je nauwkeuriger naar de YouTube-thumbnail hierboven kijkt, zul je merken dat **het bestaat uit verschillende componenten**:

1. een achtergrondafbeelding (geprinte masker)
1. een radiaal psd-gradiënt (belicht het gebied in de rechterbovenhoek)
1. een logotype met een schaduweffect
1. een onderschrift en een eenvoudige tekening (blauw rechthoek)

Laten we dieper ingaan om te zien hoe elk van deze componenten geïmplementeerd kan worden met behulp van Aspose.PSD voor Java in de volgende secties.

## **1. Voeg een achtergrondafbeelding toe**
De volgorde van lagen is belangrijk. Daarom moet eerst een achtergrondafbeelding worden toegevoegd om andere lagen niet te overlappen. Let op dat momenteel alleen worden [rasterbestandsindelingen ondersteund](/psd/nl/java/supported-file-formats/).

### **1.1. Voeg een achtergrondafbeelding toe aan een Photoshop-laag**
Om **een rasterafbeelding aan PSD toe te voegen**, moet een invoerstroom worden doorgegeven als argument tijdens de constructie van de laag (zie meer [voorbeelden van het laden van rasterafbeeldingen](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```

### **1.2. Pas de achtergrondafbeelding aan aan het canvas**
De volgende 2 acties (formaat wijzigen, positioneren) zijn handig voor die gevallen waarin **de afmeting van de afbeelding verschilt van de canvasgrootte**, hoewel de afbeelding in dit artikel dezelfde grootte heeft als de canvas (ga ervan uit dat dit niet altijd het geval zal zijn).

Zorg ervoor dat de geladen afbeelding **past bij de grootte van het canvas** (zie meer [voorbeelden van het formaat wijzigen](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

Na het wijzigen van het formaat wordt de positie van de afbeelding gewijzigd. Om de positie van de afbeelding te **resetten**, verplaats je de vergrootte afbeelding naar de linkerbovenhoek:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
```

## **2. Voeg een radiale gradiënt toe**
Er zijn **twee manieren om een radiale gradiënt toe te voegen**, namelijk:

- een [verloopoverlay-effect](/psd/nl/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) op een bestaande laag (een verloopeffect dat aan de huidige laag is gekoppeld en op de inhoud ervan wordt toegepast)
- een nieuwe [verloopvullaag](/psd/nl/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (een aparte laag met zelfstandige configuratie van de gradiënt)

Het is voldoende om het verloopoverlay-effect voor dit voorbeeld te gebruiken. Echter, om dit artikel interessanter en nuttiger te maken, **wordt de verloopvullaag gebruikt** aangezien alle laageffecten op een vergelijkbare manier worden toegepast en in de volgende sectie nog een ander laageffect wordt gebruikt.

### **2.1. Voeg een radiale gradiëntvullaag toe**
Het proces om een nieuwe verloopvullaag toe te voegen bestaat uit de volgende 2 stappen:

1. Het is noodzakelijk om **verloopvulinstellingen te declareren** omdat er geen vooraf gedefinieerde instellingen zijn. De minimaal vereiste configuratie ziet er als volgt uit (betekent dat het gradiënttype, de schaal, de kleur en de transparantiepunten vereiste eigenschappen zijn):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

De configuratie hierboven declareert een radiale gradiënt die transparant is aan de randen en donkerblauw in het midden. De gradiëntpositie bevindt zich standaard in het midden van de canvas.

Om het verloop te keren en iets naar de rechterbovenhoek te verplaatsen, gebruik je de bijbehorende optionele eigenschappen:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```

2. Wanneer de configuratie is voltooid, voeg je een verloopvullaag samen met zijn instellingen toe aan PSD:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
```

## **Voeg een logotype met een schaduw toe**
Het **schaduweffect** is een effect dat het mogelijk maakt om een aangepaste schaduw langs de contour van het object (afbeelding, tekst etc.) toe te voegen.

### **3.1. Voeg een logotype toe aan een Photoshop-laag**
Dezelfde aanpak als in sectie 1.1. kan worden gebruikt om **een logotype aan PSD toe te voegen**:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
```

### **3.2. Positioneer het logotype**
De geladen afbeelding is standaard nauw verbonden met de linkerbovenhoek. Er moeten echter enkele **marges worden toegevoegd** om eruit te zien als de originele YouTube-thumbnail op het kanaal. Daarom moet de positie van de afbeelding worden verplaatst van de randen van de laag:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
```

### **3.3. Voeg een schaduweffect toe aan het logotype**
Het logotype kan onzichtbaar zijn als een lichte achtergrondafbeelding wordt gebruikt. Daarom is het wenselijk om **een schaduweffect toe te voegen** aan een logotype via de eigenschap voor mengopties (zie meer [voorbeelden van schaduwen](/psd/nl/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}
```

Het schaduweffect heeft niet de vereiste eigenschappen vanwege de standaardconfiguratie (het ziet eruit als die van Photoshop). Echter, de bovenstaande schaduw is aangepast om eruit te zien als een doorschijnende rand vervaagd aan de randen.

## **4. Voeg een tekening van tekst en een vorm toe**
### **3.1. Maak een grafische laag**
Tekenen wordt niet rechtstreeks ondersteund door een reguliere laag. Daarom wordt de grafische engine naast de laag gebruikt om een API voor het tekenen te bieden (zie meer [voorbeelden van tekenen](/psd/nl/java/drawing-images-using-graphics/)):

```java
Layer grafischeLaag = psdImage.addRegularLayer();
Graphics graphics = **nieuwe** Graphics(grafischeLaag);
```

### **3.2. Tekend meerregelige tekst**
Een oplettende lezer zou kunnen vragen: waarom geen tekstlaag gebruiken om tekst toe te voegen? Nou, er zijn een paar redenen: tekstbewerking is in dit geval niet nodig omdat de PSD elke keer van nul af aan wordt gegenereerd; de aanpassing van het lettertype wordt nog niet ondersteund door de [tekst-API](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) (v20.6 op het moment van schrijven).

Het is gemakkelijk om **wat tekst te tekenen met een aangepast lettertype** door gewoon een gewenst lettertype te instantiëren en de overeenkomstige methode van de grafische engine aan te roepen. Echter, om een rechthoek te maken (zie details in de volgende sectie) die automatisch de hoogte verandert op basis van het aantal regels tekst is iets moeilijker. De exacte hoogte van alle regels moet eerst worden berekend:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}
```

Waarbij 1,15 de regelhoogte is en 3 de tekstvulling.

### **3.3. Tekenen van een rechthoek**
Een rechthoek is ook eenvoudig te tekenen, zelfs met een gradiëntkwast (stel gewoon een gebied in om te tekenen en een kleurbereik). Wanneer de hoogte van de tekst bekend is, worden de grootte en de positie van de rechthoek berekend. Om **een gevulde rechthoek te tekenen** **in psd** (niet slechts een frame), bel je de corresponderende methode van de grafische engine met dit alles:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}
```

Waar 40, 15, 25 inspringingen zijn.

## **Resultaat**
Dus, het vormgeven van de thumbnail is voltooid. Het is daarom tijd om **de thumbnail naar een rasterbestandsindeling te exporteren** (bijvoorbeeld PNG) voor verdere distributie:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}
```

## **Conclusie**
In dit artikel hebben we een YouTube-thumbnailgenerator voor het DW Documentary-kanaal gemaakt en uitgelegd hoe je enkele van de meest populaire samengestelde tools zoals het schaduweffect, de radiale gradiëntvulling, tekst en vormen kunt gebruiken.

## **Volledig voorbeeld**
Je kunt de [Aspose.PSD SDK downloaden](https://products.aspose.com/psd/net)

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
```