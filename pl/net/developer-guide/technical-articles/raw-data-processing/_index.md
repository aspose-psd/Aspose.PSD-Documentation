---
title: Przetwarzanie surowych danych
type: docs
weight: 50
url: /pl/net/przetwarzanie-surowych-danych/
---

## **Przetwarzanie surowych danych**
Aby poprawić wydajność interfejsu API Aspose.PSD, wprowadziliśmy metodę przetwarzania surowych danych w wersji 2.4.0. Obecnie przetwarzanie surowych danych jest używane wewnętrznie i posiada zewnętrzne API, dzięki czemu może być używane z zewnątrz biblioteki w celu poprawy ogólnej wydajności. Czasami przetwarzanie staje się nieco skomplikowane i wymaga wyjaśnień. Aktualnie przetwarzanie surowych danych jest dostępne tylko dla formatu BMP.

Aby pomóc programistom w uzyskaniu najlepszych wyników, interfejs API Aspose.PSD udostępnia system przetwarzania surowych danych, który posiada zewnętrzne API do dostosowywania. Programiści wywołują serię metod [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) oraz [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata), aby korzystać z przetwarzania surowych danych. Te metody wymagają określenia pożądanego formatu surowych danych za pomocą klasy [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings). Klasa RawDataSettings pozwala programistom określić dowolny format surowych danych. Jednakże, aby osiągnąć najlepszą wydajność, należy używać formatu surowych danych, w którym dane są przechowywane. Klasa RawDataSettings zdefiniowana w klasie [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) pomaga określić format surowych danych obrazu [data format](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat). Przekazując instancję RawDataSettings do metody LoadRawData, dane są zwracane w nienaruszonym stanie, bez stosowania jakiejkolwiek konwersji, co może poprawić wydajność. Z kolei, należy zadbać o wszystkie możliwe układy formatów surowych danych, co czasami może być nieco skomplikowane.

Aby uprościć proces obsługi, kosztem pewnej kary dla wydajności, można określić pożądane ustawienia RawDataSettings, tworząc i inicjalizując klasę z pożądanymi ustawieniami surowych danych. Istnieją przypadki, kiedy niemożliwe jest zwrócenie surowych danych w określonym formacie (na przykład konwersja z przestrzeni kolorów CMYK na RGB nie jest dostępna w wersji 2.4.0). Ponadto, mogą wystąpić scenariusze, w których przetwarzanie surowych danych nie jest dostępne w ogóle dla formatu obrazu. Aby określić, czy można użyć rodzin metod LoadRawData i SaveRawData, należy zapytać o właściwość [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable).
### **Wgląd**
Dla formatu pikseli RGB [pixel data format](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) dostępne są formaty surowych danych indeksowane (z paletą) i oparte na RGB. Indeksowane formaty surowych danych zawierają indeksy wpisów palety w zakresie od 0 do (2^liczba bitów - 1). Pozostałe formaty surowych danych są oparte na RGB. Podczas ładowania surowych danych, należy upewnić się, że jest wystarczająca ilość bajtów do ładowania danych, w przeciwnym razie zostanie zgłoszony odpowiedni wyjątek. Możesz oszacować rozmiar tablicy bajtów, mnożąc rozmiar linii przez liczbę wymaganych linii. Rozmiar linii może się różnić i zależy od formatu przechowywania surowych danych.

Aby osiągnąć najlepszą wydajność, zawsze używaj rozmiaru linii surowych danych równego wartości właściwości [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize). Jednakże czasami może być konieczne dodanie dodatkowego wypełnienia do wierszy surowych danych lub jego zmniejszenie, przypadku czym można użyć innego rozmiaru linii. Jeśli wymagany jest podzbiór prostokąta granicznego obrazu, należy uwzględnić przesunięcia bitów, które mogą wystąpić dla indeksowanych formatów pikseli RGB. Na przykład, rozważmy obraz o wymiarach 100x100 pikseli i formacie surowych danych z 1 bitem na piksel. Chcesz załadować prostokąt surowych danych o położeniu (7,0) i wymiarach (2,1), czyli mówiąc prościej, wymagasz 2 pikseli zaczynając od x=7 i y=0. W tym przypadku otrzymasz następujący układ danych:




