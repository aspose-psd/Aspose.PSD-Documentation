---
title: Przycinanie, obracanie i zmiana rozmiaru obrazów
type: docs
weight: 40
url: /pl/java/przycinanie-obracanie-i-zmiana-rozmiaru-obrazow/
---

## **Przycinanie obrazów**
Przycinanie obrazu zazwyczaj odnosi się do usunięcia zewnętrznych części obrazu, aby poprawić kompozycję. Przycinanie może być również stosowane do wycięcia pewnej części obrazu w celu zwiększenia koncentracji na określonym obszarze. Interfejs API Aspose.PSD obsługuje dwa różne podejścia do przycinania obrazów: poprzez przesunięcia i prostokąt.
### **Przycinanie przez przesunięcia**
Klasa RasterImage udostępnia przeciążoną wersję metody Crop, która przyjmuje 4 wartości całkowite oznaczające Lewą, Prawą, Górną i Dolną. Na podstawie tych czterech wartości metoda Crop przesuwa granice obrazu w kierunku środka obrazu, odrzucając zewnętrzną część. Poniższy fragment kodu demonstruje, jak przyciąć obraz przez przesunięcia.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Przycinanie przez prostokąt**
Klasa RasterImage udostępnia inną przeciążoną wersję metody Crop, która przyjmuje instancję klasy Rectangle. Możesz wyciąć dowolną część obrazu, podając żądane granice obiektowi Rectangle. Poniższy fragment kodu demonstruje, jak przyciąć dowolny obraz przez prostokąt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Obracanie i odwracanie obrazu**
Aspose.PSD dla Javy to łatwa w użyciu biblioteka, ponieważ zapewnia proste metody do wykonywania skomplikowanych operacji. Na przykład, Aspose.PSD dla Javy dostarcza metodę RotateFlip dla swojej klasy bazowej Image, jeśli aplikacja wymaga obrotu obrazu. Bez względu na format obrazu, biblioteka może wykonać określoną procedurę obracania i odwracania na nim.
### **Obracanie obrazu**
Metoda Image.RotateFlip może być użyta do obracania obrazu o 90/180/270 stopni i odwracania obrazu poziomo lub pionowo. Metoda Image.RotateFlip przyjmuje parametr RotateFlipType, który określa rodzaj obrotu i odwrócenia do zastosowania na obrazie. Kroki do wykonania obrotu i odwrócenia są takie proste, jak poniżej:

1. Wczytaj obraz za pomocą metody fabrycznej Load dostępnej w klasie Image.
1. Wywołaj metodę Image.RotateFlip, określając odpowiedni RotateFlipType.
1. Zapisz wyniki.

Poniższy przykład kodu demonstruje, jak ustawić właściwość RotateFlip obrazu i enumerację RotateFlipType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Obracanie obrazu pod konkretnym kątem**
Interfejs API Aspose.PSD dla Javy udostępnia metodę RasterImage.Rotate umożliwiającą użytkownikom obracanie obrazu pod konkretnym kątem. W przeciwieństwie do metody RasterImage.RotateFlip, metoda RasterImage.Rotate przyjmuje trzy parametry:

1. Kąt obrotu: Parametr typu float, który określa kąt obrotu, o jaki należy obrócić obraz. Dodatnia wartość obraca obraz zgodnie z ruchem wskazówek zegara, a wartość ujemna wykonuje obrót przeciwnie do ruchu wskazówek zegara.
1. Proporcjonalne zmiany rozmiaru: Parametr typu Boolean określa, czy rozmiar obrazu ma być zmieniony zgodnie z projekcjami obróconego prostokąta (punkty narożne). Jeśli ustawiono na false, wymiary obrazu pozostaną niezmienione, a jedynie zawartość wewnętrzna obrazu zostanie obrócona.
1. Kolor tła: Parametr typu Color określa kolor, który ma zostać wypełniony w tle obróconego obrazu.

Poniższy fragment kodu demonstruje użycie metody RasterImage.Rotate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
