---
title: Modyfikowanie obrazów
type: docs
weight: 50
url: /pl/java/modyfikowanie-obrazow/
---

## **Dyfuzja dla obrazów rastrowych**
Dyfuzja to technika tworzenia iluzji nowych kolorów i odcieni poprzez zmienianie wzoru kropek, które faktycznie tworzą obraz. Jest to najczęstszy sposób zmniejszania zakresu kolorów obrazów do 256 (lub mniej) kolorów. Aspose.PSD zapewnia obsługę dyfuzji dla klasy RasterImage poprzez wprowadzenie metody Dither, która przyjmuje dwa parametry. Pierwszy to typ DitheringMethod, który ma dwie możliwe opcje: FloydSteinbergDithering i ThresholdDithering. Drugi parametr dla metody Dither to BitCount w postaci liczby całkowitej. BitCount określa rozmiar próbkowania dla wyniku dyfuzji. Wartość domyślna to 1, co oznacza czarno-biały kolor, a dozwolone wartości to 1, 4, 8, generujące palety zawierające odpowiednio 2, 4 i 256 kolorów.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}

## **Dostosowywanie jasności, kontrastu i gammy**
Korekty kolorów w obrazach cyfrowych to jedna z podstawowych funkcji, które oferują większość bibliotek przetwarzania obrazów. Korekty kolorów można podzielić na następujące kategorie:

1. Jasność odnosi się do jasności lub ciemności koloru. Zwiększenie jasności obrazu rozjaśnia wszystkie kolory, podczas gdy zmniejszenie jasności ściemnia wszystkie kolory.
1. Kontrast odnosi się do zwiększenia czytelności obiektów lub szczegółów w obrazie. Zwiększenie kontrastu obrazu zwiększa różnicę między obszarami jasnymi i ciemnymi, tak że obszary jasne stają się jaśniejsze, a ciemne obszary stają się ciemniejsze. Zmniejszenie kontrastu sprawi, że jaśniejsze i ciemniejsze obszary pozostaną mniej więcej takie same, ale ogólny obraz staje się bardziej jednolity.
1. Gamma optymalizuje kontrast i jasność pośredniego oświetlenia, które oświetla obiekt na obrazie.

### **Dostosowywanie jasności**
Aspose.PSD dla Java API dostarcza metodę AdjustBrightness dla klasy RasterImage, która może być używana do dostosowywania jasności obrazu, przekazując wartość całkowitą jako parametr. Najwyższa wartość parametru oznacza jaśniejszy obraz. Poniżej przedstawiono oryginalny obraz i obraz wynikowy do porównania.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}

### **Dostosowywanie kontrastu**
Metoda AdjustContrast eksponowana przez klasę RasterImage może być użyta do dostosowania kontrastu obrazu, przekazując wartość zmiennoprzecinkową jako parametr.

Najwyższa wartość parametru oznacza wyższy kontrast na danym obrazie. Poniżej przedstawiono oryginalny obraz i obraz wynikowy do porównania.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}

### **Dostosowanie gammy**
Metoda AdjustGamma eksponowana przez klasę RasterImage posiada dwie wersje. Jedna z nich przyjmuje jedną wartość zmiennoprzecinkową i wykonuje korekcję gammy dla współczynników czerwieni, niebieskiego i zielonego kanału. Natomiast druga wersja przyjmuje trzy wartości zmiennoprzecinkowe reprezentujące każdy współczynnik koloru osobno. Poniższy przykład pokazuje, jak zastosować dostosowanie gammy na obrazie.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}

## **Rozmycie obrazu**
Ten artykuł demonstruje użycie biblioteki Aspose.PSD dla Javy do wykonania efektu rozmycia na obrazie. Interfejsy API Aspose.PSD oferują wydajne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD dla Javy udostępnia klasę GaussianBlurFilterOptions do tworzenia efektu rozmycia w locie. Klasa GaussianBlurFilterOptions wymaga wartości promienia i sigma do utworzenia efektu rozmycia na obrazie. Kroki do wykonania zmiany rozmiaru są proste:

1. Wczytaj obraz za pomocą metody Load wystawionej przez klasę Image.
1. Konwertuj obraz na RasterImage.
1. Utwórz instancję klasy GaussianBlurFilterOptions za pomocą konstruktora domyślnego lub podaj wartości promienia i sigma w konstruktorze.
1. Wywołaj metodę RasterImage.Filter, podając jako parametry prostokąt jako granice obrazu i instancję klasy GaussianBlurFilterOptions.
1. Zapisz wyniki.

Poniższy przykład kodu pokazuje, jak utworzyć efekt rozmycia na obrazie.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}

## **Sprawdź przejrzystość obrazu**
Ten artykuł demonstruje użycie Aspose.PSD dla Javy do sprawdzenia przejrzystości obrazu. Kroki do sprawdzenia przejrzystości obrazu są proste:

1. Wczytaj obraz za pomocą metody Load wystawionej przez klasę Image.
1. Sprawdź przezroczystość obrazu - jeśli przezroczystość wynosi zero, obraz jest transparentny.
Poniższy przykład kodu pokazuje, jak sprawdzić, czy obraz jest transparentny czy nie.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}

## **Wdrażanie kompresora plików GIF z utratą jakości**
Za pomocą Aspose.PSD dla Javy programiści mogą ustawić różnicę pikseli. Kompresja GIF-a opiera się na "słowniku" łańcuchów pikseli widzianych. Normalny kodownik wyszukuje w słowniku najdłuższy łańcuch pikseli, który dokładnie pasuje do pikseli na obrazie. Koder stratny wybiera najdłuższy łańcuch pikseli, który jest wystarczająco "podobny" do pikseli na obrazie. Poniżej znajduje się przykładowy kod realizujący tę funkcjonalność.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}

## **Wdrożenie interpolacji bicubicznej**
Interpolacja oznacza zmianę wymiarów pikseli obrazu. Gdy obniżasz próbkowanie, eliminujesz piksele i tym samym usuwasz informacje i detale z obrazu. Gdy zwiększasz próbkowanie, dodajesz piksele. Photoshop dodaje te piksele, używając interpolacji. Ten artykuł demonstruje, jak można wykonać interpolację bicubiczną, korzystając z Aspose.PSD dla Javy.

Poniżej znajduje się przykładowy kod realizujący tę funkcjonalność.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}

## **Warstwa dostosowania odwrócenia**
Ten artykuł demonstruje, jak można wykonać **warstwę dostosowania odwrócenia** za pomocą Aspose.PSD dla Javy. Warstwa dostosowania to specjalny rodzaj warstwy, używany głównie do korekcji koloru. Zamiast mieć własną zawartość, dostosowuje informacje na warstwach poniżej niej. Warstwa dostosowania odwraca kolory obrazu, tworząc efekt negatywny.

Poniżej znajduje się przykładowy kod realizujący tę funkcjonalność.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}
