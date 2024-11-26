---
title: Zastosowanie filtrów Median i Wiener
type: docs
weight: 10
url: /pl/zastosowanie-filtrow-median-i-wiener/
---

## **Zastosowanie filtrów Median i Wiener**
Filtr medianowy to nieliniowa technika cyfrowego filtrowania, często stosowana do usuwania szumów. Redukcja takich szumów to typowy krok wstępnego przetwarzania mający na celu poprawę wyników późniejszego przetwarzania. Filtr Wienera jest optymalnym filtrem liniowym MSE (średni błąd kwadratowy) dla obrazów zdegradowanych przez szum dodawany i rozmywanie. Korzystając z interfejsu API Aspose.PSD dla .NET, programiści mogą zastosować filtr medianowy do odszumienia obrazu oraz filtr Wienera Gaussa na obrazach. W tym artykule przedstawiono, jak filtr medianowy oraz filtr Wienera Gaussa mogą być zastosowane do obrazów.
### **Zastosowanie Filtra Medianowego**
Aspose.PSD udostępnia klasę [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) do stosowania filtra na [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Poniższy fragment kodu pokazuje, jak zastosować filtr medianowy do obrazu rastrowego.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Zastosowanie Filtra Gaussa Wienera**
Aspose.PSD udostępnia klasę [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) do stosowania filtra na [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Poniższy fragment kodu pokazuje, jak zastosować filtr Gaussa Wienera do obrazu rastrowego.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Zastosowanie Filtra Gaussa Wienera dla Obrazu Kolorowego**
Aspose.PSD udostępnia [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)do kolorowych obrazów. Poniższy fragment kodu pokazuje, jak zastosować filtr Gaussa Wienera do obrazu kolorowego.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Zastosowanie Filtra Drgania Wienera**
Aspose.PSD udostępnia klasę [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions)do stosowania filtra na [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Poniższy fragment kodu pokazuje, jak zastosować filtr Wienera do obrazu rastrowego.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Zastosowanie Filtra Korekcji Na Obrazie**
Ten artykuł przedstawia wykorzystanie Aspose.PSD dla .NET do przeprowadzenia filtrów korekcyjnych na obrazie. Interfejsy API Aspose.PSD udostępniają wydajne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD dla .NET udostępnia klasy [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)i [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions)dla filtracji. Klasa BilateralSmoothingFilterOptions wymaga wartości całkowitej jako rozmiaru. Kroki do wykonania zmiany rozmiaru są proste, jak poniżej:

1. Zaalokuj obraz za pomocą metody fabrycznej Load udostępnianej przez klasę Image.
1. Konwertuj obraz na RasterImage.
1. Utwórz instancję klas BilateralSmoothingFilterOptions i SharpenFilterOptions.
1. Wywołaj metodę [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), podając prostokąt jako granice obrazu i instancję klasy BilateralSmoothingFilterOptions.
1. Wywołaj metodę [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), podając prostokąt jako granice obrazu i instancję klasy SharpenFilterOptions.
1. Dostosuj kontrast
1. Ustaw jasność
1. Zapisz wyniki.


## **Użycie algorytmu progowania Bradley'a**
Progowanie obrazu jest stosowane w aplikacjach graficznych. Celem progowania obrazu jest klasyfikacja pikseli jako "ciemnych" lub "jasnych". Interfejs API Aspose.PSD pozwala na użycie progowania Bradley'a podczas konwersji obrazów. Poniższy fragment kodu pokazuje, jak zdefiniować wartość progu, a następnie wywołać algorytm progowania Bradley'a.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
