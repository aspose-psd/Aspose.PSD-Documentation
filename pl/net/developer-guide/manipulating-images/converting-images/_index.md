---
title: Konwersja obrazów
type: docs
weight: 20
url: /pl/net/konwersja-obrazow/ 
---

## **Konwertowanie obrazów na czarno-białe i w odcieniach szarości**
Czasami możesz potrzebować konwertować kolorowe obrazy na czarno-białe lub w odcieniach szarości do celów drukowania lub archiwizacji. W tym artykule przedstawiono użycie interfejsu API Aspose.PSD dla .NET do osiągnięcia tego przy użyciu dwóch metod, jak opisano poniżej.

- Binarizacja
- Skalowanie odcieni szarości

### **Binarizacja**
Aby zrozumieć koncepcję binarizacji, ważne jest zdefiniowanie obrazu binarnego; jest to obraz cyfrowy, który może mieć tylko dwie możliwe wartości dla każdego piksela. Zwykle dwa kolory używane do obrazów binarnych to czerń i biel, choć można użyć dowolnych dwóch kolorów. Binarizacja to proces konwertowania obrazu na dwupoziomowy, co oznacza, że każdy piksel jest przechowywany jako pojedynczy bit (0 lub 1), gdzie 0 oznacza brak koloru, a 1 oznacza obecność koloru. Interfejs API Aspose.PSD dla .NET obecnie obsługuje dwie metody binarizacji.
#### **Binarizacja z ustalonym progiem**
Poniższy fragment kodu pokazuje, jak można zastosować binarizację z ustalonym progiem do obrazu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarizacja z progiem Otsu**
Następujący fragment kodu pokazuje, jak można zastosować binarizację z progiem Otsu do obrazu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Skalowanie odcieni szarości**
Skalowanie odcieni szarości to proces konwertowania obrazu o ciągłych odcieniach na obraz z nieciągłymi odcieniami szarości. Poniższy fragment kodu pokazuje, jak używać skalowania odcieni szarości.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}

## **Konwertowanie warstw obrazów GIF na obrazy TIFF**
Czasami konieczne jest wyodrębnienie i konwersja warstw obrazów PSD na inny format obrazu rastrowego, aby spełnić potrzeby aplikacji. Interfejs API Aspose.PSD obsługuje funkcję wyodrębniania i konwertowania warstw obrazów PSD na inny format obrazu rastrowego. Po pierwsze, utworzymy instancję obrazu i wczytamy obraz PSD z dysku lokalnego, a następnie przeiterujemy każdą warstwę w właściwości Layer. Następnie przekonwertujemy blok do obrazu TIFF. Poniższy fragment kodu pokazuje, jak konwertować warstwy obrazów PSD na obrazy TIFF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}

## **Konwertowanie pliku PSD CMYK na format TIFF CMYK**
Za pomocą interfejsu Aspose.PSD dla .NET, programiści mogą konwertować plik PSD CMYK na format tiff CMYK. W artykule pokazano, jak wyeksportować/konwertować plik PSD CMYK na format tiff CMYK za pomocą Aspose.PSD. Korzystając z Aspose.PSD dla .NET, można wczytać obrazy PSD, a następnie można ustawić różne właściwości za pomocą [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) klasy i zapisać lub wyeksportować obraz. Poniższy fragment kodu pokazuje, jak osiągnąć tę funkcję.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}

