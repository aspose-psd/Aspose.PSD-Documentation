---
title: Przetwarzanie surowych danych
type: docs
weight: 70
url: /pl/java/przetwarzanie-surowych-danych/
---

## **Przetwarzanie surowych danych**
Aby poprawić wydajność interfejsu API Aspose.PSD, wprowadziliśmy metodę przetwarzania surowych danych w wersji 2.4.0. Przetwarzanie surowych danych jest teraz używane wewnętrznie i posiada zewnętrzne API, dzięki czemu może być wykorzystywane spoza biblioteki w celu poprawy ogólnej wydajności. Czasami przetwarzanie może być nieco skomplikowane i wymaga wyjaśnień. Obecnie przetwarzanie surowych danych jest dostępne tylko dla formatu BMP.

Aby pomóc programistom uzyskać możliwie najlepszą wydajność, interfejs API Aspose.PSD zapewnia system przetwarzania surowych danych z zewnętrznym API do dostosowania. Programiści wywołują rodziny metod LoadRawData i SaveRawData, aby korzystać z przetwarzania surowych danych. Metody te wymagają również ustawienia żądanego formatu surowych danych za pomocą klasy RawDataSettings. Klasa RawDataSettings pozwala programistom określić dowolny format surowych danych. Aby jednak uzyskać najlepszą wydajność, należy użyć formatu surowych danych, w jakim dane są przechowywane. Klasa RawDataSettings zdefiniowana w klasie RasterImage pomaga określić format surowych danych obrazu. Przekazując instancję RawDataSettings do metody LoadRawData, dane są zwracane bez stosowania konwersji i mogą poprawić wydajność. Z kolei, jeśli chodzi o wszystkie możliwe układy formatów surowych danych, czasami może to być nieco skomplikowane.

Aby uprościć proces obsługi, kosztem pewnej utraty wydajności można określić żądane ustawienia RawDataSettings, inicjalizując klasę z odpowiednimi ustawieniami surowych danych. Istnieją przypadki, gdy nie można zwrócić danych surowych w określonym formacie (na przykład konwersja z przestrzeni kolorów CMYK na RGB nie jest dostępna w wersji 2.4.0). Ponadto mogą wystąpić scenariusze, w których przetwarzanie surowych danych nie jest dostępne w ogóle dla formatu obrazu. Aby sprawdzić, czy można korzystać z rodzin metod LoadRawData i SaveRawData, należy sprawdzić właściwość IsRawDataAvailable.
### **Wnioskowanie**
Dla formatu danych pikseli RGB dostępne są formaty danych surowych indeksowane (oparte na palecie) oraz RGB. Formaty danych surowych indeksowane zawierają indeksy wpisów palety w zakresie od 0 do (2^liczba bitów – 1). Formaty danych surowych indeksowane to 1, 2, 4 i 8 bitów na piksel. Pozostałe są formatami surowych danych opartych na RGB. Podczas ładowania danych surowych, należy upewnić się, że dostępne są odpowiednie bajty do ładowania danych, w przeciwnym razie zostanie zgłoszony odpowiedni wyjątek. Można łatwo oszacować rozmiar tablicy bajtów, mnożąc rozmiar linii przez liczbę wymaganych linii. Rozmiar linii może się różnić i zależy od formatu przechowywania danych surowych.

Aby osiągnąć najlepszą wydajność, zawsze używaj rozmiaru linii surowych danych równego wartości własności RasterImage.RawLineSize. Jednak czasami może być konieczne dodanie dodatkowego marginesu do wierszy danych surowych lub jego zmniejszenie, a w takim przypadku można użyć innego rozmiaru linii. Jeśli wymagany jest podzbiór prostokąta granicznego obrazu, należy wziąć pod uwagę przesunięcia bitowe, które mogą wystąpić dla indeksowanych formatów pikseli RGB. Na przykład załóżmy, że obraz ma wymiary 100x100 pikseli i format surowych danych wynosi 1 bit na piksel. Chcesz załadować prostokąt danych surowych o lokalizacji (7,0) i wymiarach (2,1), czyli inaczej mówiąc, wymagasz 2 pikseli zaczynając od x=7 i y=0. W takim przypadku powinieneś otrzymać następujący układ danych:



![todo:image_alt_text](raw-data-processing_1.png)

