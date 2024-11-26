---
title: Modyfikowanie obrazów TIFF
type: docs
weight: 40
url: /pl/java/modyfikowanie-obrazow-tiff/
---

## **Dodawanie ramek z różnymi ustawieniami**
TIFF to bardzo elastyczny format, który pozwala dodawać różne ramki o różnych wymiarach, kompresji i innych ustawieniach. Interfejsy API Aspose.PSD umożliwiają dodawanie dowolnej ramki TIFF o dowolnym rozmiarze, co pomaga w tworzeniu bardziej skomplikowanych dokumentów. Jeśli zachodzi konieczność dostosowania ramek podczas procesu dodawania, aby stały się one równe, wykonaj następujące kroki:

- Utwórz nową pustą ramkę z żądanymi opcjami lub skopiuj ramkę źródłową ze wskazanymi opcjami wyjściowymi za pomocą metody CreateFrameFrom.
- Zmień rozmiar ramki/obrazu źródłowego na żądane wymiary za pomocą metody Resize.
- Dodaj piksele ramki/obrazu źródłowego do nowej ramki.
- Dodaj nową ramkę do obrazu TIFF wyjściowego.

## **Eksportowanie warstw obrazu PSD do formatu pliku TIFF wielostronicowego**
Czasami konieczne jest wyeksportowanie warstw obrazu PSD do formatu pliku TIFF wielostronicowego. W tym artykule zostanie pokazane, jak można wykonać to zadanie za pomocą interfejsu API Aspose.PSD dla Javy. Najpierw wczytamy obraz PSD z dysku. Następnie iterujemy po warstwach obrazu PSD i tworzymy TiffFrame z odpowiadających warstw. W końcu zapiszemy rezultujący obraz TIFF do pojedynczego pliku na dysku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **Konfiguracja opcji TiffOptions**


Programiści mogą dostosowywać różne właściwości klasy TiffOptions, aby uzyskać pożądane rezultaty. W tym dokumencie skupimy się na 4 głównych właściwościach kontrolujących atrybuty obrazu wynikowego.

Poniżej wymieniono te właściwości.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Przy inicjalizacji pustej struktury Tiffoptions, każda opcja jest ustawiona na swoją wartość domyślną, na przykład kompresja jest ustawiona jako None, BitsPerSample jest ustawiony na 1, a Photometric jako MinIsWhite. Zapisując w tym formacie, ostateczny obraz będzie czarno-biały, co jest oczekiwanym zachowaniem dla tej kombinacji opcji. Aby uzyskać kolorowe rezultaty, wszystkie powyższe właściwości należy ustawić na wartości odpowiadające przestrzeni barw lub można zainicjować strukturę Tiffoptions z predefiniowanymi ustawieniami, jak omówiono później w tym artykule. Poniżej znajduje się tabela opisująca oczekiwane wartości parametrów, które można ustawić, aby uzyskać pożądane rezultaty. Należy pamiętać, że wszystkie 4 kolumny należy ustawić za pomocą Tiffoptions, aby zapisać jakikolwiek obraz załadowany/stworzony w formacie TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Bez kompresji|1/4/8/16 (paleta, tryb kolorowy) tylko jednokanałowe|Brak|
|MinIsWhite/MinIsBlack|LZW/Bez kompresji|1/4/8/16 (tryb skali szarości) tylko jednokanałowe|Brak|
|Paleta|LZW/Bez kompresji|8 (paleta, tryb kolorowy) tylko jednokanałowe|Poziomy (większa kompresja osiągana dla LZW tych samych wzorców)|
|MinIsWhite/MinIsBlack|LZW/Bez kompresji|8 (tryb skali szarości) tylko jednokanałowe|Poziomy (większa kompresja osiągana dla LZW tych samych wzorców)|
|RGB|LZW/Bez kompresji|[8,8,8] (3 kanały RGB)|Brak/Poziomy|
|RGB|LZW/Bez kompresji|[8,8,8,8] (3 kanały RGB oraz dodatkowy kanał alfa można ustawić za pomocą TiffOptions.AlphaStorage) Faktycznie można obsługiwać dowolną liczbę dodatkowych kanałów, ale każdy kanał musi mieć rozmiar 8 bitów, tak jak [8,8,8,8,8,8]|Brak/Poziomy|
Wszystkie 4 właściwości należy ustawić za pomocą TiffOptions, aby zapisać jakikolwiek format obrazu w formacie Tiff. Przy użyciu różnych kombinacji niektóre przeglądarki (w tym Widok zdjęć systemu Windows) mogą odmówić renderyzacji obrazu wynikowego ze względu na ograniczone wsparcie, jakie oferują. W takim przypadku wybierz inną przeglądarkę do testów.
### **Predefiniowane ustawienia dla klasy TiffOptions**
Aby ułatwić użytkownikom i uniknąć błędnej konfiguracji instancji Tiffoptions, interfejs API Aspose.PSD dla Javy udostępnia inny konstruktor, który przyjmuje parametr typu TiffExpectedFormat. W zależności od wybranej wartości z wyliczenia TiffExpectedFormat, API automatycznie konfiguruje wszystkie obowiązkowe właściwości dla instancji Tiffoptions w celu uzyskania pożądanych rezultatów. Przed przystąpieniem do kodu przykładowego, poniżej jest lista pól TiffExpectedFormat i ich szczegóły, aby lepiej zrozumieć sposób użycia.



