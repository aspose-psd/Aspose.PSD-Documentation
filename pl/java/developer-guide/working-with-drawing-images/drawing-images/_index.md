---
title: Rysowanie obrazów
type: docs
weight: 10
url: /pl/java/rysunek-obrazow/
---

## **Rysowanie linii**
Ten przykład wykorzystuje klasę Graphics do rysowania kształtów linii na powierzchni obrazu. Aby zademonstrować operację, przykład tworzy nowy obraz i rysuje linie na powierzchni obrazu, używając metody DrawLine udostępnionej przez klasę Graphics. Najpierw utworzymy obraz PsdImage, określając jego wysokość i szerokość.

Gdy obraz zostanie utworzony, użyjemy metody Clear udostępnionej przez klasę Graphics, aby ustawić jego kolor tła. Metoda DrawLine klasy Graphics służy do rysowania linii na obrazie łączących dwie struktury punktów. Metoda ta ma kilka przeciążeń, akceptujących instancję klasy Pen oraz pary współrzędnych punktów lub struktury Point/PointF jako argumenty. Klasa Pen definiuje obiekt używany do rysowania linii, krzywych i figur. Klasa Pen ma kilka przeciążeń konstruktorów, aby rysować linie ze określonym kolorem, szerokością i pędzlem. Klasa SolidBrush jest używana do ciągłego rysowania w określonym kolorze. Na koniec obraz jest eksportowany do formatu pliku BMP. Poniższy fragment kodu pokazuje, jak rysować kształty linii na powierzchni obrazu.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}

## **Rysowanie elipsy**
Przykład rysowania elipsy to drugi artykuł z serii rysowania kształtów. Wykorzystamy klasę Graphics do rysowania kształtu elipsy na powierzchni obrazu. Aby zademonstrować operację, przykład tworzy nowy obraz i rysuje kształt elipsy na powierzchni obrazu, używając metody DrawEllipse udostępnionej przez klasę Graphics. Najpierw utworzymy obraz PsdImage, określając jego wysokość i szerokość.

Po utworzeniu obrazu, utworzymy i zainicjujemy obiekt klasy Graphics oraz ustawimy kolor tła obrazu za pomocą metody Clear klasy Graphics. Metoda DrawEllipse klasy Graphics służy do rysowania kształtu elipsy na powierzchni obrazu określonej przez strukturę prostokąta ograniczającego. Metoda ta ma kilka przeciążeń, akceptujących instancje klas Pen i Rectangle/RectangleF albo parę współrzędnych, wysokościę i szerokość jako argumenty. Klasa Pen definiuje obiekt używany do rysowania linii, krzywych i figur. Klasa Pen ma kilka przeciążeń konstruktorów, aby rysować linie ze określonym kolorem, szerokością i pędzlem. Klasa Rectangle przechowuje zestaw czterech liczb całkowitych reprezentujących położenie i rozmiar prostokąta. Klasa Rectangle ma kilka przeciążeń konstruktorów, aby narysować strukturę prostokąta ze określonym rozmiarem i położeniem. Klasa SolidBrush jest używana do ciągłego rysowania w określonym kolorze. Na koniec obraz jest eksportowany do formatu pliku BMP. Poniższy fragment kodu pokazuje, jak rysować kształt elipsy na powierzchni obrazu.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

## **Rysowanie prostokąta**
W tym przykładzie narysujemy kształt prostokąta na powierzchni obrazu. Aby zademonstrować operację, przykład tworzy nowy obraz i rysuje kształt prostokąta na powierzchni obrazu, używając metody DrawRectangle udostępnionej przez klasę Graphics. Najpierw utworzymy obraz PsdImage, określając jego wysokość i szerokość. Następnie ustalimy kolor tła obrazu za pomocą metody Clear klasy Graphics.

Metoda DrawRectangle klasy Graphics służy do rysowania kształtu prostokąta na powierzchni obrazu określonej przez strukturę prostokąta. Metoda ta ma kilka przeciążeń, akceptujących instancje klas Pen i Rectangle/RectangleF albo parę współrzędnych, szerokość i wysokość jako argumenty. Klasa Rectangle przechowuje zestaw czterech liczb całkowitych reprezentujących położenie i rozmiar prostokąta. Klasa Rectangle ma kilka przeciążeń konstruktorów, aby narysować strukturę prostokąta ze określonym rozmiarem i położeniem. Na koniec obraz jest eksportowany do formatu pliku BMP. Poniższy fragment kodu pokazuje, jak rysować kształt prostokąta na powierzchni obrazu.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}

