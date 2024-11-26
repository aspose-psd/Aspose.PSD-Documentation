---
title: Przycinanie, obracanie i zmiana rozmiaru obrazów
type: docs
weight: 40
url: /pl/net/przycinanie-obracanie-i-zmiana-rozmiaru-obrazow/
---

## **Przycinanie obrazów**
Przycinanie obrazu zazwyczaj odnosi się do usunięcia zewnętrznych części obrazu, aby poprawić jego kompozycję. Przycinanie może również być używane do wycięcia pewnej części obrazu w celu zwiększenia skupienia na określonym obszarze. Interfejs API Aspose.PSD obsługuje dwa różne podejścia do przycinania obrazów: za pomocą przesunięć i prostokąta.
### **Przycinanie za pomocą przesunięć**
Klasa [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) udostępnia przeciążoną wersję metody Crop, która przyjmuje 4 wartości całkowite określające Lewą, Prawą, Górną i Dolną stronę. Na podstawie tych czterech wartości metoda Crop przesuwa granice obrazu ku centrum obrazu, odrzucając zewnętrzną część. Poniższy fragment kodu demonstruje, jak przyciąć obraz za pomocą przesunięć.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Przycinanie za pomocą prostokąta**
Klasa [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) udostępnia inną przeciążoną wersję metody Crop, która przyjmuje instancję klasy Rectangle. Możesz wyciąć dowolną część obrazu, podając pożądane granice obiektowi Rectangle. Poniższy fragment kodu demonstruje, jak przyciąć dowolny obraz za pomocą prostokąta.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Obracanie i odbijanie obrazu**
Aspose.PSD dla .NET to łatwa w użyciu biblioteka, ponieważ dostarcza proste metody do wykonywania skomplikowanych operacji. Na przykład Aspose.PSD dla .NET udostępnia metodę RotateFlip dla swojej klasy bazowej Image, jeśli aplikacja wymaga obrócenia obrazu. Bez względu na format obrazu, biblioteka może wykonać określoną procedurę obracania i odbijania obrazu.
### **Obracanie obrazu**
Metodę Image.RotateFlip można użyć do obrócenia obrazu o 90/180/270 stopni i odbicia obrazu poziomo lub pionowo. Metoda Image.RotateFlip przyjmuje parametr RotateFlipType określający rodzaj obrotu i odbicia do zastosowania na obrazie. Kroki do wykonania obrotu i odbicia są proste, jak poniżej:

1. Wczytaj obraz za pomocą metody fabrycznej Load udostępnionej przez klasę Image.
1. Wywołaj metodę Image.RotateFlip, podając odpowiedni RotateFlipType.
1. Zapisz wyniki.