- TiffExpectedFormat.Default: Ustawienie pola na Default działa podobnie jak domyślny konstruktor klasy Tiffoptions, bez ustawionej kompresji i ustawionej liczby Bitów na 1 w celu uzyskania czarno-białego wyniku. Zaleca się używanie tego pola, gdy inne właściwości specyficzne dla formatu mają być ustawione ręcznie zgodnie z pożądanymi rezultatami.
- TiffExpectedFormat.TiffCcitRle: Specyficzne dla kodowania RLE podczas zapisywania wyniku w formacie TIFF z 1 bitem na piksel (czarno-biały).
- TiffExpectedFormat.TiffCcittFax3: Specyficzne dla kodowania CCITT Fax3 podczas zapisywania wyniku w formacie TIFF z 1 bitem na piksel (czarno-biały).
- TiffExpectedFormat.TiffCcittFax4: Specyficzne dla kodowania CCITT Fax4 podczas zapisywania wyniku w formacie TIFF z 1 bitem na piksel (czarno-biały).
- TiffExpectedFormat.TiffDeflateBW: Specyficzne dla kompresji Deflate podczas zapisywania wyniku w formacie TIFF z 1 bitem na piksel (czarno-biały).
- TiffExpectedFormat.TiffDeflateRGB: Specyficzne dla kompresji Deflate podczas zapisywania wyniku w formacie TIFF w kolorze RGB.
- TiffExpectedFormat.TiffJpegRGB: Specyficzne dla kompresji JPEG podczas zapisywania wyniku w formacie TIFF w kolorze RGB.
- TiffExpectedFormat.TiffJpegYCBCR: Specyficzne dla kompresji JPEG podczas zapisywania wyniku w formacie TIFF w kolorze YCBCR.
- TiffExpectedFormat.TiffLzwBW: Specyficzne dla kompresji LZW podczas zapisywania wyniku w formacie TIFF z 1 bitem na piksel (czarno-biały).
- TiffExpectedFormat.TiffLzwRGB: Specyficzne dla kompresji LZW podczas zapisywania wyniku w formacie TIFF w kolorze RGB.
- TiffExpectedFormat.TiffLzwRGBA: Specyficzne dla kompresji LZW podczas zapisywania wyniku w formacie TIFF w kolorze RGBA (kolor z przezroczystością).
- TiffExpectedFormat.TiffNoCompressionBW: Specyficzne dla niekompresowanego formatu TIFF podczas zapisywania wyniku z 1 bitem na piksel (czarno-biały).
- TiffExpectedFormat.TiffNoCompressionRGB: Specyficzne dla niekompresowanego formatu TIFF podczas zapisywania wyniku w kolorze RGB.
- TiffExpectedFormat.TiffNoCompressionRGBA: Specyficzne dla niekompresowanego formatu TIFF podczas zapisywania wyniku w kolorze RGBA (kolor z przezroczystością).



Poniższy fragment kodu wyjaśnia użycie pól TiffExpectedFormat podczas tworzenia instancji klasy Tiffoptions.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Wsparcie dla kompresji Deflate i Adobe Deflate**
Format pliku TIFF (Tagged Image File Format) obsługuje różne rodzaje kompresji, przy czym typ kompresji przechowywany jest jako tag (wartość całkowita) w pliku. Jedną z takich metod kompresji jest Adobe Deflate (wcześniej znany jako Deflate). Interfejs API Aspose.PSD dla Javy obsługuje tę metodę kompresji do eksportowania i tworzenia obrazów TIFF.
### **Zapisywanie obrazu w formacie TIFF z kompresją Deflate**
Konwertowanie wczytanych obrazów na TIFF z kompresją Deflate/Adobe Deflate jest proste, jak poniżej.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Tworzenie obrazu TIFF z kompresją Adobe Deflate**
Poniższy przykład demonstruje użycie interfejsu API Aspose.PSD dla Javy do tworzenia obrazu od podstaw za pomocą metody kompresji Adobe Deflate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **Kompresja obrazów TIFF**
Interfejs API Aspose.PSD dla Javy może być używany do konwertowania obrazów PSD do formatu obrazu TIFF i zmiany kompresji wynikowego obrazu TIFF. API może również być używany do przechowywania różnych obrazów jako ramek w obrazie TIFF do celów archiwizacji, zachowując kompresję obrazów na najniższym poziomie danych. Kompresja obrazów powinna być przeprowadzana przez zmniejszenie rozmiaru danych źródłowych, niezależnie od użytego algorytmu kompresji. Aby osiągnąć najlepszy współczynnik kompresji, można użyć przestrzeni kolorów indeksowanych. Poniższy kod zapewnia najlepszą kompresję, używając tylko 16 kolorów indeksowanych i algorytm kompresji LZW, jednak kolory źródłowe są delikatnie rozmyte.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
