---
title: Nagłówek pliku PSD i PSB
type: docs
weight: 40
url: /pl/net/psd-and-psb-file-header/
---

## **Opis**
Nagłówek pliku programu Adobe Photoshop zawiera informacje o wersji pliku (1 dla plików PSD i 2 dla plików PSB), liczbie kanałów, trybie koloru i głębi bitowej.

Możesz dowiedzieć się, które kombinacje trybu koloru i głębi bitowej są obsługiwane przez Aspose.PSD związane z artykułem.

Nagłówek pliku zawiera podstawowe właściwości obrazu.

|**Długość**|**Opis**|
| :- | :- |
|4|Sygnatura: zawsze równa *"8BPS"*|
|2|[Wersja PSD](https://reference.aspose.com/psd/pl/aspose.psd.fileformats.psd/fileformatversion): zawsze równa 1 dla plików PSD i 2 dla plików PSB. Aspose.PSD może wykryć wersję formatu pliku i poprawnie ją odczytać.|
|6|Zarezerwowane: musi być zerem.|
|2|Liczba kanałów w obrazie, w tym ewentualne kanały alfa. Obsługiwany zakres to od 1 do 56.|
|4|Wysokość obrazu w pikselach. Obsługiwany zakres to od 1 do 30 000. Plik PSB obsługuje wysokość do 300 000 pikseli. Pliki PSB są również obsługiwane przez Aspose.PSD.|
|4|Szerokość obrazu w pikselach. Obsługiwany zakres to od 1 do 30 000. Plik PSB obsługuje szerokość do 300 000 pikseli. Aspose.PSD również obsługuje wsadowe przetwarzanie dużych plików PSD/PSB.|
|2|Głębia: liczba bitów na kanał. Obsługiwane wartości to 1, 8, 16 i 32. Jednak nie każdy tryb koloru działa z każdą głębią.|
|2|[Tryb koloru PSD](https://reference.aspose.com/psd/pl/com.aspose.psd.fileformats.psd/ColorModes) pliku. Obsługiwane wartości to: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotone = 8; Lab = 9.|
Możesz sprawdzić nasze [API odnośnie plików PSD](https://reference.aspose.com/psd) dla tego zagadnienia.
