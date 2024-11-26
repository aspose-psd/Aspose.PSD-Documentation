---
title: Tworzenie, Otwieranie i Zapisywanie Obrazów
type: docs
weight: 30
url: /pl/java/tworzenie-otwieranie-i-zapisywanie-obrazow/
---

## **Tworzenie Plików Obrazów**
Biblioteka Aspose.PSD dla Javy pozwala programistom tworzyć własne obrazy. Użyj statycznej metody Create udostępnionej przez klasę Image, aby utworzyć nowe obrazy. Wszystko, co musisz zrobić, to dostarczyć odpowiedni obiekt jednej z klas z przestrzeni nazw ImageOptions dla pożądanego formatu obrazu wyjściowego. Aby utworzyć plik obrazu, najpierw utwórz wystąpienie jednej z klas z przestrzeni nazw ImageOptions. Te klasy określają format obrazu wyjściowego. Poniżej znajdują się niektóre klasy z przestrzeni nazw ImageOptions (zauważ, że obecnie obsługiwane są tylko rodziny formatów plików PSD):

PsdOptions ustawia opcje tworzenia pliku PSD. Pliki obrazów można tworzyć ustawiając ścieżkę wyjściową lub ustawiając strumień.
### **Tworzenie Poprzez Ustawienie Ścieżki**
Utwórz PsdOptions z przestrzeni nazw ImageOptions i ustaw różne właściwości. Najważniejszą właściwością do ustawienia jest właściwość Source. Ta właściwość określa, gdzie znajdują się dane obrazu (w pliku lub strumieniu). W poniższym przykładzie źródłem jest plik. Po ustawieniu właściwości przekaż obiekt do jednej z metod statycznych Create wraz z parametrami szerokości i wysokości. Szerokość i wysokość są definiowane w pikselach.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Tworzenie Używając Strumienia**
Proces tworzenia obrazu przy użyciu strumienia jest taki sam jak w przypadku użycia ścieżki. Jedyną różnicą jest konieczność utworzenia wystąpienia obiektu StreamSource, przekazując obiekt Stream do jego konstruktora i przypisując go do właściwości Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Otwieranie Plików Obrazów**
Programiści mogą korzystać z interfejsu API Aspose.PSD dla Javy do otwierania istniejących plików obrazów PSD w różnych celach, takich jak dodawanie efektów do obrazu lub konwertowanie istniejącego pliku na inny format. Bez względu na cel, Aspose.PSD udostępnia dwie standardowe metody otwierania istniejących plików: z pliku lub ze strumienia.
### **Otwieranie z Dysku**
Otwórz plik obrazu, przekazując ścieżkę i nazwę pliku jako parametr do metody statycznej Load udostępnionej przez klasę Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Otwieranie za pomocą Strumienia**
Czasami obraz, który musimy otworzyć, jest przechowywany jako strumień. W takich przypadkach użyj przeciążonej wersji metody Load. Ta metoda akceptuje obiekt Stream jako argument do otwarcia obrazu.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Ładowanie Obrazu Jako Warstwy**
Ten artykuł demonstruje wykorzystanie Aspose.PSD do ładowania obrazu jako warstwy. Interfejsy API Aspose.PSD udostępniają efektywne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD udostępnia metodę AddLayer klasy PsdImage do dodawania obrazu do pliku PSD jako warstwy.

Kroki do ładowania obrazu do PSD jako warstwy są tak proste jak poniżej:

- Utwórz wystąpienie obrazu za pomocą klasy PsdImage z określoną szerokością i wysokością.
- Załaduj plik PSD jako obraz, używając metody fabrycznej Load udostępnionej przez klasę Image.
- Utwórz wystąpienie klasy Layer i przypisz warstwę obrazu PSD do niej.
- Dodaj utworzoną warstwę za pomocą metody AddLayer udostępnionej przez klasę PsdImage.
- Zapisz wyniki.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Zapisywanie Plików Obrazów**
Aspose.PSD pozwala tworzyć pliki obrazów od podstaw. Zapewnia również możliwość edycji istniejących plików obrazów. Po utworzeniu lub zmodyfikowaniu obrazu, plik zazwyczaj jest zapisywany na dysku. Aspose.PSD zapewnia metody do zapisywania obrazów na dysku, określając ścieżkę lub używając obiektu strumienia.
### **Zapisywanie na Dysk**
Klasa Image reprezentuje obiekt obrazu, dlatego ta klasa zapewnia wszystkie narzędzia niezbędne do tworzenia, wczytywania i zapisywania pliku obrazu. Użyj metody Save klasy Image do zapisywania obrazów. Jedna przeciążona wersja metody Save akceptuje lokalizację pliku jako string.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Zapisywanie do Strumienia**
Inna przeciążona wersja metody Save akceptuje obiekt Stream jako argument i zapisuje plik obrazu do strumienia.

Jeśli obraz jest tworzony przez określenie któregokolwiek z CreateOptions w konstruktorze Image, obraz automatycznie jest zapisywany do ścieżki lub strumienia dostarczonego podczas inicjalizacji klasy Image przez wywołanie metody Save, która nie przyjmuje żadnych parametrów.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Ustawianie Domyślnej Czcionki Podczas Zastępowania Brakujących Czcionek**
Programiści mogą użyć interfejsu API Aspose.PSD dla Javy do wczytywania istniejących plików obrazów PSD w różnych celach, na przykład ustawienia domyślnej nazwy czcionki podczas zapisywania dokumentów PSD jako obraz rastrowy (w formatach PNG, JPG i BMP). Ta domyślna czcionka powinna być używana jako zamiennik wszystkich brakujących czcionek (czcionek, które nie są znalezione w bieżącym systemie operacyjnym). Po zmodyfikowaniu obrazu, plik zostanie zapisany na dysku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}