## **Rysowanie łuku**
W tej części serii rysowania kształtów narysujemy kształt łuku na powierzchni obrazu. Użyjemy metody DrawArc klasy Graphics, aby zademonstrować operację na obrazie BMP. Najpierw utworzymy obraz PsdImage, określając jego wysokość i szerokość. Gdy obraz zostanie utworzony, użyjemy metody Clear udostępnionej przez klasę Graphics, aby ustawić jego kolor tła.

Metoda DrawArc klasy Graphics służy do rysowania kształtu łuku na powierzchni obrazu. Metoda DrawArc reprezentuje część elipsy określoną przez strukturę prostokąta lub parę współrzędnych. Ta metoda ma kilka przeciążeń, akceptujących instancje klas Pen oraz Rectangle/RectangleF albo parę współrzędnych, szerokość i wysokość jako argumenty. Na koniec obraz jest eksportowany do formatu pliku BMP. Poniższy fragment kodu pokazuje, jak rysować kształt łuku na powierzchni obrazu.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

## **Rysowanie krzywej Beziera**
Ten przykład wykorzystuje klasę Graphics do rysowania kształtów krzywych Beziera na powierzchni obrazu. Aby zademonstrować operację, przykład tworzy nowy obraz i rysuje kształt krzywej Beziera na powierzchni obrazu, używając metody DrawBezier udostępnionej przez klasę Graphics. Najpierw utworzymy obraz PsdImage, określając jego wysokość i szerokość. Gdy obraz zostanie utworzony, użyjemy metody Clear udostępnionej przez klasę Graphics, aby ustawić jego kolor tła.

Metoda DrawBezier klasy Graphics służy do rysowania kształtu krzywej Beziera na powierzchni obrazu zdefiniowanej przez cztery struktury Point. Ta metoda ma kilka przeciążeń, akceptujących instancje klasy Pen oraz cztery uporządkowane pary współrzędnych lub cztery struktury Point/PointF albo tablicę struktur Point/PointF. Klasa Pen definiuje obiekt używany do rysowania linii, krzywych i figur. Klasa Pen ma kilka przeciążeń konstruktorów, aby rysować linie ze określonym kolorem, szerokością i pędzlem. Na koniec obraz jest eksportowany do formatu pliku BMP. Poniższy fragment kodu pokazuje, jak rysować krzywą Beziera na powierzchni obrazu.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

## **Rysowanie obrazów za pomocą podstawowej funkcjonalności**
Aspose.PSD to biblioteka, która oferuje wiele wartościowych funkcji, w tym tworzenie obrazów od podstaw. Rysuj za pomocą podstawowej funkcjonalności, takiej jak manipulacja informacjami o mapie bitowej obrazu, lub korzystaj z zaawansowanych funkcji, takich jak Graphics i GraphicsPath, do rysowania kształtów na powierzchni obrazu za pomocą różnych pędzli i kredek. Korzystając z klasy RasterImage Aspose.PSD, możesz pobrać informacje o pikselach obszaru obrazu i nimi manipulować. Klasa RasterImage zawiera całą podstawową funkcjonalność rysowania, taką jak pobieranie i ustawianie pikseli oraz inne metody manipulacji obrazem. Utwórz nowy obraz, korzystając z dowolnej z metod opisanych w Tworzenie plików i przypisz go do instancji klasy RasterImage. Użyj metody LoadPixels klasy RasterImage, aby pobrać informacje o pikselach części obrazu. Gdy masz tablicę pikseli, możesz nią manipulować, zmieniając na przykład kolor każdego piksela. Po manipulacji informacjami o pikselach, ustaw je z powrotem w żądanym obszarze obrazu za pomocą metody SavePixels klasy RasterImage. Poniższy fragment kodu pokazuje, jak rysować obrazy za pomocą podstawowej funkcjonalności.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}
