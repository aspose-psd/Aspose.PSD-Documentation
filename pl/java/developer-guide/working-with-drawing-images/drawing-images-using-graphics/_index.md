---
title: Rysowanie obrazów za pomocą Graphics
type: docs
weight: 20
url: /pl/java/rysowanie-obrazow-za-pomoca-graphics/
---

## **Rysowanie obrazów za pomocą Graphics**

Z biblioteką Aspose.PSD możesz rysować proste kształty, takie jak linie, prostokąty i koła, a także złożone kształty, takie jak wielokąty, krzywe, łuki i kształty Bezier. Biblioteka Aspose.PSD tworzy takie kształty za pomocą klasy Graphics znajdującej się w przestrzeni nazw Aspose.PSD. Obiekty Graphics są odpowiedzialne za wykonywanie różnych operacji rysowania na obrazie, zmieniając tym samym powierzchnię obrazu. Klasa Graphics używa różnych obiektów pomocniczych do ulepszania kształtów:

- Długopisy, do rysowania linii, obramowywania kształtów lub renderowania innych reprezentacji geometrycznych.
- Pędzle, do definiowania w jaki sposób obszary są wypełniane.
- Czcionki, do definiowania kształtu znaków tekstu.
### **Rysowanie za pomocą klasy Graphics**
Poniżej znajduje się przykładowy kod demonstrujący użycie klasy Graphics. Kod przykładu został podzielony na kilka części, aby zachować prostotę i ułatwić śledzenie. Krok po kroku przykłady pokazują, jak:

1. Utwórz obraz.
1. Utwórz i zainicjalizuj obiekt Graphics.
1. Wyczyść powierzchnię.
1. Narysuj elipsę.
1. Narysuj wypełniony wielokąt i zapisz obraz.
### **Przykłady programowania**
#### **Tworzenie obrazu**
Rozpocznij od utworzenia obrazu za pomocą jednej z metod opisanych w sekcji Tworzenie plików.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Utwórz i Zainicjalizuj obiekt Graphics**
Następnie utwórz i zainicjalizuj obiekt Graphics, przekazując obiekt Image do jego konstruktora.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Wyczyść powierzchnię**
Wyczyść powierzchnię graficzną, wywołując metodę Clear klasy Graphics i przekazując kolor jako parametr. Ta metoda wypełnia powierzchnię graficzną podanym kolorem.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Narysuj elipsę**
Zauważysz, że klasa Graphics udostępnia wiele metod do rysowania i wypełniania kształtów. Znajdziesz pełną listę metod w dokumnetacji API Aspose.PSD dla języka Java. Klasa Graphics udostępnia kilka przeciążonych wersji metody DrawEllipse. Wszystkie te metody przyjmują obiekt Pen jako swój pierwszy argument. Pozostałe parametry służą do zdefiniowania prostokąta otaczającego elipsę. W tym przykładzie użyj wersji akceptującej obiekt Rectangle jako drugi parametr, by narysować elipsę za pomocą obiektu Pen w wybranym kolorze.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Narysuj wypełniony wielokąt**
Następnie narysuj wielokąt, używając LinearGradientBrush i tablicy punktów. Klasa Graphics udostępnia kilka przeciążonych wersji metody FillPolygon. Wszystkie te metody przyjmują obiekt Brush jako swój pierwszy argument, definiujący charakterystyki wypełnienia. Drugim parametrem jest tablica punktów. Zauważ, że każde dwa kolejne punkty w tablicy określają bok wielokąta.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Rysowanie obrazów za pomocą Graphics: Pełen kod źródłowy**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

Wszystkie klasy, które implementują interfejs IDisposable i mają dostęp do zasobów niezarządzanych, są tworzone w instrukcji Using, aby zapewnić poprawne zwolnienie zasobów.
