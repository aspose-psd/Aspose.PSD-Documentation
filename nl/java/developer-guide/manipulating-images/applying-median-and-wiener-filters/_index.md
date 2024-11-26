---
title: Het toepassen van Median- en Wienerfilters
type: docs
weight: 10
url: /nl/java/het-toepassen-van-median-en-wienerfilters/
---

## **Het toepassen van Median- en Wienerfilters**
Het median-filter is een niet-lineaire digitale filtertechniek die vaak wordt gebruikt om ruis te verwijderen. Een dergelijke ruisreductie is een typische voorbewerking om de resultaten van latere verwerking te verbeteren. Het Wiener-filter is de MSE (mean squared error) optimale stationaire lineaire filter voor beelden die zijn aangetast door additieve ruis en vervaging. Met Aspose.PSD voor Java API kunnen ontwikkelaars median-filter toepassen om ruis uit de afbeelding te verwijderen en de Gauss Wiener-filter op afbeeldingen toe te passen. In dit artikel wordt gedemonstreerd hoe het median-filter en Gauss Wiener-filter kunnen worden toegepast op afbeeldingen.
### **Het toepassen van het Median-filter**
Aspose.PSD biedt de klasse MedianFilterOptions om een filter toe te passen op een RasterImage. Het onderstaande codefragment toont hoe het median-filter kan worden toegepast op een rasterafbeelding.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Het toepassen van de Gauss Wiener-filter**
Aspose.PSD biedt de klasse GaussWienerFilterOptions om een filter toe te passen op een RasterImage. Het onderstaande codefragment toont hoe de Gauss Wiener-filter kan worden toegepast op een rasterafbeelding.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Het toepassen van de Gauss Wiener-filter op een gekleurde afbeelding**
Aspose.PSD biedt ook GaussWienerFilterOptions voor gekleurde afbeeldingen. Het onderstaande codefragment toont hoe de Gauss Wiener-filter kan worden toegepast op een kleurenafbeelding.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Het toepassen van de Motion Wiener-filter**
Aspose.PSD biedt de klasse MotionWienerFilterOptions om een filter toe te passen op een RasterImage. Het onderstaande codefragment toont hoe de motion Wiener-filter kan worden toegepast op een rasterafbeelding.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Het toepassen van een correctiefilter op een afbeelding**
Dit artikel demonstreert het gebruik van Aspose.PSD voor Java om correctiefilters op een afbeelding toe te passen. Aspose.PSD API's hebben efficiënte en gemakkelijk te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD voor Java heeft de klassen BilateralSmoothingFilterOptions en SharpenFilterOptions blootgelegd voor filtratie. De BilateralSmoothingFilterOptions-klasse heeft een geheel getal als grootte nodig. De stappen om de grootte te wijzigen zijn als volgt:


1. Laad een afbeelding met behulp van de fabrieksmethode Load blootgelegd door de Image-klasse.
1. Converteer de afbeelding naar RasterImage.
1. Maak exemplaren van de BilateralSmoothingFilterOptions- en SharpenFilterOptions-klassen.
1. Roep de RasterImage.Filter-methode aan terwijl u het rechthoek als afbeeldingsgrenzen en een instantie van de BilateralSmoothingFilterOptions-klasse opgeeft.
1. Roep de RasterImage.Filter-methode aan terwijl u het rechthoek als afbeeldingsgrenzen en een instantie van de SharpenFilterOptions-klasse opgeeft.
1. Pas het contrast aan.
1. Stel de helderheid in.
1. Sla de resultaten op.

Het onderstaande codefragment toont je hoe je een correctiefilter kunt toepassen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Gebruik van Bradley-threshold algoritme**
Beeldthresholding wordt gebruikt in grafische toepassingen. Het doel van het toepassen van een drempelwaarde op een afbeelding is om pixels te classificeren als "donker" of "licht". Aspose.PSD API staat je toe om gebruik te maken van Bradley-thresholding bij het converteren van afbeeldingen. Het volgende codefragment toont je hoe je de drempelwaarde kunt definiëren en vervolgens het algoritme van de Bradley-threshold kunt oproepen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
