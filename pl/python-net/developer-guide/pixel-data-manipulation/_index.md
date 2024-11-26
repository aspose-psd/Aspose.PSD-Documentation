---
title: Modyfikacja danych pikseli za pomocą Aspose.PSD dla Pythona
weight: 100
type: docs
description: Przykład bezpośredniej i szybkiej aktualizacji surowych danych pikseli za pomocą interfejsu API Pythona PSD
keywords: [edycja pikseli, edycja psd, edycja warstwy, modyfikacja danych surowych, edycja danych psd, api psd, python, przykład kodu]
url: pl/python-net/modyfikacja-danych-pikseli/
---

## **Wstęp**
Aspose.PSD to potężna biblioteka, która umożliwia pracę z plikami Adobe Photoshop (PSD) w języku Python. W tym artykule przeanalizujemy, jak manipulować danymi pikseli w pliku PSD za pomocą Aspose.PSD.

## **Opis**
Przedstawiony kod demonstruje, jak utworzyć plik PSD, dodać nową warstwę dla niego, a następnie manipulować danymi pikseli bezpośrednio, zapisując zmodyfikowany obraz.

Importowanie wymaganych modułów: Pierwszym krokiem jest importowanie niezbędnych modułów. Importujemy moduł BytesIO z biblioteki io oraz klasy PsdImage i Layer z odpowiednio modułów aspose.psd.fileformats.psd i aspose.psd.fileformats.psd.layers.

Następnie definiujemy ścieżki plików wejściowych i wyjściowych.

Otwieranie pliku wejściowego jako strumień: Otwieramy plik wejściowy jako strumień za pomocą funkcji open i trybu "rb". Argument buforowania jest ustawiony na 0, aby wyłączyć buforowanie. Zawartość pliku jest odczytywana do strumienia BytesIO, a strumień jest ustawiany na początek za pomocą stream.seek(0).

Tworzymy obiekt warstwy PSD, przekazując strumień do konstruktora klasy Layer.

Tworzymy nowy obraz PSD, korzystając z konstruktora klasy PsdImage i podając szerokość i wysokość warstwy jako argumenty.

Przypisujemy warstwę do właściwości layers obrazu PSD za pomocą operatora przypisania (=).

Aby manipulować danymi pikseli, najpierw wczytujemy piksele ARGB32 z warstwy za pomocą metody load_argb_32_pixels. Wynik przechowujemy w zmiennej pixels.

Następnie definiujemy zakres indeksów (pixelsRange) na podstawie długości tablicy pixels. Iterujemy po indeksach i sprawdzamy, czy indeks jest podzielny przez 5. Jeśli tak, ustawiamy wartość piksela dla tego indeksu na 500000. Chcemy stworzyć pewien wzór powtarzający się. Możesz zmieniać dane pikseli według własnego uznania.

Następnie zapisujemy zmodyfikowane dane pikseli z powrotem do warstwy, korzystając z metody save_argb_32_pixels.

W końcu zapisujemy obraz PSD do pliku wyjściowego za pomocą metody save.

W tym artykule przeanalizowaliśmy, jak manipulować danymi pikseli w pliku PSD za pomocą Aspose.PSD dla Pythona. Dzięki zrozumieniu dostarczonego kodu można wykonywać różne operacje na pikselach, takie jak modyfikowanie pikseli na podstawie określonych warunków. Aspose.PSD zapewnia wszechstronny zestaw funkcji do pracy z plikami PSD programistycznie, co czyni go cennym narzędziem do manipulacji obrazami w Pythonie.

Należy pamiętać, że dostarczony kod zakłada, że masz już zainstalowaną bibliotekę Aspose.PSD oraz jej zależności. Więcej informacji na temat instalacji i korzystania z Aspose.PSD dla Pythona znajdziesz w oficjalnej dokumentacji.

Zachęcamy do sprawdzenia pełnego przykładu.

## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-pixel-data-manipulation.py" >}}
