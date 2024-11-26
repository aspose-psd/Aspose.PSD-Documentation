---
title: Modyfikowanie obrazów TIFF
type: docs
weight: 50
url: /pl/net/modyfikowanie-obrazow-tiff/
---

## **Dodaj ramki z różnymi ustawieniami**
TIFF jest formatem bardzo elastycznym, który pozwala dodawać różne ramki o różnych wymiarach, kompresji i innych ustawieniach. Interfejsy API Aspose.PSD umożliwiają dodawanie dowolnej ramki TIFF o dowolnym rozmiarze, co pomaga w tworzeniu złożonych dokumentów. Jeśli istnieje wymaganie dostosowania ramek podczas procesu dodawania, aby stały się one równe, wykonaj następujące kroki:

- Utwórz nową pustą ramkę z żądanymi opcjami lub skopiuj ramkę źródłową z określonymi opcjami wyjściowymi, korzystając z metody CreateFrameFrom.
- Zmień rozmiar ramki/obrazu źródłowego na żądane wymiary za pomocą metody Resize.
- Dodaj piksele ramki/obrazu źródłowego do nowej ramki.
- Dodaj nową ramkę do obrazu TIFF wynikowego.

## **Eksportuj warstwy obrazu PSD do formatu pliku Multi-Page Tiff**
Czasami konieczne jest wyeksportowanie warstw obrazu PSD do formatu pliku Multi-Page TIFF. Ten artykuł pokaże, jak można wykonać to zadanie za pomocą interfejsu API Aspose.PSD dla .NET. Na początku wczytamy obraz PSD z dysku. Następnie będziemy iterować po warstwach obrazu PSD i tworzyć TiffFrame z odpowiadających warstw. Na koniec zapiszemy rezultujący obraz Tiff w pojedynczym pliku na dysku.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}

## **Konfiguracja opcji TiffOptions**
Programiści mogą dostosować różne właściwości klasy [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) w celu uzyskania pożądanych wyników. W tym dokumencie skupimy się na 4 głównych właściwościach kontrolujących atrybuty obrazu wynikowego.

Poniżej wymienione są te właściwości.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Podczas inicjalizacji pustej struktury TiffOptions, każda opcja jest ustawiona na wartość domyślną, na przykład kompresja jest ustawiona jako Brak, BitsPerSample ustawiony jest na 1, a Photometric na MinIsWhite. Zapisanie w tym formacie spowoduje, że ostateczny obraz będzie czarno-biały, co jest oczekiwanym zachowaniem dla takiej kombinacji opcji. Aby uzyskać kolorowe rezultaty, należy ustawić wszystkie wyżej wymienione właściwości na wartości odpowiadające pożądanemu przestrzeni barwnej lub można zainicjalizować strukturę TiffOptions z ustawieniami predefiniowanymi, o których mowa później w tym artykule. Poniżej przedstawiona jest tabela opisująca oczekiwane wartości parametrów, które można ustawić, aby osiągnąć pożądane wyniki. Należy zauważyć, że wszystkie 4 kolumny powinny być ustawione za pomocą TiffOptions, aby zapisać dowolny obraz w formacie TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Nieskompresowany|1/4/8/16 (paleta, tryb koloru) tylko pojedynczy kanał|Brak|
|MinIsWhite/MinIsBlack|LZW/Nieskompresowany|1/4/8/16 (tryb odcieni szarości) tylko pojedynczy kanał|Brak|
|Paleta|LZW/Nieskompresowany|8 (paleta, tryb koloru) tylko pojedynczy kanał|Poziomy (większa kompresja jest osiągana dla LZW tych samych wzorców)|
|MinIsWhite/MinIsBlack|LZW/Nieskompresowany|8 (tryb odcieni szarości) tylko pojedynczy kanał|Poziomy (większa kompresja jest osiągana dla LZW tych samych wzorców)|
|RGB|LZW/Nieskompresowany|[8,8,8] (3 kanały RGB)|Brak/Poziomy|
|RGB|LZW/Nieskompresowany|[8,8,8,8] (3 kanały RGB i dodatkowy kanał alfa można ustawić za pomocą TiffOptions.AlphaStorage) W rzeczywistości obsługiwana jest dowolna liczba dodatkowych kanałów, ale każdy kanał musi mieć wielkość 8 bitów, np. [8,8,8,8,8,8]|Brak/Poziomy|
Wszystkie 4 właściwości powinny być ustawione za pomocą TiffOptions, aby zapisać obraz w dowolnym formacie w formacie Tiff. Przy wykorzystaniu różnych kombinacji niektóre przeglądarki (w tym przeglądarka zdjęć systemu Windows) mogą odmówić renderowania wynikowego obrazu ze względu na ograniczoną obsługę, którą oferują. W takim przypadku wybierz inną przeglądarkę do celów testowych.

