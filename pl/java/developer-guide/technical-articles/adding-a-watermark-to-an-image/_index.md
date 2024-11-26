---
title: Dodawanie znaku wodnego do obrazu
type: docs
weight: 20
url: /pl/dodawanie-znaku-wodnego-do-obrazu/
---

## **Dodawanie znaku wodnego do obrazu**
Ten dokument wyjaśnia, jak dodać znak wodny do obrazu za pomocą Aspose.PSD. Dodawanie znaku wodnego do obrazu jest powszechnym wymaganiem dla aplikacji przetwarzania obrazów. Ten przykład wykorzystuje klasę Graphics do rysowania napisu na powierzchni obrazu.

### **Dodawanie znaku wodnego**
Aby zademonstrować operację, załadujemy obraz BMP z dysku i narysujemy napis jako znak wodny na powierzchni obrazu za pomocą metody DrawString klasy Graphics. Zapiszemy obraz w formacie PNG za pomocą klasy PngOptions. Poniżej znajduje się przykładowy kod demonstrujący, jak dodać znak wodny do obrazu. Kod przykładowy został podzielony na części, aby ułatwić śledzenie. Krok po kroku przykłady pokazują, jak:

1. Załadować obraz.
1. Utworzyć i zainicjować obiekt Graphics.
1. Utworzyć i zainicjować obiekty Font i SolidBrush.
1. Narysować napis jako znak wodny za pomocą metody DrawString klasy Graphics.
1. Zapisać obraz w formacie PNG.

Poniższy fragment kodu pokazuje, jak dodać znak wodny do obrazu.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}

### **Dodawanie ukosnego znaku wodnego**
Dodawanie ukosnego znaku wodnego do obrazu jest podobne do dodawania znaku wodnego poziomego, o którym wspomniano powyżej, z kilkoma różnicami. Aby zademonstrować operację, załadujemy obraz JPG z dysku, dodamy transformacje za pomocą obiektu klasy Matrix i narysujemy napis jako znak wodny na powierzchni obrazu za pomocą metody DrawString klasy Graphics. Poniżej znajduje się przykładowy kod demonstrujący, jak dodać ukosny znak wodny do obrazu. Kod przykładowy został podzielony na części, aby ułatwić śledzenie. Krok po kroku przykłady pokazują, jak:

1. Załadować obraz.
1. Utworzyć i zainicjować obiekt Graphics.
1. Utworzyć i zainicjować obiekt Font i SolidBrush.
1. Pobierz rozmiar obrazu w obiekcie SizeF.
1. Utwórz instancję klasy Matrix i wykonaj transformację złożoną.
1. Przypisać transformację do obiektu Graphics.
1. Utwórz i zainicjuj obiekt StringFormat.
1. Narysuj napis jako znak wodny za pomocą metody DrawString klasy Graphics.
1. Zapisz obraz wynikowy.

Poniższy fragment kodu pokazuje, jak dodać ukosny znak wodny do obrazu.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
