---
title: Afbeeldingen aanpassen
type: docs
weight: 50
url: /nl/java/afbeeldingen-aanpassen/
---

## **Dithering voor Rasterafbeeldingen**
Dithering is een techniek om de illusie van nieuwe kleuren en tinten te creëren door het patroon van punten te variëren dat daadwerkelijk een afbeelding creëert. Het is de meest voorkomende manier om het kleurenbereik van afbeeldingen te verlagen tot 256 (of minder) kleuren. Aspose.PSD biedt ondersteuning voor dithering voor de Rasterafbeeldingsklasse door de Dither-methode te introduceren die twee parameters accepteert. De eerste is van het type DitheringMethod die moet worden toegepast, met twee mogelijke opties: FloydSteinbergDithering en ThresholdDithering. De tweede parameter voor de Dither-methode is de BitCount als geheel getal. BitCount definieert de steekproefgrootte voor het ditheringresultaat. De standaardwaarde is 1 die zwart en wit vertegenwoordigt, terwijl toegestane waarden 1, 4, 8 zijn die respectievelijk paletten met 2, 4 en 256 kleuren genereren.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}
## **Helderheid, Contrast en Gamma aanpassen**
Kleuraanpassingen in digitale afbeeldingen zijn een van de kernfuncties die de meeste beeldverwerkingsbibliotheken bieden. Kleuraanpassingen kunnen als volgt worden gecategoriseerd.

1. Helderheid verwijst naar de lichtheid of duisternis van de kleur. Door de helderheid van een afbeelding te verhogen, worden alle kleuren lichter, terwijl het verlagen van de helderheid alle kleuren donkerder maakt.
1. Contrast heeft betrekking op het meer opvallend maken van de objecten of details binnen een afbeelding. Door het contrast van een afbeelding te verhogen, neemt het verschil tussen lichte en donkere gebieden toe, zodat de lichte gebieden lichter worden en de donkere gebieden donkerder worden. Het verlagen van het contrast zorgt ervoor dat lichtere en donkere gebieden ongeveer hetzelfde blijven, maar de algehele afbeelding homogener wordt.
1. Gamma optimaliseert het contrast en de helderheid van het indirecte licht dat een object in de afbeelding verlicht.
### **Helderheid aanpassen**
Aspose.PSD voor Java API biedt de AdjustBrightness-methode voor de Rasterafbeeldingsklasse die kan worden gebruikt om de helderheid van de afbeelding aan te passen door een geheel getalwaarde als parameter door te geven. De hoogste parameterwaarde duidt op een helderdere afbeelding. Hier is de originele afbeelding en de resulterende afbeelding ter vergelijking.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}
### **Contrast aanpassen**
De door de Rasterafbeeldingsklasse blootgestelde AdjustContrast-methode kan worden gebruikt om het contrast van een afbeelding aan te passen door een zwevende waarde te passeren.

De hoogste parameterwaarde duidt op een hoger contrast in de gegeven afbeelding. Hier is de originele afbeelding en de resulterende afbeelding ter vergelijking.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}
### **Gamma aanpassen**
De door de Rasterafbeeldingsklasse blootgestelde AdjustGamma-methode heeft twee versies. Eén van de overbelastingen accepteert één zwevende waarde en voert de gammacorrectie uit voor de rood, blauw en groen kanaalcoëfficiënten. Terwijl de andere overbelasting drie zwevende parameters accepteert die elk kleurcoëfficiënt afzonderlijk voorstellen. Het volgende codevoorbeeld toont hoe AdjustGamma op een afbeelding kan worden toegepast.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}
## **Maak een afbeelding wazig**
Dit artikel demonstreert het gebruik van Aspose.PSD voor Java om een vervagingseffect op een afbeelding uit te voeren. Aspose.PSD API's hebben efficiënte en gemakkelijk te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD voor Java heeft de GaussianBlurFilterOptions-klasse blootgesteld om een vervagingseffect on the fly te creëren. De GaussianBlurFilterOptions-klasse heeft straal- en sigma-waarden nodig om een vervagingseffect op een afbeelding te creëren. De stappen om te schalen zijn net zo eenvoudig als hieronder:

1. Laad een afbeelding met behulp van de door de Image-klasse blootgestelde fabrieksmethode Load.
1. Converteer de afbeelding naar RasterImage.
1. Maak een instantie van de GaussianBlurFilterOptions-klasse met de standaardconstructor of verstrek straal- en sigma-waarden in de constructor.
1. Roep de RasterImage.Filter-methode aan waarbij een rechthoek als afbeeldingsgrenzen en een instantie van de GaussianBlurFilterOptions-klasse worden opgegeven.
1. Sla de resultaten op.

Het volgende codevoorbeeld demonstreert hoe het vervagingseffect op een afbeelding kan worden toegepast.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}
## **Controleer de transparantie van een afbeelding**
Dit artikel demonstreert het gebruik van Aspose.PSD voor Java om de transparantie van een afbeelding te controleren. De stappen om de transparantie van een afbeelding te controleren zijn net zo eenvoudig als hieronder:

1. Laad een afbeelding met behulp van de door de Image-klasse blootgestelde fabrieksmethode Load.
1. Controleer de afbeeldingsondoorzichtigheid; als de ondoorzichtigheid nul is, is de afbeelding transparant.
1. Het volgende codevoorbeeld demonstreert hoe kan worden gecontroleerd of een afbeelding transparant is of niet.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}
## **Implementeer de verliesgevende GIF-compressor**
Met behulp van Aspose.PSD voor Java kunnen ontwikkelaars het pixelverschil instellen. De compressie van GIF is gebaseerd op een "woordenboek" van reeksen pixels die in de afbeelding worden gezien. Een normale encoder zoekt in het woordenboek naar de langste reeks pixels die precies overeenkomt met de pixels in de afbeelding. De verliesgevende encoder kiest de langste reeks pixels die "voldoende vergelijkbaar" zijn met de pixels in de afbeelding. Hieronder wordt de code-demonstratie van de genoemde functionaliteit weergegeven.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}
## **Implementeer Bicubisch Resampling**
Resamplen betekent dat je de pixeldimensies van een afbeelding verandert. Als je afmonstert, elimineer je pixels en verwijder je daarom informatie en details uit je afbeelding. Als je opmonstert, voeg je pixels toe. Photoshop voegt deze pixels toe door interpolatie te gebruiken. Dit artikel demonstreert hoe je Bicubisch Resamplen kunt uitvoeren met behulp van Aspose.PSD voor Java.

Hieronder wordt de code van de genoemde functionaliteit weergegeven.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}
## **Negatieve aanpassingslaag**
Dit artikel demonstreert hoe je de **negatieve aanpassingslaag** kunt uitvoeren met behulp van Aspose.PSD voor Java. Een aanpassingslaag is een speciaal soort laag die voornamelijk wordt gebruikt voor kleurcorrectie. In plaats van een eigen inhoud te hebben, passen ze de informatie aan op de lagen eronder. De negatieve aanpassingslaag creëert een negatief effect van een afbeelding door de kleuren om te keren.

Hieronder wordt de code van de genoemde functionaliteit weergegeven.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}
