---
title: Het toepassen van Median en Wiener Filters
type: docs
weight: 10
url: /nl/het-toepassen-van-median-en-wiener-filters/
---

## **Het toepassen van Median en Wiener Filters**
De median filter is een niet-lineaire digitale filtertechniek die vaak wordt gebruikt om ruis te verwijderen. Het verminderen van deze ruis is een typische voorbewerking om de resultaten van latere verwerking te verbeteren. De Wiener filter is de MSE (mean squared error) optimale stationaire lineaire filter voor afbeeldingen die zijn aangetast door additief ruis en vervaging. Met behulp van de Aspose.PSD voor .NET API kunnen ontwikkelaars een median filter toepassen om ruis uit de afbeelding te verwijderen en gauss wiener filter op afbeeldingen toe te passen. Dit artikel demonstreert hoe de median filter en gauss wiener filter op afbeeldingen kunnen worden toegepast.

### **Het toepassen van Median Filter**
Aspose.PSD biedt de [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) klasse om een filter toe te passen op een [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Het onderstaande codelocatie laat zien hoe je de median filter op een rasterafbeelding kunt toepassen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Het toepassen van Gauss Wiener Filter**
Aspose.PSD biedt de [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) klasse om een filter toe te passen op een [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Het onderstaande codelocatie laat zien hoe je het gauss wiener filter op een rasterafbeelding kunt toepassen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Het toepassen van Gauss Wiener Filter voor een Gekleurde afbeelding**
Aspose.PSD biedt ook [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) voor gekleurde afbeeldingen. Het onderstaande codelocatie laat zien hoe je het gauss wiener filter op een kleurenafbeelding kunt toepassen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Het toepassen van Motion Wiener Filter**
Aspose.PSD biedt de [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) klasse om een filter toe te passen op een [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Het onderstaande codelocatie laat zien hoe je het motion wiener filter op een rasterafbeelding kunt toepassen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Het toepassen van een Correctiefilter op een afbeelding**
Dit artikel laat zien hoe je met behulp van Aspose.PSD voor .NET correctiefilters op een afbeelding kunt toepassen. Aspose.PSD API's hebben efficiënte en gemakkelijk te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD voor .NET heeft de klassen [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)en [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions)voor filtratie blootgelegd. De klasse BilateralSmoothingFilterOptions heeft een integer nodig als grootte. De stappen om het formaat aan te passen zijn zo eenvoudig als hieronder:

1. Laad een afbeelding met behulp van de fabrieksmethode Load die wordt blootgelegd door de Image klasse.
1. Zet de afbeelding om in een RasterImage.
1. Maak een instantie van de BilateralSmoothingFilterOptions en SharpenFilterOptions klassen.
1. Roep de [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) methode aan terwijl je het rechthoek als de grenzen van de afbeelding en een instantie van de BilateralSmoothingFilterOptions klasse opgeeft.
1. Roep de [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) methode aan terwijl je het rechthoek als de grenzen van de afbeelding en een instantie van de SharpenFilterOptions klasse opgeeft.
1. Pas het contrast aan
1. Stel de helderheid in
1. Bewaar de resultaten.


## **Gebruik Bradley threshold algoritme**
Beeldthresholding wordt gebruikt in grafische toepassingen. Het doel van het thresholde van een afbeelding is om pixels te classificeren als "donker" of "licht". Aspose.PSD API stelt je in staat om Bradley thresholding te gebruiken tijdens het converteren van afbeeldingen. De volgende codelocatie laat zien hoe je de drempelwaarde kunt definiëren en vervolgens het Bradley drempelalgoritme kunt oproepen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
