---
title: Manipulowanie obrazami JPEG
type: docs
weight: 30
url: /pl/net/manipulowanie-obrazami-jpeg/
---

## **Używanie klasy ExifData do odczytywania i modyfikowania tagów EXIF w plikach JPEG**
Prawie wszystkie aparaty cyfrowe (w tym smartfony), skanery i inne systemy obsługujące obrazy zapisują obrazy z informacją EXIF (Exchangeable Image File). Ustawienia aparatu oraz informacje o scenie są rejestrowane przez aparat do pliku obrazu. Dane EXIF zawierają także informacje o czasie naświetlania, dacie i godzinie zrobienia zdjęcia, ogniskowej, kompensacji ekspozycji, wzorze pomiaru i o użyciu lampy błyskowej. Interfejsy API Aspose.Imaging umożliwiają wydobycie informacji EXIF z danego obrazu w sposób łatwy i prosty. Programiści mogą również pisać dane EXIF do obrazów lub modyfikować istniejące informacje zgodnie z własnymi potrzebami. Aspose.PSD udostępnia klasę [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) do odczytywania, pisania i modyfikowania danych EXIF, natomiast przestrzeń nazw [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) zawiera odpowiednie enumeracje używane w tym procesie.
### **Odczytywanie danych EXIF**
Interfejsy API Aspose.PSD umożliwiają odczytywanie danych EXIF z danego obrazu. Poniższe kroki ilustrują sposób użycia klasy ExifData do odczytywania informacji EXIF z obrazu.

- Załaduj obraz PSD za pomocą metody fabrycznej Load.
- Znajdź miniaturę Jpeg wśród zasobów PSD.
- Wydobądź instancję klasy ExifData.

Pobierz wymagane informacje i wypisz je na konsoli.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Alternatywnie programiści mogą również uzyskać konkretne informacje za pomocą poniższego fragmentu kodu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Pisanie i modyfikowanie danych EXIF**
Za pomocą interfejsów API Aspose.PSD programiści mogą pisać nowe informacje EXIF i modyfikować istniejące dane EXIF obrazu. Obie procesy (Pisanie i Modyfikowanie) wymagają wczytania obrazu i uzyskania danych EXIF w instancji klasy ExifData. Następnie można uzyskać dostęp do właściwości udostępnianych przez klasę ExifData i ustawić je zgodnie z potrzebami. Należy pamiętać, że obrazy przeznaczone do modyfikacji powinny być obrazami Jpeg lub Tiff, które zazwyczaj są miniaturami PSD. Przykładowy kod demonstrujący sposób użycia wygląda następująco:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Wyciąganie miniatur z zasobów PSD**
Miniatury to zmniejszone wersje obrazów, służące do wyświetlania istotnej części obrazu zamiast całej klatki. Niektóre pliki obrazów (szczególnie te zrobione aparatem cyfrowym) zawierają obraz miniatury osadzony w pliku. Interfejs API Aspose.PSD pozwala na wyciąganie miniatur z zasobów PSD i zapisanie ich oddzielnie na dysku. Zasoby miniatur zawierają właściwość ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail), która umożliwia pobranie danych miniatury. Poniższy fragment kodu pokazuje, jak z niej skorzystać.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Skorzystaj z powyższej metody, aby zapisać miniaturę w innych obsługiwanych formatach plików. Jeśli chcesz wyeksportować dane miniatury do innych formatów obrazów, takich jak BMP i PNG, proszę skorzystaj z innych opcji eksportu obrazu.


### **Wyciąganie miniatur z segmentów JFIF**
Jest także możliwe wydobycie miniatur z segmentu ExifData lub JFIF z zasobów miniatur PSD. Poniższy kod pokazuje, jak wykonać wyciąganie danych miniatury z segmentu JFIF lub ExifData:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Skorzystaj z powyższej metody, aby zapisać miniaturę w innych obsługiwanych formatach plików. Jeśli chcesz wyeksportować dane miniatury do innych formatów obrazów, takich jak BMP i PNG, proszę skorzystaj z innych opcji eksportu obrazu.
### **Dodawanie miniatury do segmentu JFIF**
Poniższy fragment kodu demontruje, jak skorzystać z właściwości JFIF. Thumbnail, aby dodać obraz miniatury do segmentu JFIF załadowanego obrazu PSD.


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Obrazy miniatur wraz z innymi danymi segmentu nie mogą zajmować więcej niż 65 545 bajtów ze względu na specyfikacje formatu JPEG. W przypadkach, gdy duże obrazy mają zostać użyte jako miniatury, może wystąpić wyjątek.


