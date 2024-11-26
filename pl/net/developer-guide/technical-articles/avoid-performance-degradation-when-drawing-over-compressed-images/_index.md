---
title: Unikaj Degradacji Wydajności Przy Rysowaniu na Skompresowanych Obrazach
type: docs
weight: 10
url: /pl/net/unikaj-degradacji-wydajnosci-przy-rysowaniu-na-skompresowanych-obrazach/
---

## **Unikaj Degradacji Wydajności Przy Rysowaniu na Skompresowanych Obrazach**
Są momenty, kiedy chcesz wykonać bardzo złożone operacje graficzne na skompresowanym obrazie. Gdy Aspose.PSD musi kompresować i dekompresować obrazy na żywo, może wystąpić degradacja wydajności. Rysowanie na skompresowanych obrazach może również wiązać się z karą dla wydajności.
### **Rozwiązanie**
Aby uniknąć degradacji wydajności, zalecamy konwersję obrazu do formatu nieskompresowanego, czyli surowego, przed wykonywaniem operacji graficznych.
### **Używanie Ścieżki Pliku**
W poniższym przykładzie obraz PSD jest konwertowany do formatu surowego (bez kompresji) i zapisywany na dysku. Nieskompresowany obraz jest następnie ponownie wczytywany przed wykonaniem na nim operacji graficznych. Ta sama technika dotyczy plików BMP i GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **Używanie Obiektu Strumienia**
Poniższy fragment kodu pokazuje, jak obraz PSD jest konwertowany do formatu surowego (bez kompresji) i zapisywany na dysku przy użyciu MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
