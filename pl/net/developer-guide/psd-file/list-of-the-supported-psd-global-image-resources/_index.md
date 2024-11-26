---
title: Lista obsługiwanych globalnych zasobów obrazów PSD
type: docs
weight: 30
url: /pl/net/lista-obsługiwanych-globalnych-zasobów-obrazów-psd/
---

## **Aspose.PSD obsługuje edycję niskopoziomową zasobów obrazów.**
Lista w pełni obsługiwanych Zasobów obrazów, które można znaleźć w Aspose.PSD .Net [API Reference](https://reference.aspose.com/psd/net)

Zgodnie ze specyfikacją formatu Adobe® Photoshop®: Zasoby obrazu używają kilku standardowych numerów ID, jak pokazano w ID zasobów obrazu. Nie wszystkie formaty plików używają wszystkich ID. Niektóre informacje mogą być przechowywane w innych sekcjach pliku.

Dla tych numerów ID zasobów, które zostały dodane od wersji Photoshop 3.0. wpis wskazuje wersję, w której zostały wprowadzone, np. (*Photoshop 6.0).*

Numer ID zasobu obrazu.

|**ID**|**Opis**|
| :- | :- |
|**Dziesiętny**||
|1000|*(Przestarzałe - tylko Photoshop 2.0)* Liczba kanałów, wierszy, kolumn, głębokości i trybu|
|1001|Rekord informacji o druku menedżera druku Macintosh|
|1002|Informacje o formacie strony Macintosh. Już nie czytane przez Photoshop. *(Przestarzałe)*|
|1003|*(Przestarzałe - tylko Photoshop 2.0)* Tabela kolorów indeksowanych|
|1005|[Struktura ResolutionInfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource).|
|1006|Nazwy kanałów alfa jako seria ciągów Pascala.|
|1007|*(Przestarzałe) Patrz ID 1077 Struktura DisplayInfo*.*|
|1008|Opis jako ciąg Pascala.|
|1009|[Informacje o obramowaniu.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource) Zawiera ustaloną liczbę (2 bajty rzeczywista, 2 bajty ułamek) dla szerokości obramowania oraz 2 bajty dla jednostek obramowania (1 = cale, 2 = cm, 3 = punkty, 4 = piki, 5 = kolumny).|
|1010|[Kolor tła.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Flagi druku. Seria jednobajtowych wartości logicznych: etykiety, znaczniki przycięcia, paski kolorów, znaczniki rejestracyjne, negatyw, odwrócenie, interpolacja, podpis, flagi drukowania.|
|1012|Informacje o skalowaniu odcieni szarości i wielokanałowych|
|1013|[Informacje o skalowaniu kolorów](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Informacje o skalowaniu bi-tonalnym|
|1015|Funkcja przekazania odcieni szarości i wielokanałowych|
|1016|[Funkcje przekazania kolorów](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&amp;linkCreation=true&amp;fromPageId=106204188)|
|1017|Funkcje przekazania bi-tonalne|
|1018|Informacje o obrazie bi-tonalnym|
|1019|Dwa bajty dla efektywnych wartości czerni i bieli w zakresie kropek|
|1020|*(Przestarzałe)*|
|1021|Opcje EPS|
|1022|[Informacje o szybkiej masce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). ID kanału maski szybkiej; 1-bajtowa wartość logiczna wskazująca, czy maska początkowo była pusta.|
|1023|*(Przestarzałe)*|
|1024|[Informacje o stanie warstwy](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource).|
|1025|Ścieżka robocza (niezapisana). Format zasobu ścieżki.|
|1026|[Informacje o grupach warstw](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 bajty na warstwę zawierający identyfikator grupy dla grup przeciągających. Warstwy w grupie mają ten sam identyfikator grupy.|
|1027|*(Przestarzałe)*|
|1028|Rekord IPTC-NAA. Zawiera informacje *File Info....*.|
|1029|Tryb obrazu dla plików w formacie surowym|
|1030|Jakość JPEG. Prywatne.|
|1032|*(Photoshop 4.0) [Informacje o siatce i prowadnicach.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0) [](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[Zasób miniatury](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[dla Photoshopa 4.0](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* tylko|
|1034|*(Photoshop 4.0)* Flaga praw autorskich. Wartość logiczna wskazująca, czy obraz jest chroniony prawami autorskimi.|
|1035|*(Photoshop 4.0)* URL. Uchwyt ciągu tekstowego z adresem zasobu uniform resource locator*.*|
|1036|*(Photoshop 5.0)[Zasób miniatury](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (zastępuje zasób 1033).|
|1037|*(Photoshop 5.0) [Kąt globalny](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 bajty zawierające liczbę całkowitą między 0 a 359, co oznacza globalny kąt oświetlenia dla warstwy efektów. Jeśli nieobecny, zakłada się, że jest równy 30.|
|1038|*(Przestarzałe) Patrz ID 1073 poniżej. (Photoshop 5.0)* Zasób próbek kolorów.|
|1039|*(Photoshop 5.0) [Profil ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. Surowe bajty profilu w formacie ICC (International Color Consortium).*  |
|1040|*(Photoshop 5.0) [Znak wodny](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*.|
|1041|*(Photoshop 5.0) [Profil bez otagowania ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 bajt, który wyłącza obsługę założonego profilu podczas otwierania pliku. 1 = celowo bez otagowania.|
|1042|*(Photoshop 5.0)* Widoczność efektów. 1-bajtowa flaga globalna do pokazywania/ukrywania wszystkich warstw efektów. Obecna tylko wtedy, gdy są ukryte.|
|1043|*(Photoshop 5.0)* Punktowana siatka. 4 bajty dla wersji, 4 bajty dla długości oraz dane o zmiennym wymiarze.|
|1044|*(Photoshop 5.0)[ID specyficzne dla dokumentu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* numer sekwencyjny. 4 bajty: Wartość bazowa, od której będą generowane identyfikatory warstw (lub większa wartość, jeśli istniejące identyfikatory przekraczają już tę wartość). Jego celem jest uniknięcie sytuacji, w której dodajemy warstwy, spłaszczamy, zapisujemy, otwieramy, a następnie dodajemy kolejne warstwy, które kończą się tymi samymi identyfikatorami co pierwszy zestaw.|
|1045|*(Photoshop 5.0) [Nazwy alfa Unicode](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*.|
|1046|*(Photoshop 6.0)* Liczba kolorów zdefiniowanych w tabeli kolorów indeksowanych. 2 bajty.|
|1047|*(Photoshop 6.0)* [Indeks przezroczystości](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource).|
|1049|*(Photoshop 6.0)* [Globalna wysokość.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Kawałki.|
|1051|*(Photoshop 6.0)* Adres URL przepływu pracy.|
|1052|*(Photoshop 6.0)* Przełącz do XPEP. 2 bajty dla wersji głównej, 2 bajty dla wersji podrzędnej, 4 bajty dla licznika. Poniższe jest powtarzane dla liczby: 4 bajty dla rozmiaru bloku, 4 bajty dla klucza, jeśli klucz = *'jtDd'* , to następny jest wartość logiczna dla flagi brudu; w przeciwnym razie jest to 4-bajtowy wpis dla daty modyfikacji.|
|1053|*(Photoshop 6.0)* Identyfikatory alfa.|
|1054|*(Photoshop 6.0)[Lista adresów URL](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*.|
|1057|*(Photoshop 6.0)* [Informacje o wersji](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource).|
|1058|*(Photoshop 7.0)* Dane EXIF 1.|
|1059|*(Photoshop 7.0)* Dane EXIF 3*.*|
|1060|*(Photoshop 7.0)* [Metadane XMP](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). Informacje o pliku jako opis XML.|
|1061|*(Photoshop 7.0)[Skrót podpisu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 bajtów: RSA Data Security, algorytm skrótu MD5|
|1062|*(Photoshop 7.0)[Skala drukowania](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = wyśrodkowane, 1 = dopasowane do rozmiaru, 2 = zdefiniowane przez użytkownika). 4 bajty na lokalizację x (liczba zmiennoprzecinkowa). 4 bajty na lokalizację y (liczba zmiennoprzecinkowa). 4 bajty na skalę (liczba zmiennoprzecinkowa)|
|1064|*(Photoshop CS)* Współczynnik proporcji pikseli[Pixel Aspect Ratio](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource).|
|1065|*(Photoshop CS)* Zestawy warstw.|
|1066|*(Photoshop CS)* Alternatywne kolory bi-tonalne. Ten zasób nie jest odczytywany ani używany przez Photoshop.|
|1067|*(Photoshop CS)* Alternatywne kolory spotowe. Ten zasób nie jest odczytywany ani używany przez Photoshop.|
|1069|*(Photoshop CS2)* [ID wyboru warstwy](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerselectionidsresource)(ów). 2 bajty licznika, po czym dla każdego licznika powtarzają się: 4 bajty identyfikatora warstwy|
|1070|*(Photoshop CS2)* Informacje o tonowaniu HDR|
|1071|*(Photoshop CS2)* Informacje o druku|
|1072|*(Photoshop CS2)* [Włączony identyfikator grup warstw](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 bajt dla każdej warstwy w dokumencie, powtórzony według długości zasobu. UWAGA: Grupy warstw mają znaczniki początkowe i końcowe|
|1073|*(Photoshop CS3)* Zasób próbek kolorów. Patrz także ID 1038 dla starego formatu.|
|1074|*(Photoshop CS3)* Skala pomiarowa.|
|1075|*(Photoshop CS3)* Informacje na temat osi czasu.|
|1076|*(Photoshop CS3)* Ujawnienie arkusza.|
|1077|*(Photoshop CS3) Struktura DisplayInfo* w celu obsługi kolorów zmiennoprzecinkowych. Patrz także ID 1007.|
|1078|*(Photoshop CS3)* Cebulki.|
|1080|*(Photoshop CS4)* Informacje o liczbie.|
|1082|*(Photoshop CS5)* Informacje o druku.|
|1083|*(Photoshop CS5)* Styl druku. Znaczniki drukowania, etykiety, ozdoby, itp.|
|1084|*(Photoshop CS5)* Macintosh NSPrintInfo. Zmienna informacja specyficzna dla systemu operacyjnego dla Macintosh.|
|1085|*(Photoshop CS5)* Windows DEVMODE. Zmienna informacja specyficzna dla systemu operacyjnego dla systemu Windows.|
|1086|*(Photoshop CS6)* Ścieżka pliku automatycznego zapisu.|
|1087|*(Photoshop CS6)* Format automatycznego zapisu.* |
|1088|*(Photoshop CC)* Stan wyboru ścieżki.|
|2000-2997|Informacje o ścieżce (zapisane ścieżki).|
|2999|Nazwa ścieżki przycinania.|
|3000|*(Photoshop CC)* Informacje o ścieżce pochodzenia|
|4000-4999|Zasoby wtyczki. Zasoby dodane przez wtyczkę.|
|7000|Zmienne programu Image Ready. Reprezentacja XML definicji zmiennych|
|7001|Zbiory danych programu Image Ready|
|7002|Domyślny stan zaznaczania programu Image Ready|
|7003|7 stan rozszerzony rollover programu Image Ready|
|7004|Stan rozszerzony rollover programu Image Ready|
|7005|Ustawienia warstw zapisywane programem Image Ready|
|7006|Wersja programu Image Ready|
|8000|*(Photoshop CS3)* Przepływ pracy Lightroom, jeśli dokument jest w trakcie przepływu pracy Lightroom.|
|10000|[Informacje o flagach druku](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printflagsresource).|


Aspose.PSD obsługuje niektóre z tych zasobów. Jeśli zasób nie ma własnej klasy, można użyć [UnknownResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unknownresource) z As