---
title: Konwertowanie obrazów
type: docs
weight: 20
url: /pl/java/konwertowanie-obrazow/
---

## **Konwertowanie obrazów na czarno-białe oraz odcienie szarości**
Czasami może być konieczne konwertowanie obrazów kolorowych na czarno-białe lub odcienie szarości do celów drukowania lub archiwizacji. Ten artykuł przedstawia użycie interfejsu API Aspose.PSD dla Javy w celu osiągnięcia tego za pomocą dwóch wymienionych poniżej metod.

- Binarnizacja
- Skalowanie odcieni szarości
### **Binarnizacja**
Aby zrozumieć pojęcie binarnizacji, ważne jest zdefiniowanie Obrazu Binarnego; jest to obraz cyfrowy, który może mieć tylko dwie możliwe wartości dla każdego piksela. Zazwyczaj używane są dwa kolory dla obrazu binarnego: czarny i biały, choć można użyć dowolnych dwóch kolorów. Binarnizacja polega na przekształceniu obrazu na dwupoziomowy, co oznacza, że każdy piksel jest przechowywany jako pojedynczy bit (0 lub 1), gdzie 0 oznacza brak koloru, a 1 oznacza obecność koloru. Interfejs API Aspose.PSD dla Javy obecnie obsługuje dwie metody binarnizacji.
#### **Binarnizacja z ustalonym progiem**
Poniższy fragment kodu pokazuje, jak stosować binarnizację ze stałym progiem do obrazu.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarnizacja z progiem Otsu**
Poniższy fragment kodu pokazuje, jak stosować binarnizację z progiem Otsu do obrazu.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Skalowanie odcieni szarości**
Skalowanie odcieni szarości polega na przekształceniu obrazu o ciągłym tonie na obraz z nieciągłymi odcieniami szarości. Poniższy fragment kodu pokazuje, jak stosować skalowanie odcieni szarości.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Konwertowanie warstw obrazu GIF na obraz TIFF**
Czasami konieczne jest wyodrębnienie i konwersja warstw obrazu PSD na inny format obrazu rastrowego, aby sprostać potrzebom aplikacji. Interfejs API Aspose.PSD obsługuje funkcję wyodrębnienia i konwersji warstw obrazu PSD na inny format obrazu rastrowego. Na początku stworzymy instancję obrazu i wczytamy obraz PSD z dysku lokalnego, a następnie będziemy iterować przez każdą warstwę w właściwości Layer. Następnie przekonwertujemy blok na obraz TIFF. Poniższy fragment kodu pokazuje, jak konwertować warstwy obrazu PSD na obrazy TIFF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Konwertowanie pliku CMYK PSD na TIFF CMYK**
Za pomocą Aspose.PSD dla Javy programiści mogą konwertować plik CMYK PSD na format tiff CMYK. Ten artykuł pokazuje, jak wyeksportować / skonwertować plik CMYK PSD na format tiff CMYK za pomocą Aspose.PSD. Za pomocą Aspose.PSD dla Javy można wczytywać obrazy PSD, a następnie można ustawiać różne właściwości za pomocą klasy TiffOptions i zapisywać lub eksportować obraz. Poniższy fragment kodu pokazuje, jak osiągnąć tę funkcjonalność.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Eksportowanie obrazów**
Oprócz bogatego zestawu procedur przetwarzania obrazów, Aspose.PSD dostarcza specjalizowane klasy do konwertowania formatów plików PSD na inne formaty. Korzystając z tej biblioteki, konwersja obrazów PSD jest bardzo prosta i intuicyjna. Poniżej znajdują się specjalizowane klasy do tego celu w przestrzeni nazw ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Eksportowanie obrazów PSD jest łatwe dzięki interfejsowi API Aspose.PSD dla Javy. Wszystko, czego potrzebujesz, to obiekt odpowiedniej klasy z przestrzeni nazw ImageOptions. Korzystając z tych klas, możesz łatwo eksportować dowolny obraz utworzony, edytowany lub po prostu wczytany za pomocą Aspose.PSD dla Javy do dowolnego obsługiwanego formatu.
## **Łączenie obrazów**
Ten przykład wykorzystuje klasę Graphics i pokazuje, jak połączyć dwa lub więcej obrazów w pojedynczy kompletny obraz. Aby zademonstrować operację, przykład tworzy nowy obraz PsdImage i rysuje obrazy na powierzchni płótna za pomocą metody Draw Image udostępnionej przez klasę Graphics. Korzystając z klasy Graphics, możesz połączyć dwa lub więcej obrazów w taki sposób, że rezultatowa połączony obraz będzie wyglądać jak kompletny obraz bez miejsc pomiędzy częściami obrazu i bez marginesów. Wielkość płótna musi być równa wielkości wynikowego obrazu. Poniżej znajduje się demonstracja kodu pokazująca, jak użyć metody Draw Image klasy Graphics do łączenia obrazów w jeden obraz.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Rozszerzanie i Przycinanie obrazów**
Interfejs API Aspose.PSD umożliwia rozszerzanie lub przycinanie obrazu podczas procesu konwersji obrazów. Programista musi utworzyć prostokąt z współrzędnymi X i Y oraz określić szerokość i wysokość prostokąta. Współrzędne X, Y oraz szerokość i wysokość prostokąta będą określać rozszerzanie lub przycinanie wczytanego obrazu. Jeśli podczas konwersji obrazu jest wymagane jego rozszerzanie lub przycinanie, wykonaj następujące kroki:

