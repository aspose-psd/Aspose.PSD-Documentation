---
title: Obsługiwane połączenie trybów kolorów i głębi bitowej w formacie PSD
type: docs
weight: 80
url: /pl/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Opis**
Aspose.PSD obsługuje otwieranie plików PSD z dowolną kombinacją trybu kolorów i głębi bitowej w plikach Adobe Photoshop PSD. Możesz otworzyć takie pliki i użyć interfejsu API niskiego poziomu do modyfikacji zawartości pliku. Jednak dla niektórych mniej popularnych kombinacji mogą wystąpić specyficzne problemy, niektóre z nich związane z Ograniczeniami Trybów Kolorów.

## **Obsługiwane połączenie eksportu trybów kolorów i głębokości bitowej w formacie PSD w trybie tylko do odczytu**

| |Bitmap|Skala odcieni szarości|Indeksowany|RGB|CMYK|Wielokanałowy|Duotono|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Głębokość 1|Tak[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Głębokość 8|-|Tak|Tak|Tak|Tak|Nie Q3-Q4|Nie Q3-Q4|Tak[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Głębokość 16|-|Tak|-|Tak|Tak|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Nie (Q3-Q4)|
|Głębokość 32|-|Tak*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Tak*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Mniejsze problemy w niektórych przypadkach

## **Obsługiwane połączenie eksportu trybów kolorów i głębokości bitowej w formacie PSD w trybie edycji**

| |Bitmap|Skala odcieni szarości|Indeksowany|RGB|CMYK|Wielokanałowy|Duotono|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Głębokość 1|Tak|-|-|-|-|-|-|-|
|Głębokość 8|-|Tak|Nie|Tak|Tak|Nie Q3-Q4|Nie Q3-Q4|Tak*|
|Głębokość 16|-|Tak|-|Tak|Tak*|-|-|Nie (Q3-Q4)|
|Głębokość 32|-|Nie (Q3-Q4)|-|Nie (Q3-Q4)|-|-|-|-|
\* Mniejsze problemy w niektórych przypadkach

Jeśli potrzebujesz wsparcia dla konkretnej kombinacji trybu kolorów / głębi bitowej, możesz opublikować to na [Forach Aspose](https://forum.aspose.com/c/psd)