Oznacza to, że otrzymujesz 2 bajty, w których pierwszy bajt zawiera 7

 Początkowo niechcianych pikseli, następnie 1 pożądany piksel, a drugi bajt zawiera 1 pożądany piksel, a następnie 7 niechcianych pikseli. Możesz zapytać, dlaczego nie wykonaliśmy przesunięcia danych i umieściliśmy te 2 piksele w jednym bajcie? Odpowiedź jest prosta: aby zachować wysoką wydajność. Całe przetwarzanie wewnętrzne zazwyczaj odbywa się ze wszystkimi danymi począwszy od pierwszego piksela i kończąc na ostatnim dostępnym pikselu. Istnieją rzadkie sytuacje, gdy wymagany jest podzbiór pikseli. Ponadto nie mamy pojęcia, w jaki sposób te piksele zostaną przetworzone później, dlatego przesunięcie obniżyłoby wydajność i sprawiłoby, że kod byłby niepotrzebnie złożony. Zawsze oszacuj odpowiedni bit (nie trzeba określać poprawnego bajtu, ponieważ dane zawsze przychodzą z pierwszym wypełnionym bajtem), na którym zaczynają się żądane piksele. Aby obliczyć odpowiedni bit, można użyć prostego wzoru: (rect.Left * liczba bitów) % 8.
### **Konwersja kolorów RGB indeksowanych**
Aby uzyskać jak największą wydajność, zawsze używaj tych samych ustawień surowych danych źródłowych i docelowych, formatów pikseli i rozmiarów linii. Jednak czasami konieczna może być konwersja danych. Na przykład można załadować obraz z formatem RGB 1 bit na piksel i zapisać go z formatem 2 bity na piksel, lub załadować obraz RGB 4 bitowy i zmniejszyć jego zakres kolorów do 2 bitów na piksel. W obu przypadkach należy zastosować konwersję kolorów. Konwersja obrazów RGB indeksowanych może być czasami skomplikowana i nie może być wykonana bez odpowiednich ustawień. Musimy określić, jak zakres kolorów źródłowych jest mapowany na przestrzeń kolorów docelowych. Aby wykonać to zadanie, mamy do dyspozycji różne tryby:

- Odwzorowanie palety (DitheringMethods.PaletteConversion)
- Odwzorowanie surowych danych (DitheringMethods.PaletteIgnore)
- Konwersja niestandardowa (DitheringMethods.CustomConverter)

W przypadku użycia konwersji paletowej, przestrzeń kolorów źródłowa stara się dopasować do przestrzeni kolorów docelowej jak najbliżej. Na przykład załóżmy, że mamy obraz 4-bitowy z następującymi kolorami:
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

I konwertujemy obraz 4-bitowy na obraz 1-bitowy z poniższymi zdefiniowanymi kolorami palety:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

W trybie konwersji paletowej konwerter odczytuje kolor źródłowy i określa indeks docelowy, używając metody GetNearestColorIndex palety docelowej. Wartość własności RasterImage.RawFallbackIndex jest używana w przypadku, gdy metoda GetNearestColorIndex palety daje indeks poza zakresem. To konwertuje kolory źródłowe na najbliższe kolory docelowe pod względem wartości intensywności. Obraz docelowy pasuje do obrazu źródłowego jak najbliżej. Możesz zobaczyć następujący wynik:



![todo:image_alt_text](raw-data-processing_3.png)

W trybie odwzorowania surowych danych stosowany jest inny scenariusz. Palety kolorów źródłowych i docelowych są po prostu ignorowane, a indeksy źródłowe są odwzorowywane na indeksy docelowe. Gdy odnaleziona zostanie wartość, która nie może być odwzorowana w zakres docelny (gdy liczba bitów jest zmniejszana), wartość własności RasterImage.RawFallbackIndex jest używana. Wartość ta domyślnie wynosi 0 i będzie odwzorowana na pierwszy kolor w palecie docelowej. Jeżeli właściwość ta leży poza zakresem docelowym, zgłoszony zostanie odpowiedni wyjątek. Powoduje to mniej przewidywalne rezultaty, które można pokazać na poniższym obrazie:



![todo:image_alt_text](raw-data-processing_4.png)