![todo:image_alt_text](raw-data-processing_1.png)

Oznacza to, że otrzymasz 2 bajty, gdzie pierwszy bajt zawiera 7 niechcianych pikseli, następnie 1 pożądany piksel, a drugi bajt zawiera 1 pożądany piksel i 7 niechcianych pikseli. Można zadać pytanie, dlaczego nie przesuniemy danych i nie umieścimy tych 2 pikseli w jednym bajcie? Odpowiedź jest prosta: aby utrzymać wysoką wydajność. Wszystkie wewnętrzne przetwarzanie zwykle odbywa się z danymi zaczynającymi się od pierwszego piksela i kończącymi się na ostatnim dostępnym pikselu. Istnieją rzadkie sytuacje, gdy jest wymagany podzbiór pikseli. Ponadto, nie mamy pojęcia, jak te piksele będą przetwarzane później, więc przesunięcie obniży wydajność i sprawi, że kod będzie niepotrzebnie skomplikowany. Zawsze oszacuj odpowiedni bit (nie trzeba określać odpowiedniego bajtu, ponieważ dane zawsze są przesyłane z wypełnionym pierwszym bajtem), od którego zaczynają się wymagane piksele. Aby obliczyć odpowiedni bit, można użyć prostego wzoru: (rect.Left * liczba bitów) % 8.
### **Konwersja kolorów indeksowanych RGB**
Aby uzyskać jak najwyższą wydajność, zawsze używaj tych samych ustawień surowych danych źródłowych i docelowych, formatów pikseli i rozmiarów linii. Czasami jednak może być konieczna konwersja danych. Na przykład można załadować obraz RGB z 1 bitem na piksel i zapisać go z 2 bitami na piksel, lub załadować obraz RGB z 4 bitami na piksel i zmniejszyć jego zakres kolorów do 2 bitów na piksel. W obu przypadkach należy zastosować konwersję kolorów. Konwersja obrazów indeksowanych RGB może być czasami trudna i nie można jej wykonać bez odpowiednich ustawień. Musimy określić, jak zakres kolorów źródłowych jest mapowany na przestrzeń kolorów docelowych. Aby wykonać to zadanie, mamy różne [tryby](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods):

- Mapowanie palety (DitheringMethods.PaletteConversion)
- Mapowanie surowych danych (DitheringMethods.PaletteIgnore)
- Konwersja niestandardowa (DitheringMethods.CustomConverter)

Gdy używane jest mapowanie palety, przestrzeń kolorów źródłowa stara się dopasować do przestrzeni kolorów docelowej jak najdokładniej. Na przykład, załóżmy, że mamy obraz z 4 bity, zawierający następujące kolory:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

Obraz źródłowy wygląda następująco:



![todo:image_alt_text](raw-data-processing_2.png)

A następnie konwertujemy obraz 4 bitowy na obraz 1 bitowy, z wykorzystaniem zdefiniowanych kolorów palety:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

W trybie konwersji palety konwerter odczytuje kolor źródłowy i określa indeks docelowy, korzystając z metody [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) palety docelowej. Wartość własności [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) jest używana, gdy metoda GetNearestColorIndex palety zwróci indeks spoza zakresu. Ta konwersja zamienia kolory źródłowe na najbliższe kolory docelowe pod względem wartości intensywności. Obraz docelowy pasuje do obrazu źródłowego jak najdokładniej. Możesz zobaczyć następujący wynik:


![todo:image_alt_text](raw-data-processing_3.png)

