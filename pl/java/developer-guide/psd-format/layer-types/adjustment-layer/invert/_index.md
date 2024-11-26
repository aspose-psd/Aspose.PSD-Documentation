---
title: Warstwa dostosowania odwrócenia
type: docs
weight: 30
url: /pl/java/layer-types/adjustment-layer/invert/
---

# Praca z warstwą dostosowania odwrócenia w programie Photoshop w języku Java

W tym artykule pokażemy, jak programowo zamienić obraz w dokumencie Photoshopa na negatywny w języku Java. W tym celu będziemy używać biblioteki do manipulacji formatem plików PSD o nazwie Aspose.PSD dla Javy.

Interfejs programowania aplikacji (API) do odwracania kolorów pozwala **dodać negatywny efekt do obrazu**. Możesz już widział, jak [odwrócić kolory obrazu przy użyciu warstwy dostosowania Krzywe](/psd/pl/java/layer-types/adjustment-layer/curves/). Jednak dzisiaj rozważymy szybszy i łatwiejszy sposób wykonania tej samej czynności za pomocą warstwy dostosowania odwrócenia.

## Przegląd API

**API warstwy dostosowania odwrócenia** składa się z samej klasy warstwy, czyli [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Ta klasa nie posiada własnych elementów publicznych, ponieważ dziedziczy je wszystkie po klasie nadrzędnej ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). To upraszcza jej użycie, ponieważ wszystko, co musisz zrobić, to dodać ją do pliku PSD, a obraz stanie się negatywny.

## Odwróć kolory obrazu

Więc nawet jeśli wydaje się to oczywiste, pozwól nam pokazać dla jasności, jak **zastosować warstwę dostosowania odwrócenia do obrazu** astronauty (a), aby uzyskać efekt negatywny dla tego obrazu (b).

![Przykład przed i po zastosowaniu warstwy dostosowania odwrócenia](invert-adjustment-layer-figure-1.png)

Aby **odwrócić kolory obrazu**, po prostu dodaj warstwę dostosowania odwrócenia do pliku PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

To wszystko! Nie ma żadnych konkretnych właściwości do skonfigurowania dla tego typu warstwy dostosowania.

## Wnioski

W tym artykule dowiedzieliśmy się o API warstwy dostosowania odwrócenia w Aspose.PSD dla języka Java. Jest to narzędzie bezproblemowe do uzyskiwania obrazów negatywnych, ponieważ API tej warstwy dostosowania nie deklaruje żadnych elementów publicznych.
