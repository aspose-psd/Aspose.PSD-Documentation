---
title: Wsparcie dla dużych obrazów
type: docs
weight: 60
url: /pl/java/wsparcie-dla-duzych-obrazow/
---

## **Wsparcie dla dużych obrazów**
Ponieważ standardowa biblioteka Java ma pewne ograniczenia co do rozmiaru obrazu, wprowadziliśmy nowy mechanizm wspierający duże obrazy. Nowe podejście eliminuje te ograniczenia, ale ze względu na ograniczenia rozmiaru danych maksymalne obsługiwane wymiary do tworzenia i ładowania to 2 147 483 647 x 2 147 483 647 pikseli.
### **Praca z dużymi obrazami**
Aspose.PSD poprawił wydajność i obsługę dużych obrazów. Obrazy o rozmiarze setek megabajtów nie stanowią już problemu, więc możesz tworzyć, ładować i rysować na tych obrazach. Jednak ze względu na częściowe przetwarzanie i obsługę wyjątków OutOfMemoryException, wydajność może być bardzo niska dla bardzo dużych obrazów. Wynika to z faktu, że Aspose.PSD próbuje ponownie przydzielić mniejszą ilość danych do przetwarzania, a każdy krok realokacji jest bardzo kosztowny. Korzyści nowej architektury są oczywiste:

- Nie ma ograniczeń co do rozmiaru obrazu.
- Nie jesteś ograniczony ilością dostępnej pamięci na twoim komputerze.

Jeśli doświadczasz wolnego przetwarzania, zaleca się zwiększenie całkowitej ilości RAM, aby pomieścić wszystkie swoje piksele w pamięci. Jeśli nie zrobisz tego, przetwarzanie jest nadal możliwe, ale wolniejsze. Podejście jest następujące:

- Wywołaj metodę LoadPartialPixels z pożądanym prostokątem i deleguj otrzymywanie wczytanych pikseli.
  
Aspose.PSD próbuje załadować cały prostokąt.

- Jeśli jest wystarczająco pamięci, aby pomieścić wszystkie piksele, wszystkie piksele zostają po prostu zwrócone do wywołującego.
- Jeśli pamięci brakuje, wywołujący otrzymuje podzbiór pikseli z wnętrza wskazanego prostokąta. Po przetworzeniu tych pikseli, wywołujący otrzymuje następny prostokąt. Przetwarzanie kończy się, gdy cały prostokąt zostanie przetworzony.

Aspose.PSD stara się wyodrębnić jak najwięcej linii. Jeśli nie ma wystarczająco pamięci, aby pomieścić pojedynczą linię pikseli, wtedy jedna linia jest dzielona na części zgodnie z prostokątami o wysokości 1. Możesz także rysować na dużych obrazach. Proces rysowania stara się obejmować cały pożądany prostokąt. Jeśli nie ma wystarczająco pamięci, rysowanie jest wykonywane na częściowych prostokątach aż cały obszar zostanie narysowany. Dodatkowo, Aspose.PSD obsługuje zapisywanie i eksportowanie dużych obrazów. Zachowaj obraz źródłowy na dysku lub wyeksportuj go do innego formatu pliku. Proces zapisu lub eksportu jest wykonywany przy użyciu częściowych prostokątów w razie potrzeby.
### **Obsługiwane formaty obrazów**
Następujące formaty są obsługiwane podczas przetwarzania dużych obrazów:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Wymienione powyżej formaty mogą być bezpiecznie przetwarzane poprzez tworzenie, modyfikowanie, stosowanie operacji rysowania, zapisywanie na dysku lub eksportowanie bez względu na rozmiar obrazu.

.