W trybie mapowania surowych danych jest używany inny scenariusz. Palety kolorów źródłowej i docelowej są po prostu ignorowane, a indeksy źródłowe są odwzorowywane na indeksy docelowe. Gdy znaleziona zostanie wartość, którą nie można odwzorować w zakresie docelowym (gdy zmniejszane są bity), używana jest wartość właściwości RasterImage.RawFallbackIndex. Wartość domyślna to 0 i zostanie odwzorowana na pierwszy kolor w palecie docelowej. Jeśli wartość tej właściwości znajduje się poza zakresem docelowym, zostanie zgłoszony odpowiedni wyjątek. Powoduje to mniej przewidywalne wyniki, co można zobaczyć na poniższym obrazie:


![todo:image_alt_text](raw-data-processing_4.png)

Tryb konwersji palety jest bardziej poprawnym rozwiązaniem dla problemu mapowania kolorów, ale zajmuje trochę więcej czasu na zakończenie, ponieważ obliczenia muszą być wykonywane w celu oszacowania poprawnego mapowania palet. (Zazwyczaj istnieje bardzo mała różnica w wydajności między dwoma metodami.) Z drugiej strony, tryb mapowania surowych danych działa nieco szybciej i może być używany do bardziej przybliżonej konwersji kolorów, gdy dokładne mapowanie kolorów nie jest tak istotne. Istnieją przypadki, kiedy paleta kolorów źródłowych jest ograniczona i można ją bezpiecznie przekonwertować na mniejszą liczbę bitów, ponieważ dodatkowe bity i tak nie są używane.

Aby korzystać z któregokolwiek z tych podejść, należy użyć właściwości RawDitheringMethod klasy RasterImage. Domyślnie jest ona ustawiona na metodę konwersji palety, aby uzyskać najbardziej atrakcyjne wyniki. Możesz zmienić tę właściwość przed jakąkolwiek konwersją (na przykład podczas zapisywania obrazu do strumienia). Należy pamiętać, że metody mieszania pominięcia palety i konwersji palety nie będą miały miejsca, jeśli obraz został załadowany i zmieniono niektóre z oryginalnych danych pikseli, ponieważ nowe dane trafiają do pamięci podręcznej, a pamięć podręczna przechowuje dane w maksymalnie dostępnym formacie 32ARGB (z wersji 2.4.0, podlegając zmianie). Ten format jest używany do pokonania problemów z możliwymi różnymi zakresami kolorów dla obrazów załadowanych i zapisanych. Ponadto metody mieszania za pomocą pominięcia palety i konwersji palety nie będą uwzględnione, gdy obraz zostanie załadowany w trybie RGB i przekonwertowany na tryb indeksowany lub odwrotnie.
### **Własne konwertery kolorów**
Czasami standardowe podejście do konwersji kolorów jest niewystarczające. Możesz chcieć użyć niestandardowego algorytmu, aby uzyskać pełną swobodę korzystania z rutyn konwersji kolorów. Gdy formaty pikseli obrazów źródłowych i docelowych są oba formatami indeksowanymi RGB, można użyć prostszego interfejsu, [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter). Należy ustawić właściwość [RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter) na instancję interfejsu IIndexedColorConverter i użyć [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter jako wartość właściwości RawDitheringMethod. W przypadku takiego połączenia, każda konwersja kolorów indeksowanych przechodzi przez określoną instancję IIndexedColorConverter. Niestandardowy konwerter kolorów indeksowanych ma zdefiniowaną następującą metodę:




{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



Metoda FillIndexedtoIndexedMap jest wywoływana, gdy wymagana jest konwersja z obrazu indeksowanego RGB do formatu obrazu indeksowanego RGB (gdy któreś z formatów 1, 2, 4 lub 8 bitów jest przekonwertowane na inne). Tablica map ma długość wszystkich możliwych liczb wpisów formatu źródłowego. Należy wypełnić tę tablicę dla odwzorowania wpisu palety kolorów źródłowych na wpis palety docelowej. Należy pamiętać, że wartość indeksu docelowego mieści się w zakresie od 0 do (liczba bitów - 1), w przeciwnym razie zostanie zgłoszony odpowiedni wyjątek.

Jeśli wymagana jest bardziej niestandardowa konwersja kolorów, właściwość [Raster