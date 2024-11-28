---
title: Unikaj degradacji wydajności podczas rysowania na skompresowanych obrazach
type: docs
weight: 40
url: /pl/java/unikaj-degradacji-wydajnosci-podczas-rysowania-na-skomrpesowanych-obrazach/
---

## **Unikaj degradacji wydajności podczas rysowania na skompresowanych obrazach**
Są sytuacje, gdy chcesz przeprowadzić bardzo złożone operacje graficzne na skompresowanym obrazie. Gdy Aspose.PSD musi kompresować i dekompresować obrazy w locie, może wystąpić degradacja wydajności. Rysowanie na skompresowanych obrazach może również wpłynąć na wydajność.
### **Rozwiązanie**
Aby uniknąć degradacji wydajności, zalecamy konwersję obrazu do formatu nieskompresowanego, tzw. formatu surowego, przed wykonaniem operacji graficznych.
### **Używanie ścieżki pliku**
W poniższym przykładzie obraz PSD jest konwertowany do formatu surowego (bez kompresji) i zapisywany na dysku. Nieskompresowany obraz jest następnie ponownie wczytany przed wykonaniem na nim operacji graficznych. Ta sama technika można zastosować do plików BMP i GIF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Użycie obiektu strumienia**
Poniższy fragment kodu pokazuje, jak obraz PSD jest konwertowany do formatu surowego (bez kompresji) i zapisywany na dysku za pomocą strumienia.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
