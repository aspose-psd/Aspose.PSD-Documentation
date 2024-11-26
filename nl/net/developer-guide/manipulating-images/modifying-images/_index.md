---
title: Afbeeldingen aanpassen
type: docs
weight: 50
url: /nl/net/modifying-images/
---

## **Dithering voor rasterafbeeldingen**
Dithering is een techniek om de illusie van nieuwe kleuren en tinten te creëren door het patroon van punten te variëren dat daadwerkelijk een afbeelding creëert. Het is de meest voorkomende manier om het kleurenbereik van afbeeldingen te verkleinen tot 256 (of minder) kleuren. Aspose.PSD biedt ondersteuning voor dithering voor de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) klasse door de Dither-methode te introduceren die twee parameters accepteert. De eerste is van het type DitheringMethod om toe te passen met twee mogelijke opties: FloydSteinbergDithering en ThresholdDithering. De tweede parameter voor de [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) methode is de BitCount als geheel getal. BitCount definieert de steekproefgrootte voor het ditheringresultaat. De standaardwaarde is 1 die zwart en wit vertegenwoordigt, terwijl toegestane waarden 1, 4, 8 zijn die respectievelijk paletten met 2, 4 en 256 kleuren genereren.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}
## **Helderheid, contrast en gamma aanpassen**
Kleurafstellingen in digitale afbeeldingen zijn een van de kernfuncties die de meeste beeldverwerkingsbibliotheken bieden. Kleurafstellingen kunnen worden gecategoriseerd in het volgende.

1. Helderheid verwijst naar de lichtheid of duisternis van een kleur. Door de helderheid van een afbeelding te verhogen, worden alle kleuren lichter, terwijl het verlagen van de helderheid alle kleuren donkerder maakt.
1. Contrast verwijst naar het duidelijker maken van de objecten of details binnen een afbeelding. Door het contrast van een afbeelding te vergroten, neemt het verschil tussen lichte en donkere gebieden toe, zodat de lichte gebieden lichter worden en de donkere gebieden donkerder worden. Het verlagen van het contrast zorgt ervoor dat lichtere en donkerdere gebieden ongeveer hetzelfde blijven, maar de algehele afbeelding homogener wordt.
1. Gamma optimaliseert het contrast en de helderheid van de indirecte verlichting die een object in de afbeelding verlicht.
### **Helderheid aanpassen**
Aspose.PSD voor .NET API biedt de [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) methode voor de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) klasse die kan worden gebruikt om de helderheid van de afbeelding aan te passen door een geheel getal door te geven als parameter. De hoogste parameterwaarde verwijst naar een helderdere afbeelding. Hier is de originele afbeelding en de resulterende afbeelding ter vergelijking.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **Contrast aanpassen**
De [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) methode blootgesteld door de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) klasse kan worden gebruikt om het contrast van een afbeelding aan te passen door een zwevende waarde als parameter door te geven.

De hoogste parameterwaarde geeft een hoger contrast aan in de gegeven afbeelding. Hier is de originele afbeelding en de resulterende afbeelding ter vergelijking.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}
### **Gamma aanpassen**
De [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) methode blootgesteld door de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) klasse heeft twee versies. Een van de overbelastingen accepteert één zwevende waarde en voert de gammacorrectie uit voor de rode, blauwe en groene kanaalcoëfficiënten. De andere overbelasting accepteert drie zwevende parameters die elk kleurcoëfficiënt afzonderlijk vertegenwoordigen. Het volgende codevoorbeeld toont hoe AdjustGamma op een afbeelding moet worden toegepast.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}
## **Afbeelding vervagen**
Dit artikel toont het gebruik van Aspose.PSD voor .NET om een vervageffect op een afbeelding toe te passen. Aspose.PSD-API's bieden efficiënte en eenvoudig te gebruiken methoden om dit doel te bereiken. Aspose.PSD voor .NET heeft de [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) klasse blootgelegd om op de vlieg een vervageffect te creëren. [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) klasse heeft straal- en sigma-waarden nodig om een vervagingseffect op een afbeelding te creëren. De stappen om een wijziging op te slaan zijn net zo eenvoudig als hieronder:

1. Laad een afbeelding met behulp van de fabrieksmethode Load die blootgesteld wordt door de Image-klasse.
1. Converteer de afbeelding naar [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Maak een instantie van de [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) klasse met de standaardconstructor of verstrek straal- en sigma-waarden in de constructor.
1. Roep de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter-methode aan en specificeer rechthoek als afmetingen van de afbeelding en een instantie van [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) klasse.
1. Sla de resultaten op.

Het volgende codevoorbeeld toont hoe een vervageffect op een afbeelding kan worden gecreëerd.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}
## **Transparantie van afbeeldingen verifiëren**
Dit artikel toont het gebruik van Aspose.PSD voor .NET om afbeeldingstransparantie te controleren. De stappen om de transparantie van afbeeldingen te controleren zijn zo eenvoudig als hieronder:

1. Laad een afbeelding met behulp van de fabrieksmethode [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) blootgesteld door de [Image](https://reference.aspose.com/psd/net/aspose.psd/image) klasse.
1. Controleer de afbeeldingsdekking: als de dekking nul is, is de afbeelding transparant.
1. Het volgende codevoorbeeld toont hoe gecontroleerd kan worden of de afbeelding transparant is of niet.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}
## **Implementeer een verliesgevende GIF-compressor**
Met behulp van Aspose.PSD voor .NET kunnen ontwikkelaars een verschil in pixels instellen. De compressie van GIF is gebaseerd op een "woordenboek" van reeksen pixels die gezien zijn. Een normale encoder zoekt in het woordenboek naar de langste reeks pixels die exact overeenkomen met pixels in de afbeelding. Een verliesgevende encoder kiest de langste reeks pixels die "voldoende vergelijkbaar" zijn met pixels in de afbeelding. Hieronder staat de code-demonstratie van de genoemde functionaliteit.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}
## **Implementeer Bicubic Resampling**
Resamplen betekent dat je de pixeldimensies van een afbeelding wijzigt. Wanneer je afschaalt, elimineer je pixels en verlies je dus informatie en detail van je afbeelding. Wanneer je opschaalt, voeg je pixels toe. Photoshop voegt deze pixels toe door interpolatie te gebruiken. Dit artikel toont hoe je Bicubic Resampling kunt uitvoeren met behulp van Aspose.PSD voor .NET.

Hieronder staat de code-demonstratie van de genoemde functionaliteit.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}
## **Kleurbalans aanpassingslaag**
Dit artikel toont het gebruik van Aspose.PSD voor .NET om de **kleurbalans aanpassingslaag** op een afbeelding uit te voeren. De kleurbalans aanpassingslaag geeft u de mogelijkheid om aanpassingen te maken aan de kleuren van uw afbeeldingen. Het toont de drie kleurkanalen en hun complementaire kleuren, en u kunt het evenwicht van deze paren aanpassen om het uiterlijk van een foto te veranderen.

Hieronder staat de code-demonstratie van de genoemde functionaliteit.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}
## **Inverteer aanpassingslaag**
Dit artikel toont hoe u de **inverteer aanpassingslaag** kunt uitvoeren met behulp van Aspose.PSD voor .NET. Een aanpassingslaag is een speciaal soort laag die voornamelijk wordt gebruikt voor kleurcorrectie. In plaats van hun eigen inhoud te hebben, passen ze de informatie aan op de lagen eronder. De inverteer aanpassingslaag maakt een negatief effect op de foto door de kleuren van een afbeelding om te keren.

Hieronder staat de code-demonstratie van de genoemde functionaliteit.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}
