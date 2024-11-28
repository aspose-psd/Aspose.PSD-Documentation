---
title: Rysowanie obrazów przy użyciu GraphicsPath
type: docs
weight: 30
url: /pl/java/rysowanie-obrazow-przy-uzyciu-graphicspath/
---

## **Rysowanie obrazów przy użyciu GraphicsPath**
Klasa GraphicsPath jest odpowiedzialna za tworzenie i utrzymywanie ścieżki graficznej. GraphicsPath nie odnosi się bezpośrednio do obrazu i nie zmienia samego obrazu, zamiast tego można ją uznać za obiekt zawierający metadane opisujące ścieżki, które może rysować klasa Graphics. Klasa GraphicsPath używa figur; każda figura jest skonstruowana z sekwencji połączonych linii i krzywych lub podstawowych kształtów geometrycznych. Każdy kształt może zostać podzielony na segmenty kształtu. Można dodawać, usuwać i zmieniać różne figury lub kształty w obiekcie GraphicsPath. Gdy GraphicsPath został w pełni opisany, użyj odpowiednich metod klasy Graphics (DrawPath i Fill Paths) do narysowania ścieżek lub wypełnienia ścieżek. Klasa Graphics pobiera każdy segment kształtu i rysuje go, tworząc ostateczny obraz.
### **Rysowanie przy użyciu klasy GraphicsPath**
Poniżej znajduje się przykład demonstrujący użycie klasy GraphicsPath. Źródło przykładu zostało podzielone na kilka części, aby było proste i łatwe do śledzenia. Krok po kroku przykłady pokazują, jak:

- Utwórz obraz.
- Zainicjuj obiekt Graphics.
- Wyczyść powierzchnię.
- Utwórz instancję GraphicsPath.
- Utwórz figurę.
- Dodaj kształty do figury.
- Utwórz tablicę figur.
- Narysuj ścieżki.
- Wypełnij ścieżki.

### **Rysowanie obrazów przy użyciu GraphicsPath: Przykłady programowania**
#### **GraphicsPath : Utwórz obraz**
Zacznij od stworzenia obrazu, korzystając z dowolnej z metod opisanych w Tworzenie plików.
#### **GraphicsPath : Zainicjuj obiekt Graphics**
Utwórz i zainicjuj obiekt Graphics, przekazując obiekt Image do jego konstruktora.
#### **GraphicsPath : Wyczyść powierzchnię**
Wyczyść powierzchnię graficzną, wywołując metodę Clear klasy Graphics i przekazując kolor jako parametr. Ta metoda wypełnia powierzchnię graficzną kolorem przekazanym jako argument.
#### **GraphicsPath : Utwórz instancję GraphicsPath**
Utwórz instancję GraphicsPath, z ustawieniem GraphicsPath na Alternate domyślnie. Ten tryb określa, jak wypełnić wnętrze zamkniętej figury. Inna możliwa wartość GraphicsPath to Winding.
#### **GraphicsPath : Utwórz figurę**
Utwórz instancję klasy Figure. Jak wspomniano wcześniej, figura może zawierać kształty, a kształty znajdują się w przestrzeni nazw Aspose.PSD.Shapes.
#### **GraphicsPath : Dodaj kształty do figury**
Metoda Add Shapes udostępniana przez klasę Figure pozwala dodać kształty do figury. W przedstawionych poniżej przykładach kodu dodawane są różne kształty do obiektu Figure.
#### **GraphicsPath : Dodaj figury do tablicy**
Wiele figurek można dodać do obiektu GraphicsPath, korzystając z metody AddFigures udostępnionej przez klasę GraphicsPath. Ta metoda przyjmuje tablicę figur jako parametr.
#### **GraphicsPath : Narysuj ścieżki**
Narysuj GraphicsPath za pomocą metody DrawPath udostępnionej przez klasę Graphics. Metoda przyjmuje dwa parametry. Pierwszy parametr to obiekt klasy Pen, który określa kolor, szerokość i styl ścieżki. Drugi parametr to obiekt klasy GraphicsPath, reprezentujący samą ścieżkę.
#### **GraphicsPath : Wypełnij ścieżki**

Możesz wypełnić ścieżkę, przekazując obiekt GraphicsPath do metody Fill Paths udostępnionej przez klasę Graphics. Metoda Fill Paths wypełnia ścieżkę zgodnie z ustawionym modelem wypełnienia (alternate lub winding) dla ścieżki. Jeśli ścieżka zawiera jakiekolwiek otwarte figury, ścieżka jest wypełniana tak, jakby te figury były zamknięte.

Metoda Fill Paths akceptuje dwa parametry. Pierwszy parametr to obiekt dowolnej klasy pędzla z przestrzeni nazw Aspose.PSD.Brushes. Drugi parametr to sama ścieżka. W tym przykładzie użyj HatchBrush, który jest prostokątnym pędzlem z wzorem kratki, kolorem pierwszoplanowym i kolorem tła. Przed przekazaniem obiektu HatchBrush do metody Fill Paths ustaw jego właściwości.
### **GraphicsPath : Pełne źródło**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



Wszystkie klasy implementujące IDisposable są tworzone w instrukcji Using, aby zapewnić ich poprawne usunięcie.