1. Utwórz instancję klasy RasterImage i wczytaj istniejący obraz.
1. Utwórz instancję klasy ImageOption.
1. Utwórz instancję klasy Rectangle i zainicjuj współrzędne X, Y oraz szerokość i wysokość prostokąta.
1. Wywołaj metodę Save klasy RasterImage, przekazując nazwę pliku wyjściowego, opcje obrazu i obiekt prostokąta jako parametry.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Odczytanie i Zapisanie danych XMP do obrazów**
XMP (Extensible Metadata Platform) to standard ISO. XMP standaryzuje model danych, format serializacji i podstawowe właściwości do definiowania i przetwarzania metadanych rozszerzalnych. Zapewnia również wskazówki dotyczące osadzania informacji XMP w popularnych formatach obrazów, takich jak JPEG, bez zagrożenia ich czytelności przez aplikacje, które nie obsługują XMP. Za pomocą interfejsu API Aspose.PSD dla Javy programiści mogą odczytywać lub zapisywać metadane XMP do obrazów. Ten artykuł przedstawia, jak metadane XMP mogą być odczytywane z obrazu i jak metadane XMP można zapisywać do obrazów.
### **Utwórz metadane XMP, zapisz je i odczytaj z pliku**
Dzięki przestrzeni nazw XMP deweloper może utworzyć obiekt metadanych XMP i zapisać go do obrazu. Poniższy fragment kodu pokazuje, jak korzystać z pakietów XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage i DublinCorePackage zawartych w przestrzeni nazw XMP.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Eksportowanie obrazów w środowisku wielowątkowym**
Aspose.PSD dla Javy obsługuje teraz konwertowanie obrazów w środowisku wielowątkowym. Aspose.PSD dla Javy zapewnia zoptymalizowaną wydajność operacji podczas wykonywania kodu w środowisku wielowątkowym. Wszystkie klasy opcji obrazu (np. BmpOptions, TiffOptions, JpegOptions, itp.) w Aspose.PSD dla Javy implementują interfejs IDisposable. Dlatego konieczne jest, aby deweloper prawidłowo zwolnił obiekt klasy opcji obrazu w przypadku ustawienia właściwości źródłowej. Poniższy fragment kodu demonstruje tę funkcjonalność.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSD teraz obsługuje właściwość SyncRoot podczas pracy w środowisku wielowątkowym. Deweloper może użyć tej właściwości do synchronizacji dostępu do strumienia źródłowego. Poniższy fragment kodu demonstruje, w jaki sposób można użyć właściwości SyncRoot.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}