### **Dodawanie miniatury do segmentu EXIF**
Poniższy fragment kodu demontruje, jak wykorzystać właściwość ExifData.Thumbnail, aby dodać obraz miniatury do segmentu EXIF załadowanego obrazu PSD.


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


W tym przypadku interfejsu API Aspose.PSD nie jest w stanie oszacować wymiarów obrazu miniatury, ale może sprawdzić rozmiar całego segmentu danych EXIF. Nie może on być większy niż 65 535 bajtów.
## **Używanie klasy JpegExifData do odczytywania i modyfikowania tagów EXIF w obrazach Jpeg**
Interfejsy API Aspose.PSD udostępniają klasę [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata), która jest przeznaczona wyłącznie dla formatów obrazów Jpeg do pobierania i aktualizacji informacji EXIF. Ten artykuł demonstruje sposób użycia klasy JpegExifData do osiągnięcia tego samego celu. Klasa Aspose.PSD.Exif.JpegExifData służy jako kontener danych EXIF dla obrazów Jpeg i umożliwia pobieranie standardowych tagów EXIF dla obrazów Jpeg, jak pokazano poniżej:



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Kompletna lista tagów EXIF**
Powyższy fragment kodu odczytuje kilka tagów EXIF za pomocą właściwości udostępnionych przez klasę Aspose.PSD.Exif.JpegExifData. Kompletna lista tych właściwości jest dostępna tutaj. Poniższy kod odczyta wszystkie tagi EXIF za pomocą klasy [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0).


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Automatyczna korekcja orientacji obrazów JPEG**


Zdjęcia mogą zostać zrobione aparatem obróconym o 90°, 180°, 270° lub bez żadnego obrotu (normalna orientacja). Większość aparatów cyfrowych przechowuje informacje o orientacji razem z danymi obrazu jako tagi EXIF obrazów JEPG. Te informacje można wykorzystać do automatycznej korekcji orientacji obrazów. Interfejsy API Aspose.PSD udostępniają metodę AutoRotate dla klasy JpegImage do automatycznej korekcji orientacji obrazów JPEG. Oto jak można użyć metody AutoRotate z API Aspose.PSD dla .NET.


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Wsparcie dla JPEG-LS z modelami kolorów CMYK i YCCK**


Interfejs API Aspose.PSD dla .NET udostępnia wsparcie dla modeli kolorów CMYK i YCCK z formatem JPEG-LS. Poniższy fragment kodu demonstruje, jak skorzystać z tego wsparcia dla JPEG-LS.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Wsparcie dla obrazów JPEG-LS z 2-7 bitami na próbkę**


Interfejs API Aspose.PSD dla .NET udostępnia wsparcie dla obrazów JPEG-LS z 2-7 bitami na próbkę. Poniższy fragment kodu demonstruje, jak skorzystać z tego wsparcia dla JPEG-LS.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Ustawianie typu koloru i typu kompresji dla obrazów JPEG**




Interfejs API Aspose.PSD dla .NET udostępnia wsparcie dla typu koloru i typu kompresji oraz ustawia je jako odcienie szarości i progresywne dla obrazów JPEG. Poniższy fragment kodu demonstruje, jak skorzystać z tego wsparcia.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





Poniższy fragment kodu demonstruje, jak skorzystać z właściwości ExifData.Thumbnail, aby dodać obraz miniatury do segmentu EXIF załadowanego obrazu PSD.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

W tym przypadku interfejs API Aspose.PSD nie jest w stanie oszacować wymiarów obrazu miniatury, ale może sprawdzić rozmiar całego segmentu danych EXIF. Nie może on być większy niż 65 535 bajtów.
