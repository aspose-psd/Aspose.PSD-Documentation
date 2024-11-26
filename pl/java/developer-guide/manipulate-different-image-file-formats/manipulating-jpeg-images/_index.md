---
title: Manipulowanie obrazami JPEG
type: docs
weight: 20
url: /pl/java/manipulowanie-obrazami-jpeg/
---

## **Używanie klasy ExifData do odczytu i modyfikacji metadanych EXIF w plikach JPEG**


Prawie wszystkie aparaty cyfrowe (w tym smartfony), skanery i inne systemy obsługi obrazów zapisują obrazy z informacjami EXIF (Exchangeable Image File). Ustawienia kamery i informacje o scenie są zapisywane przez aparat do pliku obrazu. Dane EXIF obejmują także wartości takie jak prędkość migawki, data i czas zrobienia zdjęcia, ogniskowa, kompensacja ekspozycji, wzorzec pomiaru i informacje o użyciu lampy błyskowej. Interfejsy API Aspose.Imaging umożliwiają wydobycie informacji EXIF z danego obrazu w bardzo łatwy i prosty sposób. Programiści mogą także pisać dane EXIF do obrazów lub modyfikować istniejące informacje zgodnie z ich potrzebami. Aspose.Imaging dostarcza klasę ExifData do odczytu, zapisu i modyfikacji danych EXIF, natomiast przestrzeń nazw Aspose.PSD.Exif.Enums zawiera odpowiednie enumeracje używane w procesie.
### **Odczytywanie danych EXIF**
Interfejsy API Aspose.PSD umożliwiają odczytywanie danych EXIF z danego obrazu. Poniższe kroki przedstawiają korzystanie z klasy ExifData do odczytywania informacji EXIF z obrazu.

- Załaduj obraz PSD za pomocą metody fabrycznej Load.
- Znajdź miniature JPEG wśród zasobów PSD.
- Wyodrębnij instancję klasy ExifData.

Pobierz wymagane informacje i wypisz je w konsoli.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Alternatywnie, programiści mogą także uzyskać konkretne informacje, korzystając z poniższego fragmentu kodu.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Pisanie i modyfikowanie danych EXIF**
Za pomocą interfejsów API Aspose.PSD, programiści mogą pisać nowe informacje EXIF i modyfikować istniejące dane EXIF w obrazie. Zarówno proces pisania, jak i modyfikacji wymaga wczytania obrazu i uzyskania danych EXIF do instancji klasy ExifData. Następnie można uzyskać dostęp do właściwości udostępnionych przez klasę ExifData i je odpowiednio ustawić. Należy pamiętać, że obrazy do modyfikacji powinny być obrazami JPEG lub TIFF, które zazwyczaj są miniaturami PSD. Kod przykładowy demonstrujący sposób użycia jest podany poniżej:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Wyodrębnianie miniatur z zasobów PSD**
Miniatury to zredukowane wersje obrazów, używane do wyświetlania znacznej części obrazu zamiast pełnej ramki. Niektóre pliki obrazów (szczególnie te zrobione aparatem cyfrowym) mają zagnieżdżony obraz miniatury w pliku. Interfejs API Aspose.PSD pozwala na wyodrębnienie miniatur z zasobów PSD i ich oddzielne zapisanie na dysku. Zasoby miniatur zawierają właściwość ExifData.Thumbnail, która pozwala na pobranie danych dotyczących miniatury. Poniższy fragment kodu demonstruje, jak z niej skorzystać.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Zastosuj podejście omówione powyżej, aby zapisać miniaturę w innych obsługiwanych formatach plików. Jeśli chcesz wyeksportować dane miniatury do innych formatów obrazów, takich jak BMP & PNG, skorzystaj z innych opcji eksportu obrazów.
### **Wyodrębnianie miniatur z segmentów JFIF**
Istnieje także możliwość wyodrębnienia miniatur z segmentu ExifData lub JFIF z zasobów miniatur PSD. Poniższy kod pokazuje, jak przeprowadzić wyodrębnienie danych miniatury z segmentu JFIF lub ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Zastosuj podejście omówione powyżej, aby zapisać miniaturę w innych obsługiwanych formatach plików. Jeśli chcesz wyeksportować dane miniatury do innych formatów obrazów, takich jak BMP & PNG, skorzystaj z innych opcji eksportu obrazów.
### **Dodawanie miniatury do segmentu JFIF**
Poniższy fragment kodu demonstruje, jak użyć właściwości JFIF.Thumbnail do dodania obrazu miniatury do segmentu JFIF załadowanego obrazu PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}