## **Eksportowanie obrazów**
Oprócz bogatego zestawu procedur przetwarzania obrazów, Aspose.PSD zapewnia specjalistyczne klasy do konwertowania formatów plików PSD na inne formaty. Korzystając z tej biblioteki, konwersja obrazów PSD jest bardzo prosta i intuicyjna. Poniżej znajdują się specjalistyczne klasy do tego celu w przestrzeni nazw [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Eksportowanie obrazów PSD za pomocą interfejsu API Aspose.PSD dla .NET jest proste. Wszystko, czego potrzebujesz, to obiekt odpowiedniej klasy z przestrzeni nazw [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions). Korzystając z tych klas, łatwo możesz wyeksportować każdy obraz utworzony, edytowany lub po prostu wczytany za pomocą interfejsu Aspose.PSD dla .NET do dowolnie obsługiwanego formatu.

## **Łączenie obrazów**
Ten przykład wykorzystuje klasę Graphics i pokazuje, jak połączyć dwa lub więcej obrazów w pojedynczy obraz kompletu. Aby zademonstrować operację, przykład tworzy nowy obraz PsdImage i rysuje obrazy na powierzchni płótna za pomocą metody Draw Image udostępnionej przez klasę Graphics. Korzystając z klasy Graphics, dwa lub więcej obrazów można połączyć w taki sposób, że wynikowy obraz będzie wyglądał jak kompletny obraz bez odstępów między częściami obrazu i bez stron. Rozmiar płótna musi być równy rozmiarowi obrazu wynikowego. Poniżej znajduje się przykład kodu pokazujący, jak korzystać z metody [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) klasy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) do łączenia obrazów w pojedynczy obraz.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **Rozszerzanie i Przycinanie obrazów**
Interfejs API Aspose.PSD pozwala na rozszerzanie lub przycinanie obrazu podczas procesu konwersji obrazu. Programista musi utworzyć prostokąt z współrzędnymi X i Y oraz określić szerokość i wysokość prostokąta. Współrzędne X, Y oraz szerokość i wysokość prostokąta będą odzwierciedlały rozszerzanie lub przycinanie wczytanego obrazu. Jeśli podczas konwersji obrazu konieczne jest rozszerzenie lub przycięcie obrazu, wykonaj następujące kroki:

1. Utwórz instancję klasy [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) i wczytaj istniejący obraz.
1. Utwórz instancję klasy ImageOption.
1. Utwórz instancję klasy [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) i zainicjuj współrzędne X, Y oraz szerokość i wysokość prostokąta.
1. Wywołaj [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) metodę klasy RasterImage, podając nazwę pliku wyjściowego, opcje obrazu i obiekt prostokąta jako parametry.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **Odczytywanie i Zapisywanie danych XMP do obrazów**
XMP (Extensible Metadata Platform) to standard ISO. XMP standaryzuje model danych, format serializacji oraz podstawowe właściwości dla definicji i przetwarzania metadanych rozszerzalnych. Zapewnia również wytyczne dotyczące osadzania informacji XMP w popularnym obrazie, takim jak JPEG, bez utraty czytelności dla aplikacji, które nie obsługują XMP. Korzystając z interfejsu API Aspose.PSD dla .NET, programiści mogą odczytywać lub zapisywać metadane XMP do obrazów. Ten artykuł demonstruje, jak metadane XMP mogą być odczytywane z obrazu i zapisywane do obrazów.
### **Utwórz obiekt metadanych XMP, Zapisz go i Oczytaj z Pliku**
Za pomocą przestrzeni nazw Xmp programista może utworzyć obiekt metadanych XMP i zapisać go do obrazu. Poniższy fragment kodu pokazuje, jak używać pakietów XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage i DublinCorePackage zawartych w przestrzeni nazw [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}

## **Eksportowanie obrazów w środowisku wielowątkowym**
Aspose.PSD dla .NET teraz obsługuje konwersję obrazów w środowisku wielowątkowym. Aspose.PSD dla .NET zapewnia zoptymalizowaną wydajność operacji podczas wykonywania kodu w środowisku wielowątkowym. Wszystkie klasy [opcji obrazów](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) (np. BmpOptions, TiffOptions, JpegOptions, itp.) w Aspose.PSD dla .NET implementują interfejs IDisposable. Dlatego konieczne jest prawidłowe zwolnienie obiektu klasy opcji obrazu w przypadku ustawienia właściwości Source. Poniższy fragment kodu demonstruje tę funkcjonalność.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD obsługuje teraz właściwość SyncRoot podczas pracy w środowisku wielowątkowym. Programista może użyć tej właściwości do synchronizacji dostępu do strumienia źródłowego. Poniższy fragment kodu demonstruje, jak można użyć właściwości SyncRoot.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}