### **Predefiniowane ustawienia dla klasy TiffOptions**
Aby ułatwić użytkownikom i uniknąć błędów konfiguracji instancji TiffOptions, interfejs API Aspose.PSD dla .NET udostępnił inny konstruktor, który przyjmuje parametr typu [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Na podstawie wybranej wartości z wyliczenia TiffExpectedFormat, interfejs API automatycznie konfiguruje wszystkie obowiązkowe właściwości dla instancji TiffOptions w celu uzyskania pożądanych wyników. Przed przejściem do przykładowego kodu oto lista pól TiffExpectedFormat i ich szczegółów dla lepszego zrozumienia użycia.

- TiffExpectedFormat.Default: Ustawienie pola na Default zachowuje się podobnie do domyślnego konstruktora klasy TiffOptions bez ustawionej kompresji i BitsPerPixel ustawionego na 1 w celu uzyskania czarno-białego wyniku. Zaleca się korzystanie z tego pola, gdy inne właściwości związane z formatem mają być ustawione ręcznie zgodnie z pożądanymi wynikami.
- TiffExpectedFormat.TiffCcitRle: Specyficzne dla kodowania RLE podczas zapisywania wyniku w formacie TIFF 1 BitsPerPixel (czarno-biały).
- TiffExpectedFormat.TiffCcittFax3: Specyficzne dla kodowania CCITT Fax3 podczas zapisywania wyniku w formacie TIFF 1 BitsPerPixel (czarno-biały).
- TiffExpectedFormat.TiffCcittFax4: Specyficzne dla kodowania CCITT Fax4 podczas zapisywania wyniku w formacie TIFF 1 BitsPerPixel (czarno-biały).
- TiffExpectedFormat.TiffDeflateBW: Specyficzne dla kompresji Deflate podczas zapisywania wyniku w formacie TIFF 1 BitsPerPixel (czarno-biały).
- TiffExpectedFormat.TiffDeflateRGB: Specyficzne dla kompresji Deflate podczas zapisywania wyniku w formacie TIFF RGB (kolor).
- TiffExpectedFormat.TiffJpegRGB: Specyficzne dla kompresji Jpeg podczas zapisywania wyniku w formacie TIFF RGB (kolor).
- TiffExpectedFormat.TiffJpegYCBCR: Specyficzne dla kompresji Deflate podczas zapisywania wyniku w formacie TIFF YCBCR (kolor).
- TiffExpectedFormat.TiffLzwBW: Specyficzne dla kompresji LZW podczas zapisywania wyniku w formacie TIFF 1 BitsPerPixel (czarno-biały).
- TiffExpectedFormat.TiffLzwRGB: Specyficzne dla kompresji LZW podczas zapisywania wyniku w formacie TIFF RGB (kolor).
- TiffExpectedFormat.TiffLzwRGBA: Specyficzne dla kompresji LZW podczas zapisywania wyniku w formacie TIFF RGBA (kolor z przejrzystością).
- TiffExpectedFormat.TiffNoCompressionBW: Specyficzne dla niekompresowanego formatu TIFF podczas zapisywania wyniku w formacie 1 BitsPerPixel (czarno-biały).
- TiffExpectedFormat.TiffNoCompressionRGB: Specyficzne dla niekompresowanego formatu TIFF podczas zapisywania wyniku w formacie RGB (kolor).
- TiffExpectedFormat.TiffNoCompressionRGBA: Specyficzne dla niekompresowanego formatu TIFF podczas zapisywania wyniku w formacie RGBA (kolor z przejrzystością).

Poniższy fragment kodu wyjaśnia użycie pól TiffExpectedFormat przy tworzeniu instancji klasy TiffOptions.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}

## **Obsługa kompresji Deflate i Adobe Deflate**
Format pliku TIFF (Tagged Image File Format) obsługuje różne typy kompresji, podczas gdy typ kompresji jest przechowywany jako znacznik (wartość całkowita) w pliku. Jednym z takich metod kompresji jest Adobe Deflate (wcześniej znany jako Deflate). Interfejs API Aspose.PSD dla .NET obsługuje tę metodę kompresji do eksportu i tworzenia obrazów TIFF.
### **Zapis obrazu do formatu TIFF z kompresją Deflate**
Konwersja wczytanych obrazów do formatu TIFF z kompresją Deflate/Adobe Deflate jest łatwa do wykonania.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Tworzenie obrazu TiffImage z kompresją Adobe Deflate**
Poniższy przykład demonstruje użycie interfejsu API Aspose.PSD dla .NET do utworzenia obrazu od podstaw za pomocą metody kompresji Adobe Deflate.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Kompresowanie obrazów TIFF**
Interfejs API Aspose.PSD dla .NET może być używany do konwersji obrazów PSD do formatu obrazu TIFF oraz zmiany kompresji rezultującego obrazu TIFF. API może być również użyte do przechowywania różnych obrazów jako ramek w obrazie TIFF do celów archiwizacyjnych, przy równoczesnym kompresowaniu obrazów do rozmiaru danych minimalnego. Kompresja obrazu powinna być przeprowadzana poprzez zmniejszenie rozmiaru danych źródłowych, niezależnie od użytego algorytmu kompresji. Aby uzyskać najlepsze współczynniki kompresji, możemy użyć przestrzeni kolorów indeksowanych. Poniższy fragment kodu wykonuje najlepszą kompresję przy użyciu 16 kolorów indeksowanych i algorytmu kompresji LZW, chociaż kolory źródłowe są nieznacznie rozmyte.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}