Obrazy miniatur wraz z innymi danymi segmentowymi nie mogą zajmować więcej niż 65 545 bajtów z uwagi na specyfikacje formatu JPEG. W przypadkach, gdy duże obrazy mają być ustawione jako miniatury, może pojawić się wyjątek.


### **Dodawanie miniatury do segmentu EXIF**
Poniższy fragment kodu demonstruje, jak użyć właściwości ExifData.Thumbnail do dodania obrazu miniatury do segmentu EXIF załadowanego obrazu PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}


W tym przypadku interfejs API Aspose.PSD nie jest w stanie oszacować wielkości obrazu miniatury, ale może sprawdzić wielkość całego segmentu danych EXIF. Nie powinna ona przekraczać 65 535 bajtów.
## **Używanie klasy JpegExifData do odczytu i modyfikacji tagów EXIF obrazów JPEG**
Interfejsy API Aspose.PSD zapewniają klasę JpegExifData, która jest przeznaczona wyłącznie do formatów obrazów JPEG w celu pobierania i aktualizowania informacji EXIF. Ten artykuł demonstrowany jest sposób użycia klasy JpegExifData do osiągnięcia tego samego efektu. Klasa Aspose.PSD.Exif.JpegExifData służy jako kontener danych EXIF dla obrazów JPEG i umożliwia pobranie standardowych tagów EXIF JPEG, jak pokazano poniżej:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Pełna lista tagów EXIF**
Powyższy fragment kodu odczytuje kilka tagów EXIF, korzystając z właściwości oferowanych przez klasę Aspose.PSD.Exif.JpegExifData. Pełna lista tych właściwości jest dostępna tutaj. Poniższy kod odczytuje wszystkie tagi EXIF, korzystając z klasy System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Automatyczna korekcja orientacji obrazów JPEG**
Zdjęcia mogą być zrobione kamerą obróconą o 90°, 180°, 270° lub bez obrotu (normalna orientacja). Większość aparatów cyfrowych przechowuje informacje o orientacji wraz z danymi obrazu jako tagi EXIF obrazów JPEG. Te informacje mogą być wykorzystane do automatycznego obracania obrazów w celu poprawy orientacji. Interfejsy API Aspose.PSD zapewniają metodę AutoRotate dla klasy JpegImage do automatycznej korekcji orientacji obrazów JPEG. Oto jak można skorzystać z metody AutoRotate z Aspose.PSD dla interfejsu Java.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Wsparcie dla JPEG-LS z CMYK i YCCK**


Interfejs API Aspose.PSD dla Javy zapewnia obsługę modeli kolorów CMYK i YCCK z JPEG-LS. Poniższy fragment kodu demonstruje, jak użyć tego wsparcia dla JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}


## **Wsparcie dla obrazów JPEG-LS z wartościami 2-7 bitów na próbkę**


Interfejs API Aspose.PSD dla Javy zapewnia obsługę obrazów JPEG-LS z wartościami 2-7 bitów na próbkę. Poniższy fragment kodu demonstruje, jak skorzystać z tego wsparcia dla JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}


## **Ustawianie typu koloru i typu kompresji dla obrazów JPEG**







Interfejs API Aspose.PSD dla Javy zapewnia wsparcie dla typu koloru i typu kompresji i ustawia je jako skala szarości oraz progresywne dla obrazów JPEG. Poniższy fragment kodu demonstruje, jak skorzystać z tego wsparcia.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}



