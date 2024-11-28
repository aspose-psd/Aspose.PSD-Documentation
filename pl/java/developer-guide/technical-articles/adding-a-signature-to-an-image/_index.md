---
title: Dodawanie sygnatury do obrazu
type: docs
weight: 10
url: /pl/java/dodawanie-sygnatury-do-obrazu/
---

## **Dodawanie sygnatury**


Dodanie sygnatury do obrazu jest czasami wymagane, aby cyfrowo podpisać obrazy i uniknąć fałszerstw. Innym pomysłem może być traktowanie obrazu bardziej jakby był wyświetlany w galerii. Bez względu na powód, API Aspose.PSD zapewnia możliwość dodania sygnatury do obrazu za pomocą najprostszego mechanizmu, jak to jest wyjaśnione poniżej. Należy zauważyć, że ten przykład wykorzystuje klasę Graphics do narysowania innego obrazu z sygnaturą na oryginalnej powierzchni obrazu. Aby wyjaśnić operację, załadujemy obraz PSD z dysku i narysujemy inny obraz jako sygnaturę na oryginalnej powierzchni obrazu za pomocą metody DrawImage klasy Graphics. Zapiszemy wynikowy obraz w formacie PNG za pomocą klasy PngOptions. Poniżej znajduje się przykładowy kod, który demonstruje, jak dodać sygnaturę do obrazu. Przykładowy kod źródłowy został podzielony na części, aby ułatwić śledzenie. Kroki po kroku przykład pokazuje, jak:

- Załaduj obrazy główne i drugorzędne (sygnatury).
- Utwórz i zainicjuj obiekt klasy Graphics.
- Narysuj obraz za pomocą metody DrawImage klasy Graphics.
- Zapisz wynik w formacie PNG.
### **Przykłady programów**
#### **Ładowanie obrazów**
Najpierw utwórz instancje klasy Image, aby załadować przykładowe obrazy z dysku.
#### **Tworzenie i inicjowanie obiektu graficznego**
Po załadowaniu obrazów, utwórz i zainicjuj obiekt klasy Graphics, korzystając z obiektu obrazu głównego.
#### **Rysowanie obrazu drugiego na obrazie głównym**
Następnie przy użyciu metody DrawImage klasy Graphics dodaj obraz drugorzędny na obraz główny. Istnieje kilka przeciążeń metody DrawImage, które akceptują obiekt Image jako pierwszy parametr, podczas gdy wszystkie inne parametry odpowiadają lokalizacji, gdzie obraz ma zostać narysowany. Na potrzeby demonstracji poniższy kod używa wersji przeciążonej DrawImage, która przyjmuje obiekt Point jako drugi parametr i próbuje narysować sygnaturę w prawym dolnym rogu obrazu głównego.
#### **Zapisywanie obrazu**
Na koniec zapisz obraz z powrotem na dysku lokalnym jako plik PNG, korzystając z klasy PngOptions.
#### **Źródło**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}