Poniższy przykład kodu demonstruje, jak ustawić właściwość RotateFlip obrazu oraz wyliczenie RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Obracanie obrazu o określonym kącie**
Interfejs API Aspose.PSD dla .NET udostępnia metodę Rotate klasy [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) do ułatwienia użytkownikom, którzy chcą obrócić obraz o określony kąt. W odróżnieniu od metody [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, metoda [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate przyjmuje trzy parametry:

1. Kąt obrotu: Parametr typu float określający kąt obrotu, o który ma zostać obrócony obraz. Dodatnia wartość obraca obraz zgodnie z ruchem wskazówek zegara; ujemna wartość wykonuje obrót przeciwnie do ruchu wskazówek zegara.
1. Proporcjonalne zmiany rozmiaru: Parametr typu Boolean określa, czy rozmiar obrazu ma być zmieniony zgodnie z projekcjami obrotowych prostokątów (punkty w narożach). Jeśli ustawione na false, wymiary obrazu pozostaną niezmienione, a obrócane są jedynie wewnętrzne treści obrazu.
1. Kolor tła: Parametr typu Color określa kolor, który ma być wypełniony w tle obróconego obrazu.

Poniższy fragment kodu demonstruje użycie metody [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Zmiana rozmiaru obrazów**
Ten artykuł demonstruje użycie Aspose.PSD dla .NET do wykonywania operacji zmiany rozmiaru obrazu. Interfejsy API Aspose.PSD udostępniają skuteczne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD dla .NET udostępnia metodę Resize dla klasy Image, która może być użyta do dynamicznej zmiany rozmiaru istniejących obrazów. Istnieją dwie przeciążenia metody Resize, aby dostosować się do potrzeb aplikacji.
### **Prosta zmiana rozmiaru**
Kroki do wykonania zmiany rozmiaru są proste, jak poniżej:

1. Wczytaj obraz za pomocą metody fabrycznej Load udostępnionej przez klasę Image.
1. Wywołaj metodę Image.Resize, podając nową Wysokość i Szerokość.
1. Zapisz wyniki.

Poniższy przykład kodu demonstruje, jak zmienić rozmiar obrazu.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **Zmiana rozmiaru z użyciem wyliczenia ResizeType**
Interfejs API Aspose.PSD udostępnia wyliczenie ResizeType, które może być użyte z metodą Image.Resize, aby osiągnąć pożądane rezultaty. Poniższy fragment kodu demonstruje użycie wyliczenia ResizeType, natomiast szczegóły elementów wyliczenia ResizeType można znaleźć na dole tej strony.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



Jeśli zamierzasz uzyskać wysokiej jakości wynik po zastosowaniu zmiany rozmiaru, zaleca się zawsze korzystanie z ResizeType.LanczosResample, ponieważ generuje on wysokiej jakości wyniki, ale może działać wolniej niż ResizeType.NearestNeighbourResample. Z drugiej strony algorytm ResizeType.NearestNeighbourResample jest używany specjalnie do szybkiej zmiany rozmiaru kosztem jakości obrazu. Metoda ta może być przydatna do generowania miniatur w czasie rzeczywistym lub podobnych procesów, gdzie wymagana jest wydajność.
## **Proporcjonalna zmiana rozmiaru obrazu**
Możesz zmieniać rozmiar obrazów, wprowadzając nowe wartości wysokości i szerokości jako parametry do metody Image.Resize, ale wtedy musisz samodzielnie obliczyć proporcje aspektowe. Dzieje się tak dlatego, że gdy szerokość lub wysokość obrazu jest zmieniana, obraz jest skalowany lub zmniejszany, aby wypełnić nowy rozmiar. Jeśli zmiany szerokości i wysokości obrazu nie są proporcjonalne, może to prowadzić do rozciągniętego i zniekształconego rezultatu. Ten artykuł demonstruje użycie interfejsu API Aspose.PSD dla .NET do zmiany rozmiaru obrazów, przekazując jako parametr nową wysokość lub szerokość, pozwalając interfejsowi API automatycznie obliczyć drugą wartość proporcjonalną.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Wyliczenie ResizeType**
ResizeType określa rodzaj zmiany rozmiaru obrazu na podstawie wybranego filtru.

Elementy wyliczenia [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**Nazwa elementu**|**Wartość**|**Opis**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Lewy górny punkt nowego obrazu będzie pokrywał się z lewym górnym punktem oryginalnego obrazu. Zachodzi przycięcie, jeśli jest to wymagane.|
|RightTopToRightTop|1|Prawy górny punkt nowego obrazu będzie pokrywał się z prawym górnym punktem oryginalnego obrazu. Zachodzi przycięcie, jeśli jest to wymagane.|
|RightBottomToRightBottom|2|Prawy dolny punkt nowego obrazu będzie pokrywał się z prawym dolnym punktem oryginalnego obrazu. Zachodzi przycięcie, jeśli jest to wymagane.|
|LeftBottomToLeftBottom|3|Lewy dolny punkt nowego obrazu będzie pokrywał się z lewym dolnym punktem oryginalnego obrazu. Zachodzi przycięcie, jeśli jest to wymagane.|
|CenterToCenter|4|Środek nowego obrazu będzie pokrywał się z centrum oryginalnego obrazu. Zachodzi przycięcie, jeśli jest to wymagane.|
|LanczosResample|5|Próbkowanie przy użyciu algorytmu Lanczosa przy użyciu maski 7x7.|
|NearestNeighbourResample|6|Próbkowanie przy użyciu algorytmu najbliższego sąsiada.|

