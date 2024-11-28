---
title: Warstwa Korygowania Naświetlenia
type: docs
weight: 30
url: /pl/java/rodzaje-warstw/warstwa-korygowania-naswietlenia/
---

# Praca z warstwą korygowania naswietlenia w programie Photoshop w języku Java

W tym artykule dodamy warstwę korygowania naswietlenia do dokumentu programu Adobe® Photoshop® za pomocą biblioteki do manipulacji formatem plików PSD Aspose.PSD dla języka Java. Biblioteka działa bez konieczności instalowania edytora Photoshopa, ponieważ wykorzystuje własne algorytmy przetwarzania obrazów. Dowiedzieliśmy się również kilku szczegółów dotyczących interfejsu API korygowania naswietlenia biblioteki.

## Przegląd API

Warstwa korygowania naswietlenia konfigurowana jest za pomocą klasy [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), która zawiera następujące właściwości do pracy z korekcją naświetlenia:

- Określa, jak dużo światła ma zdjęcie poprzez ścieśnianie lub rozciąganie całego histogramu w stosunku do barw czarnych. Działa głównie na najjaśniejsze elementy.
- W przeciwieństwie do przesunięcia naswietlenia, które działa głównie na cienie.
- Korekta gamma. Korektuje luminancję obrazu.

## Poprawa naswietlenia

Korekcja naswietlenia i powiązane właściwości sprowadzają się do zmiany kilku właściwości klasy. Zastosujmy więc pewną korekcję naswietlenia (a) do zbyt słabo naświetlonego zdjęcia biblioteki (b), aby uczynić je zauważalnym dla ludzkiego oka (c).

![Przykład Warstwy Korygowania Naswietlenia](exposure-adjustment-layer-figure-1.png)

Cała korekcja realizowana jest głównie za pomocą korekty gamma. Jednakże, naswietlenie i przesunięcie również są nieco dostosowywane. Wszystko, co musisz zrobić, to ustawić odpowiednie wartości dla wymienionych właściwości:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Zwróć uwagę, że naswietlenie musi znajdować się w zakresie od -20.0 do 20.0, wartość przesunięcia musi mieścić się w zakresie od -0.5 do 0.5, a zakres wartości korekty gamma musi wynosić od 9.99 do 0.01.

Zajrzyj do [referencji API warstwy korygowania naswietlenia](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) po więcej informacji.

## Podsumowanie

W tym artykule nauczyliśmy się, jak dodać warstwę korygowania naswietlenia do pliku PSD, aby rozjaśnić obraz, a także omówiliśmy niektóre szczegóły API.