Tryb konwersji paletowej jest bardziej poprawnym rozwiązaniem dla problemu odwzorowywania kolorów, ale wymaga nieco więcej czasu na zakończenie, ponieważ trzeba wykonać obliczenia, aby oszacować poprawne odwzorowania palet. (Zazwyczaj istnieje bardzo mała różnica w wydajności między tymi dwoma metodami.) Z drugiej strony tryb odwzorowywania surowych danych działa trochę szybciej i można go stosować do bardziej surowej konwersji kolorów, gdy dokładne odwzorowanie kolorów nie jest tak istotne. Na przykład mogą istnieć przypadki, gdy paleta kolorów źródłowych jest przycięta i można bezpiecznie przekonwertować ją na mniejsze liczby bitów, ponieważ dodatkowe bity i tak nie zostały użyte.

Aby korzystać z któregokolwiek z tych podejść, użyj własności RawDitheringMethod klasy RasterImage. Domyślnie jest ustawiona na metodę konwersji paletowej w celu uzyskania najlepszych wyników wizualnych. Możesz zmienić tę wartość przed jakąkolwiek konwersją (na przykład podczas zapisywania obrazu do strumienia). Należy pamiętać, że metody od ignore i konwersji paletowych nie będą miały miejsca, jeśli załadowano obraz i ponownie zapisano część oryginalnych danych pikseli, ponieważ nowe dane trafiają do pamięci podręcznej, a pamięć podręczna przechowuje dane w maksymalnie dostępnym formacie 32ARGB (od wersji 2.4.0, podlega zmianie). Ten format jest używany do rozwiązania problemów z ewentualnie różnymi zakresami kolorów dla obrazów załadowanych i zapisanych. Ponadto metody ignore i konwersji paletowe nie będą uwzględniane, gdy obraz jest ładowany w trybie RGB i przekonwertowany na tryb indeksowany lub odwrotnie.
### **Niestandardowe konwertery kolorów**
Czasami standardowe podejście do konwersji kolorów nie jest wystarczające. Możesz chcieć użyć niestandardowego algorytmu, aby uzyskać pełną swobodę w użytkowaniu rutyn konwersji kolorów. Gdy formaty pikseli obrazów źródłowych i docelowych są oba formatami RGB indeksowanymi, prostszy interfejs, IIndexedColorConverter, może być używany. Należy ustawić właściwość RasterImage.RawIndexedColorConverter na instancję interfejsu IIndexedColorConverter i użyć wartości właściwości RawDitheringMethod równą DitheringMethods.CustomConverter. Gdy zachodzi ta kombinacja, każda konwersja kolorów indeksowanych przechodzi przez określoną instancję IIndexedColorConverter. Niestandardowy konwerter kolorów indeksowanych ma zdefiniowaną następującą metodę:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



Metoda FillIndexedtoIndexedMap jest wywoływana, gdy wymagana jest konwersja z obrazu RGB indeksowanego na format obrazu RGB indeksowanego (gdy dowolna liczba bitów 1, 2, 4 lub 8 jest konwertowana na siebie). Tablica map ma długość wszystkich możliwych wpisów formatu źródłowego. Należy wypełnić tę tablicę, aby odwzorować wpisy palety kolorów źródłowych na docelowe wpisy palety. Należy zadbać o to, że wartość indeksu docelowego mieści się w zakresie 0..(liczba bitów - 1), w przeciwnym razie zgłoszony zostanie odpowiedni wyjątek.

Jeśli wymagana jest bardziej niestandardowa konwersja kolorów, wartość właściwości RasterImage.RawCustomColorConverter powinna być ustawiona na instancję interfejsu IColorConverter. Właściwość RawCustomColorConverter zawsze zastępuje właściwość RawIndexedColorConverter, gdy obie są ustawione, a konwerter kolorów indeksowanych nie zostanie użyty w takim przypadku. Interfejs IColorConverter ma jedną metodę:



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset);

{{< /highlight >}}



Metoda Convert jest wywoływana za każdym razem, gdy wymagana jest konwersja kolorów. Metoda odbiera surowe dane źródłowe w formacie źródłowym i ma bufor wynikowy do otrzymania skonwertowanego formatu koloru na cel. Bufor docelowy powinien być wystarczający do otrzymania skonwertowanych danych (jeśli wywołanie interfejsu jest wykonywane wewnętrznie przez bibliotekę Aspose.PSD) i powinien zawierać skonwertowane surowe dane po zakończeniu metody. Metoda Convert może być wywoływana kilkakrotnie, a