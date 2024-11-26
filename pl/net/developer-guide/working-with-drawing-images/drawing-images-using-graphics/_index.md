---
title: Rysowanie obrazów przy użyciu Graphics
type: docs
weight: 20
url: /pl/net/rysowanie-obrazow-przy-uzyciu-graphics/
---

## **Rysowanie obrazów przy użyciu Graphics**
Dzięki bibliotece Aspose.PSD możesz rysować proste kształty, takie jak linie, prostokąty i koła, a także bardziej skomplikowane kształty, takie jak wielokąty, krzywe, łuki i kształty Beziera. Biblioteka Aspose.PSD tworzy takie kształty za pomocą klasy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), która znajduje się w przestrzeni nazw Aspose.PSD. Obiekty Graphics są odpowiedzialne za wykonywanie różnych operacji rysowania na obrazie, zmieniając tym samym powierzchnię obrazu. Klasa [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) korzysta z różnych obiektów pomocniczych, aby ulepszyć kształty:

·         Długopisy, do rysowania linii, konturów kształtów lub renderowania innych reprezentacji geometrycznych.

·         Pędzle, do definiowania, jakie obszary są wypełnione.

·         Czcionki, do definiowania kształtu znaków tekstu.
### **Rysowanie za pomocą klasy Graphics**
Poniżej znajduje się przykładowy kod demonstrowujący użycie klasy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Kod źródłowy przykładu został podzielony na kilka części, aby był prosty i łatwy do śledzenia. Krok po kroku przykłady pokazują, jak:

1. Utwórz obraz.
1. Utwórz i zainicjalizuj obiekt Graphics.
1. Wyczyść powierzchnię.
1. Narysuj elipsę.
1. Narysuj wypełniony wielokąt i zapisz obraz.
### **Przykłady programowania**
#### **Tworzenie obrazu**
Zacznij od utworzenia obrazu za pomocą dowolnej z metod opisanych w sekcji Utwórz pliki.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Utwórz i zainicjalizuj obiekt Graphics**
Następnie utwórz i zainicjalizuj obiekt Graphics, przekazując obiekt Image do jego konstruktora.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Wyczyść powierzchnię**
Wyczyść powierzchnię Graphics, wywołując metodę Clear klasy [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) i przekazując kolor jako parametr. Ta metoda wypełnia powierzchnię Graphics przekazanym kolorem jako argumentem.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Narysuj elipsę**
Zauważysz, że klasa [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) posiada wiele metod do rysowania i wypełniania kształtów. Znajdziesz pełną listę metod w Dokumentacji interfejsu API Aspose.PSD dla .NET. Klasa Graphics udostępnia kilka wersji przeciążonych metod metody DrawEllipse. Wszystkie te metody przyjmują obiekt Pen jako swój pierwszy argument. Pozostałe parametry służą do zdefiniowania prostokąta otaczającego elipsę. W celu tego przykładu użyj wersji przyjmującej obiekt Rectangle jako drugi parametr, aby narysować elipsę za pomocą obiektu Pen w wybranym kolorze.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Narysuj wypełniony wielokąt**
Następnie narysuj wielokąt, korzystając z LinearGradientBrush i tablicy punktów. Klasa Graphics udostępnia wiele przeciążonych wersji metody FillPolygon(). Wszystkie one przyjmują obiekt Brush jako swój pierwszy argument, definiujący charakterystyki wypełnienia. Drugim parametrem jest tablica punktów. Zauważ, że każde dwa kolejne punkty w tablicy określają bok wielokąta.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Rysowanie obrazów przy użyciu klasy Graphics: Pełne źródło**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Wszystkie klasy, które implementują IDisposable i uzyskują dostęp do zasobów zarządzanych, są tworzone w instrukcji Using, aby zapewnić poprawne zwolnienie zasobów.
