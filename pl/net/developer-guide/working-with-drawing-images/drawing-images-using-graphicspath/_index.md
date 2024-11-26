---
title: Rysowanie obrazów za pomocą GraphicsPath
type: docs
weight: 30
url: /pl/net/rysowanie-obrazow-uzywajac-graphicspath/
---

## **Rysowanie obrazów za pomocą GraphicsPath**
Klasa [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) jest odpowiedzialna za tworzenie i utrzymywanie ścieżki graficznej. GraphicsPath nie odnosi się do obrazu i nie zmienia samego obrazu, zamiast tego można go uznać za obiekt zawierający metadane opisujące ścieżki, które możne narysować klasa Graphics. Klasa GraphicsPath korzysta z figur; każda figura składa się albo z sekwencji połączonych linii i krzywych, albo z podstawowej figury geometrycznej. Każdą figurę można podzielić na segmenty figury. Można dodać, usunąć i zmienić różne figury lub kształty w obiekcie GraphicsPath. Gdy GraphicsPath zostanie w pełni opisany, użyj odpowiednich metod klasy Graphics (DrawPath i Fill Paths), aby narysować nad ścieżkami lub je wypełnić. Klasa Graphics pobiera każdy segment figury i rysuje go, aby uzyskać finalny obraz.
### **Rysowanie za pomocą klasy GraphicsPath**
Poniżej znajduje się przykład demonstrujący użycie klasy [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath). Kod źródłowy przykładu został podzielony na kilka części, aby ułatwić śledzenie. Krok po kroku przykłady pokazują, jak:

- Utwórz obraz.
- Zainicjuj obiekt Graphics.
- Wyczyść powierzchnię.
- Utwórz instancję [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Utwórz figurę.
- Dodaj kształty do figury.
- Utwórz tablicę figur.
- Narysuj ścieżki.
- Wypełnij ścieżki.


### **Rysowanie obrazów za pomocą GraphicsPath: Przykłady programowania**
#### **GraphicsPath : Utwórz obraz**
Zacznij od utworzenia obrazu używając jednej z metod opisanych w Tworzenie plików.
#### **GraphicsPath : Zainicjuj obiekt Graphics**
Utwórz i zainicjuj obiekt Graphics, przekazując obiekt Image do jego konstruktora.
#### **GraphicsPath : Wyczyść powierzchnię**
Wyczyść powierzchnię Graphics, wywołując metodę Clear klasy Graphics i przekazując kolor jako parametr. Ta metoda wypełnia powierzchnię Graphics kolorem podanym jako argument.
#### **GraphicsPath : Utwórz instancję GraphicsPath**
Utwórz instancję GraphicsPath, gdzie GraphicsPath domyślnie jest ustawiony na Alternate. Ten tryb określa, w jaki sposób wypełnić wnętrze zamkniętej figury. Inna możliwa wartość GraphicsPath to Winding.
#### **GraphicsPath : Utwórz figurę**
Utwórz instancję klasy Figure. Jak już wspomniano, Figura może zawierać Kształty, a kształty znajdują się w przestrzeni nazw Aspose.PSD.Shapes.
#### **GraphicsPath : Dodaj kształty do figury**
Metoda Dodaj kształty udostępniona przez klasę Figure pozwala dodać kształty do figury. W poniższych przykładach kodu dodawane są różne kształty do obiektu Figure.
#### **GraphicsPath : Dodaj figury do tablicy**
Wiele figur można dodać do obiektu GraphicsPath, korzystając z metody AddFigures udostępnionej przez klasę GraphicsPath. Ta metoda przyjmuje tablicę figur jako parametr.
#### **GraphicsPath : Narysuj ścieżki**
Narysuj GraphicsPath, korzystając z metody DrawPath udostępnionej przez klasę Graphics. Metoda przyjmuje dwa parametry. Pierwszy parametr to obiekt klasy Pen, który określa kolor, grubość i styl ścieżki. Drugi parametr to obiekt klasy GraphicsPath, reprezentujący samą ścieżkę.
#### **GraphicsPath : Wypełnij ścieżki**


Możesz wypełnić ścieżkę, przekazując obiekt GraphicsPath do metody Fill Paths udostępnionej przez klasę Graphics. Metoda Fill Paths wypełnia ścieżkę zgodnie z obecnym trybem wypełnienia (alternate lub winding) ustawionym dla ścieżki. Jeśli ścieżka ma jakieś otwarte figury, ścieżka jest wypełniana, jak gdyby te figury były zamknięte.

Metoda Fill Paths przyjmuje dwa parametry. Pierwszy parametr to obiekt dowolnej klasy pędzla z przestrzeni nazw Aspose.PSD.Brushes. Drugi parametr to sama ścieżka. Dla tego przykładu użyj HatchBrush, który jest prostokątnym pędzlem z stylem kratki, kolorem pierwszoplanowym i kolorem tła. Przed przekazaniem obiektu HatchBrush do metody Fill Paths ustaw jego właściwości.
### **GraphicsPath : Pełne źródło**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Wszystkie klasy implementujące IDisposable są tworzone w instrukcji Using, aby zapewnić poprawne ich usuwanie.
