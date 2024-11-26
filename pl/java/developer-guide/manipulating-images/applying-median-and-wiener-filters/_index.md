---
title: Zastosowanie filtrów medianowych i Wienera
type: docs
weight: 10
url: /pl/java/zastosowanie-filtrow-medianowych-i-wienera/
---

## **Zastosowanie filtrów medianowych i Wienera**
Filtr medianowy to nieliniowa technika filtrowania cyfrowego, często używana do usuwania szumów. Takie zmniejszenie szumów jest typowym krokiem wstępnym w celu poprawy wyników późniejszej obróbki. Filtr Wienera jest optymalnym filtrem MSE (błędu średniokwadratowego) do filtracji liniowej obrazów zdegradowanych przez szum dodawany i zamazanie. Korzystając z interfejsu API Aspose.PSD dla Javy, programiści mogą zastosować filtr medianowy w celu usunięcia szumów z obrazu oraz zastosować filtr Gaussa Wienera na obrazach. Ten artykuł demonstrowe, jak zastosować filtr medianowy i filtr Gaussa Wienera do obrazów.

### **Zastosowanie Filtra Medianowego**
Aspose.PSD udostępnia klasę MedianFilterOptions do zastosowania filtru na RasterImage. Poniższy fragment kodu demonstruje, jak zastosować filtr medianowy do obrazu rastrowego.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **Zastosowanie Filtra Gaussa Wienera**
Aspose.PSD udostępnia klasę GaussWienerFilterOptions do zastosowania filtru na RasterImage. Poniższy fragment kodu demonstruje, jak zastosować filtr Gaussa Wienera do obrazu rastrowego.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **Zastosowanie Filtra Gaussa Wienera do Obrazu Kolorowego**
Aspose.PSD udostępnia klasę GaussWienerFilterOptions także do obrazów kolorowych. Poniższy fragment kodu demonstruje, jak zastosować filtr Gaussa Wienera do obrazu kolorowego.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **Zastosowanie Filtra Wienera Ruchu**
Aspose.PSD udostępnia klasę MotionWienerFilterOptions do zastosowania filtru na RasterImage. Poniższy fragment kodu demonstruje, jak zastosować filtr Wienera ruchu do obrazu rastrowego.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **Zastosowanie Filtra Korekcyjnego Na Obrazie**
Ten artykuł demonstruje użycie Aspose.PSD dla Javy do stosowania filtrów korekcyjnych na obrazie. API Aspose.PSD udostępnia wydajne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD dla Javy udostępnia klasy BilateralSmoothingFilterOptions i SharpenFilterOptions do filtrowania. Klasa BilateralSmoothingFilterOptions wymaga podania liczby całkowitej jako rozmiaru. Kroki do wykonania zmiany rozmiaru są proste, jak poniżej:


1. Załaduj obraz za pomocą metody fabrycznej Load udostępnionej przez klasę Image.
1. Konwertuj obraz na RasterImage.
1. Utwórz instancje klas BilateralSmoothingFilterOptions i SharpenFilterOptions.
1. Wywołaj metodę Filter klasy RasterImage, podając prostokąt jako granice obrazu i instancję klasy BilateralSmoothingFilterOptions.
1. Wywołaj metodę Filter klasy RasterImage, podając prostokąt jako granice obrazu i instancję klasy SharpenFilterOptions.
1. Dostosuj kontrast.
1. Ustaw jasność.
1. Zapisz wyniki.

Poniższy fragment kodu pokazuje, jak zastosować filtr korekcyjny.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **Użyj algorytmu progowania Bradley'a**
Progowanie obrazu jest używane w aplikacjach graficznych. Celem progowania obrazu jest sklasyfikowanie pikseli jako „ciemne” lub „jasne”. Interfejs API Aspose.PSD pozwala na użycie progowania Bradley'a podczas konwertowania obrazów. Poniższy fragment kodu pokazuje, jak zdefiniować wartość progu, a następnie wywołać algorytm progowania Bradley'a.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
