---
title: Obsługa dużych obrazów
type: docs
weight: 40
url: /pl/net/obsługa-dużych-obrazów/
---

## **Obsługa dużych obrazów**
Ponieważ standardowa biblioteka .NET ma pewne ograniczenia dotyczące rozmiaru obrazu, wprowadziliśmy nowy mechanizm obsługi dużych obrazów. Nowe podejście eliminuje te ograniczenia, ale ze względu na limity rozmiaru danych maksymalne obsługiwane wymiary do tworzenia i wczytywania wynoszą 2 147 483 647 x 2 147 483 647 pikseli.
### **Praca z dużymi obrazami**
Aspose.PSD poprawił wydajność oraz obsługę dużych obrazów. Obrazy o wielkości setek megabajtów nie stanowią już problemu, dzięki czemu można je tworzyć, wczytywać i rysować. Niemniej jednak, ze względu na częściowe przetwarzanie i obsługę wyjątków OutOfMemoryException, wydajność może być bardzo niska przy bardzo dużych obrazach. Wynika to z faktu, że Aspose.PSD stara się ponownie alokować mniejszą ilość danych do przetwarzania, a każdy krok realokacji jest bardzo kosztowny. Korzyści nowej architektury są oczywiste:

- Brak ograniczeń co do rozmiaru obrazu.
- Nie jesteś ograniczony dostępną pamięcią w komputerze.

Jeśli doświadczasz wolnego przetwarzania, zaleca się zwiększenie całkowitej ilości pamięci RAM, aby pomieścić wszystkie piksele w pamięci. Jeśli nie zrobisz tego, przetwarzanie nadal jest możliwe, ale wolniejsze. Podejście jest następujące:

- Wywołaj metodę [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) z określonym prostokątem i delegatem do otrzymywania załadowanych pikseli.

Aspose.PSD próbuje wczytać cały prostokąt.

- Jeśli jest wystarczająco pamięci, aby pomieścić wszystkie piksele, wszystkie piksele są po prostu zwracane do wywoływającego.
- Jeśli nie ma wystarczająco pamięci, wywołujący otrzymuje podzbiór pikseli z wewnątrz określonego prostokąta. Gdy te piksele zostaną przetworzone, wywoływający otrzymuje następny prostokąt. Przetwarzanie kończy się, gdy cały prostokąt zostanie przetworzony.

Aspose.PSD stara się wyodrębnić jak najwięcej linii. Jeśli nie ma wystarczającej pamięci, aby pomieścić pojedynczą linię pikseli, to jedna linia jest dzielona na części zgodnie z prostokątami mającymi wysokość 1. Możesz również rysować na dużych obrazach. Proces rysowania stara się dotknąć całego żądanego prostokąta. Jeśli nie ma wystarczająco pamięci, rysowanie jest wykonane na częściowych prostokątach, aż cały obszar zostanie narysowany. Dodatkowo, Aspose.PSD obsługuje zapisywanie i eksportowanie dużych obrazów. Zapisz obraz źródłowy na dysku lub wyeksportuj go do innego formatu pliku. Proces zapisywania lub eksportowania jest wykonywany za pomocą częściowych prostokątów, jeśli jest to konieczne.
### **Obsługiwane formaty obrazów**
Następujące formaty są obsługiwane dla przetwarzania dużych obrazów:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Powyższe formaty mogą być bezpiecznie przetwarzane poprzez tworzenie, modyfikowanie, stosowanie operacji rysowania, zapisywanie na dysku lub eksportowanie bez względu na rozmiar obrazu.

