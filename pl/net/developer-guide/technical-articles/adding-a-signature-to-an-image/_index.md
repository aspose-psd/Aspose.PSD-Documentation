---
title: Dodawanie podpisu do obrazu
type: docs
weight: 70
url: /pl/net/dodawanie-podpisu-do-obrazu/
---

## **Dodawanie podpisu**

Dodawanie podpisu do obrazu jest czasami konieczne, aby cyfrowo podpisać obrazy i uniknąć fałszowania. Innym pomysłem może być traktowanie obrazu bardziej jakby był prezentowany w galerii. Bez względu na powód, interfejsy API Aspose.PSD zapewniają funkcję dodawania podpisu do obrazu za pomocą najprostszego mechanizmu, jak wyjaśniono poniżej. Należy pamiętać, że ten przykład wykorzystuje klasę [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), aby narysować inny obraz z podpisem na powierzchni oryginalnego obrazu. Aby zademonstrować operację, załadujemy obraz PSD z dysku i narysujemy inny obraz jako podpis na powierzchni oryginalnego obrazu przy użyciu metody [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) klasy Graphics. Zapiszemy wynikowy obraz w formacie PNG, używając klasy [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions). Poniżej znajduje się przykładowy kod demonstrujący, jak dodać podpis do obrazu. Kod źródłowy przykładu został podzielony na części, aby ułatwić śledzenie. Krok po kroku przykład pokazuje, jak:

- Załaduj główny i pomocniczy (podpis) obraz.
- Utwórz i zainicjuj obiekt klasy Graphics.
- Narysuj obraz za pomocą metody DrawImage klasy Graphics.
- Zapisz wynik w formacie PNG.
### **Przykłady programów**
#### **Ładowanie obrazów**
Najpierw utwórz instancje klasy Image, aby załadować przykładowe obrazy z dysku.
#### **Tworzenie i Inicjowanie Obiektu Graficznego**
Po załadowaniu obrazów utwórz i zainicjuj obiekt klasy Graphics, korzystając z obiektu obrazu głównego.
#### **Rysowanie Obrazu Pomocniczego na Obrazie Głównym**
Następnie, używając metody DrawImage klasy Graphics, dodaj obraz pomocniczy do obrazu głównego. Istnieje kilka wersji metody DrawImage, które przyjmują obiekt klasy Image jako pierwszy parametr, podczas gdy wszystkie inne parametry odpowiadają lokalizacji, gdzie obraz ma zostać narysowany. W celu demonstracji poniższy kod używa wersji przeciążenia DrawImage, której drugi parametr przyjmuje obiekt klasy Point i próbuje narysować podpis w dolnym prawym rogu obrazu głównego.
#### **Zapisywanie Obrazu**
Na koniec zapisz obraz z powrotem na dysku lokalnym jako plik PNG, używając klasy PngOptions.
#### **Pełne źródło**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
