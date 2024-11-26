---
title: Warstwa dostosowująca filtr zdjęć
type: docs
weight: 30
url: /pl/java/layer-types/adjustment-layer/photo-filter/
---

# Praca z Java Photoshop Photo Filter adjustment layer

Dziś zobaczymy, jak zastosować warstwę dostosowującą filtr zdjęć do istniejącego dokumentu Photoshopa za pomocą Aspose.PSD dla Javy, czyli biblioteki do manipulowania formatem pliku PSD.

**API warstwy dostosowującej filtr zdjęć** zmienia balans kolorów obrazu poprzez barwienie. Obraz wynikowy będzie wyglądał tak samo jak po użyciu rzeczywistego filtra do aparatu. Zauważ, że API warstwy dostosowującej filtr zdjęć biblioteki nieco różni się od tego w Photoshopie, ponieważ nie ma jeszcze predefiniowanych filtrów. Jednakże, jest taka sama pod względem wszystkich innych aspektów. Oznacza to, że można ustawić kolor barwnika oraz zmieniać jego intensywność (gęstość) oraz korzystać z opcji Zachowaj luminescencję.

## Przegląd API

API warstwy dostosowującej filtr zdjęć jest dość proste w użyciu. Istnieje główna klasa [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), która służy jako punkt wejścia do tej warstwy dostosowującej i zawiera tylko trzy publiczne właściwości, a mianowicie kolor, gęstość oraz zachowanie luminescencji, poprzez które zachodzi dostosowanie.

## Regulacja balansu kolorów

Ponieważ nie ma dużo do omówienia, rozważmy **przykład dostosowania balansu kolorów** za pomocą filtra zdjęć od razu. Dodamy ręcznie filtr rozgrzewający (a) do obrazu rzeźby jelenia (b), aby uzyskać obraz w ciepłych tonacjach (c), który jest przyjemniejszy dla oka.

![Przykład warstwy dostosowującej filtr zdjęć](photo-filter-adjustment-layer-figure-1.png)

Przede wszystkim zauważ, że [metoda fabryczna](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) różni się od metody dla [innych warstw dostosowujących](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers), ponieważ nie ma domyślnej metody (bez argumentów). Dlatego, aby dodać warstwę dostosowującą filtr zdjęć do załadowanego dokumentu Photoshopa, wymagany jest pojedynczy argument, czyli [kolor](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Aby odtworzyć efekt filtra rozgrzewającego, wystarczy przekazać pomarańcz jako argument do metody fabrycznej, następnie ustawić gęstość za pomocą odpowiednich setterów:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Warto dodać, że właściwość Density ma domyślną wartość 100, a właściwość Preserve Luminosity ma domyślną wartość true (dlatego nie włączamy explicite tej opcji).

## Wnioski

W tym artykule rozważaliśmy użycie API warstwy dostosowującej filtr zdjęć Aspose.PSD dla Javy. To narzędzie jest proste w użyciu i pozwala dodać barwnik do obrazu z zmienną gęstością. To szybki sposób regulacji balansu kolorów całego obrazu.
