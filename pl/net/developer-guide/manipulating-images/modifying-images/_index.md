---
title: Modyfikowanie obrazów
type: docs
weight: 50
url: /pl/net/modyfikowanie-obrazow/
---

## **Dithering dla obrazów rastrowych**
Dithering to technika tworzenia złudzenia nowych kolorów i odcieni poprzez zmienianie wzoru kropek, które faktycznie tworzą obraz. Jest to najczęstszy sposób redukcji zakresu kolorów obrazów do 256 (lub mniej) kolorów. Aspose.PSD zapewnia obsługę ditheringu dla klasy [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) poprzez wprowadzenie metody Dither, która przyjmuje dwa parametry. Pierwszy to rodzaj DitheringMethod, który ma dwie możliwe opcje: FloydSteinbergDithering i ThresholdDithering. Drugi parametr dla metody [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) to BitCount typu int. BitCount definiuje rozmiar próbkowania dla wyniku ditheringu. Wartość domyślna to 1, co reprezentuje czarno-biały, podczas gdy dozwolone wartości to 1, 4, 8 generujące palety z kolejno 2, 4 i 256 kolorami.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}

## **Dostosowywanie jasności, kontrastu i gammy**
Dostosowywanie kolorów w obrazach cyfrowych to jedna z podstawowych funkcji, które większość bibliotek przetwarzania obrazów udostępnia. Dostosowanie kolorów można podzielić na następujące kategorie.

1. Jasność odnosi się do jasności lub ciemności koloru. Zwiększenie jasności obrazu powoduje rozjaśnienie wszystkich kolorów, podczas gdy zmniejszenie jasności przyciemnia wszystkie kolory.
1. Kontrast odnosi się do zwiększenia czytelności obiektów lub szczegółów na obrazie. Zwiększenie kontrastu obrazu zwiększa różnicę między obszarami jasnymi i ciemnymi, aby obszary jasne stawały się jaśniejsze, a obszary ciemne ciemniejsze. Zmniejszenie kontrastu sprawi, że obszary jaśniejsze i ciemniejsze pozostaną mniej więcej takie same, ale ogólny obraz stanie się bardziej jednolity.
1. Gamma optymalizuje kontrast i jasność pośredniego oświetlenia, które oświetla obiekt na obrazie.
### **Dostosowywanie jasności**
API Aspose.PSD dla .NET udostępnia metodę [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) dla klasy [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), która może być użyta do dostosowania jasności obrazu poprzez przekazanie wartości całkowitej jako parametru. Najwyższa wartość parametru oznacza jaśniejszy obraz. Oto oryginalny obraz i obraz wynikowy do porównania.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}

### **Dostosowywanie kontrastu**
Metoda [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) udostępniana przez klasę [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) może być użyta do dostosowania kontrastu obrazu, przekazując wartość zmiennoprzecinkową jako parametr.

Najwyższa wartość parametru oznacza wyższy kontrast w danym obrazie. Oto oryginalny obraz i obraz wynikowy do porównania.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}

### **Dostosowywanie gammy**
Metoda [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) udostępniana przez klasę [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) posiada dwie wersje. Jedna z przeciążeń akceptuje jedną wartość zmiennoprzecinkową i wykonuje korektę gammy dla współczynników kanałów czerwonego, niebieskiego i zielonego. Natomiast drugie przeciążenie akceptuje trzy wartości zmiennoprzecinkowe reprezentujące każdy współczynnik koloru osobno. Poniższy przykład kodu demonstruje, jak wykonać dostosowanie gammy na obrazie.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}

## **Rozmyj obraz**
Ten artykuł demonstruje użycie Aspose.PSD dla .NET do wykonania efektu rozmycia na obrazie. API Aspose.PSD udostępnia efektywne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD dla .NET udostępnia klasę [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) do tworzenia efektu rozmycia na żywo. Klasa [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) wymaga wartości promienia i sigma do stworzenia efektu rozmycia na obrazie. Procedura do wykonania rozmycia jest prosta, jak poniżej:

1. Wczytaj obraz za pomocą metody fabrycznej Load udostępnianej przez klasę Image.
1. Konwertuj obraz na [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Utwórz instancję klasy [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) z domyślnym konstruktorem lub podaj wartości promienia i sigma w konstruktorze.
1. Wywołaj metodę [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter, podając prostokąt jako granice obrazu i instancję klasy [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Zapisz wyniki.

Poniższy przykład kodu demonstruje, jak stworzyć efekt rozmycia na obrazie.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}

## **Sprawdź transparentność obrazu**
Ten artykuł demonstruje użycie Aspose.PSD dla .NET w celu sprawdzenia transparentności obrazu. Procedura sprawdzenia transparentności obrazu jest prosta, jak poniżej:

1. Wczytaj obraz za pomocą metody fabrycznej [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) udostępnianej przez klasę [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Sprawdź przezroczystość obrazu, jeśli przezroczystość wynosi zero, obraz jest przezroczysty.
1. Poniższy przykład kodu demonstruje, jak sprawdzić, czy obraz jest transparentny czy nie.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}

## **Wprowadź kompresor GIF z utratą jakości**
Wykorzystując Aspose.PSD dla .NET, programiści mogą ustawić różnicę pikseli. Kompresja GIF opiera się na „słowniku” ciągów pikseli. Normalny kodownik przeszukuje słownik, aby znaleźć najdłuższy ciąg pikseli, który dokładnie pasuje do pikseli na obrazie. Koder stratny wybiera najdłuższy ciąg pikseli, który jest „wystarczająco podobny” do pikseli na obrazie. Poniżej znajduje się prezentacja kodowa wspomnianej funkcjonalności.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}

## **Wprowadź przeskalowanie bicubiczne**
Przeskalowanie oznacza zmianę wymiarów pikseli obrazu. Gdy zmniejszasz próbkę, eliminujesz piksele i tym samym usuwasz informacje i szczegóły z obrazu. Gdy zwiększasz próbkę, dodajesz piksele. Adobe Photoshop dodaje te piksele za pomocą interpolacji. Ten artykuł demonstruje, jak wykonać przeskalowanie bicubiczne, korzystając z Aspose.PSD dla .NET.

Poniżej znajduje się prezentacja kodowa wspomnianej funkcjonalności.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}

## **Warstwa dostosowania bilansu kolorów**
Ten artykuł demonstruje użycie Aspose.PSD dla .NET do wykonania **warstwy dostosowania bilansu kolorów** na obrazie. Warstwa dostosowania bilansu kolorów umożliwia dokonywanie dostosowań kolorów obrazów. Przedstawia trzy kanały kolorów i ich kolory komplementarne, dzięki czemu można dostosować balans tych par, aby zmienić wygląd zdjęcia.

Poniżej znajduje się prezentacja kodowa wspomnianej funkcjonalności.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}

## **Warstwa dostosowania odwrócenia**
Ten artykuł demonstruje, jak wykonać **warstwę dostosowania odwrócenia** za pomocą Aspose.PSD dla .NET. Warstwa dostosowania to specjalny rodzaj warstwy stosowany głównie do korekty kolorów. Zamiast posiadać własną zawartość, dostosowują one informacje na warstwach pod nimi. Warstwa dostosowania odwraca efekt kolorów w obrazie, tworząc efekt negatywu.

Poniżej znajduje się prezentacja kodowa wspomnianej funkcjonalności.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}
