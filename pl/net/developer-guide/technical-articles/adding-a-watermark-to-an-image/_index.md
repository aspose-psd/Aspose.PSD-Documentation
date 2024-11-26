---
title: Dodawanie znaku wodnego do obrazu
type: docs
weight: 30
url: /pl/dodawanie-znaku-wodnego-do-obrazu/
---

## **Dodawanie znaku wodnego do obrazu**
Ten dokument wyjaśnia, jak dodać znak wodny do obrazu za pomocą Aspose.PSD. Dodawanie znaku wodnego do obrazu jest częstym wymaganiem dla aplikacji przetwarzania obrazów. Ten przykład wykorzystuje klasę Graphics do rysowania ciągu znaków na powierzchni obrazu.

### **Dodawanie znaku wodnego**
Aby zilustrować operację, wczytamy obraz BMP z dysku i narysujemy ciąg znaków jako znak wodny na powierzchni obrazu za pomocą metody DrawString klasy Graphics. Zapiszemy obraz w formacie PNG za pomocą klasy PngOptions. Poniżej znajduje się przykładowy kod demonstrujący, jak dodać znak wodny do obrazu. Kod źródłowy został podzielony na części, aby ułatwić śledzenie. Krok po kroku przykłady pokazują, jak:

1. [Wczytać](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) obraz.
1. Utwórz i zainicjuj obiekt [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Utwórz i zainicjuj obiekt Font oraz [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Narysuj ciąg znaków jako znak wodny za pomocą metody [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) klasy Graphics.
1. Zapisz obraz w formacie PNG.

Poniższy fragment kodu pokazuje, jak dodać znak wodny do obrazu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **Dodawanie przekątnego znaku wodnego**
Dodanie przekątnego znaku wodnego do obrazu jest podobne do dodawania poziomego znaku wodnego, o którym dyskutowaliśmy powyżej, z kilkoma różnicami. Aby zilustrować operację, wczytamy obraz JPG z dysku, dodamy transformacje za pomocą obiektu klasy [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) i narysujemy ciąg znaków jako znak wodny na powierzchni obrazu za pomocą metody DrawString klasy Graphics. Poniżej znajduje się przykładowy kod demonstrujący, jak dodać przekątny znak wodny do obrazu. Kod źródłowy został podzielony na części, aby ułatwić śledzenie. Krok po kroku przykłady pokazują, jak:

1. Wczytać obraz.
1. Utwórz i zainicjuj obiekt Graphics.
1. Utwórz i zainicjuj obiekty [Font](https://reference.aspose.com/psd/net/aspose.psd/font) oraz SolidBrush.
1. Pobierz rozmiar obrazu w obiekcie [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Utwórz instancję klasy Matrix i wykonaj transformację składaną.
1. Przypisz transformację do obiektu Graphics.
1. Utwórz i zainicjuj obiekt [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Narysuj ciąg znaków jako znak wodny za pomocą metody DrawString klasy Graphics.
1. Zapisz obraz wynikowy.

Poniższy fragment kodu pokazuje, jak dodać przekątny znak wodny.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
