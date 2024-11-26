---
title: Tworzenie, Otwieranie i Zapisywanie Obrazów
type: docs
weight: 30
url: /pl/net/tworzenie-otwieranie-i-zapisywanie-obrazow/
---

## **Tworzenie Plików Obrazów**
Aspose.PSD dla .NET pozwala programistom tworzyć własne obrazy. Użyj statycznej metody Create wystawionej przez klasę Image, aby utworzyć nowe obrazy. Wszystko, co musisz zrobić, to dostarczyć odpowiedni obiekt jednej z klas z przestrzeni nazw ImageOptions dla wybranego formatu obrazu wyjściowego. Aby utworzyć plik obrazu, najpierw utwórz egzemplarz jednej z klas z przestrzeni nazw ImageOptions. Te klasy określają format obrazu wyjściowego. Poniżej znajdują się niektóre klasy z przestrzeni nazw ImageOptions (należy zauważyć, że obecnie obsługiwane są tylko formaty plików PSD):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) ustawia opcje tworzenia pliku PSD. Pliki obrazów można tworzyć, ustawiając ścieżkę wyjściową lub ustawiając strumień.
### **Tworzenie poprzez Ustawienie Ścieżki**
Utwórz PsdOptions z przestrzeni nazw [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) i ustaw różne właściwości. Najważniejszą właściwością do ustawienia jest Właściwość Source. Ta właściwość określa, gdzie znajdują się dane obrazu (w pliku lub strumieniu). W poniższym przykładzie źródłem jest plik. Po ustawieniu właściwości przekaż obiekt do jednej z statycznych metod [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) wraz z parametrami szerokości i wysokości. Szerokość i wysokość są zdefiniowane w pikselach.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Tworzenie Za Pomocą Strumienia**
Proces tworzenia obrazu za pomocą strumienia jest taki sam jak w przypadku użycia ścieżki. Jedyną różnicą jest konieczność utworzenia egzemplarza [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) poprzez przekazanie obiektu Stream do jego konstruktora i przypisanie go do właściwości Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Otwieranie Plików Obrazów**
Programiści mogą używać interfejsu API Aspose.PSD dla .NET do otwierania istniejących plików obrazów PSD do różnych celów, takich jak dodawanie efektów do obrazu lub konwertowanie istniejącego pliku do innego formatu. Bez względu na cel, Aspose.PSD udostępnia dwa standardowe sposoby otwierania istniejących plików: z pliku lub ze strumienia.
### **Otwieranie z Dysku**
Otwórz plik obrazu, przekazując ścieżkę i nazwę pliku jako parametr do statycznej metody Load wystawionej przez klasę Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Otwieranie za Pomocą Strumienia**
Czasami obraz, który musimy otworzyć, jest przechowywany jako strumień. W takich przypadkach użyj przeciążonej wersji metody Load. Ta metoda akceptuje obiekt Stream jako argument do otwarcia obrazu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Załaduj Obraz Jako Warstwę**
Ten artykuł demonstruje użycie Aspose.PSD do wczytania obrazu jako warstwy. API Aspose.PSD udostępnia wydajne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD udostępnił metodę AddLayer klasy PsdImage, aby dodać obraz do pliku PSD jako warstwę.

Kroki potrzebne do wczytania obrazu do PSD jako warstwy są tak proste jak poniżej:

- Utwórz egzemplarz obrazu za pomocą klasy PsdImage z określoną szerokością i wysokością.
- Wczytaj plik PSD jako obraz przy użyciu metody fabrycznej Load wystawionej przez klasę Image.
- Utwórz egzemplarz klasy Layer i przypisz do niego warstwę obrazu PSD.
- Dodaj utworzoną warstwę przy użyciu metody AddLayer wystawionej przez klasę PsdImage
- Zapisz wyniki.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Załaduj Obraz Jako Warstwę ze Strumienia**
Ten artykuł demonstruje użycie Aspose.PSD do wczytania obrazu jako warstwy ze strumienia. Aby wczytać obraz ze strumienia, po prostu przekaż obiekt strumienia zawierającego obraz do konstruktora klasy Layer. Dodaj utworzoną warstwę przy użyciu metody AddLayer wystawionej przez klasę PsdImage i zapisz wyniki.


Oto przykładowy kod.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Zapisywanie Plików Obrazów**
Aspose.PSD pozwala tworzyć pliki obrazów od podstaw. Zapewnia również możliwość edycji istniejących plików obrazów. Po utworzeniu lub zmodyfikowaniu obrazu, plik zazwyczaj jest zapisywany na dysk. Aspose.PSD udostępnia metody do zapisywania obrazów na dysk poprzez określenie ścieżki lub użycie obiektu strumienia.
### **Zapisywanie do Dysku**
Klasa Image reprezentuje obiekt obrazu, dlatego ta klasa dostarcza wszystkie narzędzia potrzebne do tworzenia, wczytywania i zapisywania pliku obrazu. Użyj metody Save klasy Image do zapisywania obrazów. Jedna przeciążona wersja metody Save akceptuje lokalizację pliku jako ciąg.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Zapisywanie do Strumienia**
Inna przeciążona wersja metody Save akceptuje obiekt Stream jako argument i zapisuje plik obrazu do strumienia.

Jeśli obraz jest utworzony przez określenie któregokolwiek z CreateOptions w konstruktorze Image, obraz automatycznie jest zapisywany do ścieżki lub strumienia podanego podczas inicjalizacji klasy Image, wywołując metodę Save, która nie przyjmuje żadnych parametrów.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Ustawianie Domyślnej Czcionki do zastąpienia brakujących czcionek**
Programiści mogą użyć interfejsu API Aspose.PSD dla .NET do wczytania istniejących plików obrazów PSD do różnych celów, na przykład, aby ustawić domyślną nazwę czcionki podczas zapisywania dokumentów PSD jako obraz rastrowy (do formatów PNG, JPG i BMP). Ta domyślna czcionka powinna być używana jako zastępstwo dla wszystkich brakujących czcionek (czcionek, które nie zostały znalezione w bieżącym systemie operacyjnym). Po zmodyfikowaniu obrazu, plik zostanie zapisany na dysku.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}
