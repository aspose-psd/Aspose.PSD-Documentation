---
title: Korzystanie z interfejsu API graficznego do edycji warstw w plikach PSD
weight: 100
type: docs
description: Przykład użycia interfejsu API graficznego w Aspose.PSD dla języka Python
keywords: [aktualizacja warstwy, rysowanie koła, rysowanie elipsy, rysowanie wypełnionego koła, grafika, api psd, python, przykład kodu]
url: pl/python-net/graphics-api/
---

## **Przegląd**
Najpierw musisz załadować plik PSD używając metody Image.load() lub utworzyć obraz Psd od podstaw. W przykładzie zmienna inputFile reprezentuje ścieżkę do pliku PSD, a loadOpt reprezentuje opcje ładowania (jeśli takie istnieją).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Następnie możesz uzyskać dostęp do pierwszej warstwy obrazu PSD, używając składni psdImage.layers[0]. Daje to odwołanie do obiektu warstwy, który można manipulować.

```python 
layer = psdImage.layers[0]
```
Aby edytować warstwę, musisz utworzyć obiekt Graphics, przekazując warstwę jako parametr. Ten obiekt udostępnia różne metody do rysowania kształtów i stosowania pędzli.

```python 
graphics = Graphics(layer)
```
W przykładowym kodzie, obiekt Pen jest tworzony, aby zdefiniować kolor i grubość linii kształtu elipsy. Stała Color.alice_blue reprezentuje kolor, a grubość można dostosować według potrzeb.

```python 
pen = Pen(Color.alice_blue)
```
Podobnie, tworzony jest obiekt LinearGradientBrush, aby zdefiniować kolor wypełnienia kształtu elipsy. Rectangle(250, 250, 150, 100) reprezentuje pozycję i rozmiar kształtu elipsy, a Color.red i Color.aquamarine reprezentują kolory początkowy i końcowy gradientu.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Aby narysować kształt elipsy na warstwie, można użyć metody graphics.draw_ellipse(). Rectangle(100, 100, 200, 200) reprezentuje pozycję i rozmiar kształtu elipsy.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Aby wypełnić kształt elipsy za pomocą pędzla gradientowego, można użyć metody graphics.fill_ellipse(). Rectangle(250, 250, 150, 100) reprezentuje pozycję i rozmiar kształtu elipsy.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Po wprowadzeniu pożądanych zmian na warstwie, można zapisać zmodyfikowany obraz PSD, używając metody psdImage.save(). W przykładzie zmienna psdName reprezentuje ścieżkę do zapisania zmodyfikowanego pliku PSD.

```python 
psdImage.save(psdName)
```
Dodatkowo można również zapisać zmodyfikowany obraz w innych formatach, takich jak PNG, korzystając z klasy PngOptions. Zmienna pngName reprezentuje ścieżkę do zapisania pliku PNG.

```python 
psdImage.save(pngName, PngOptions())
```
To wszystko! Skutecznie użyłeś interfejsu API graficznego Aspose.PSD dla języka Python, aby edytować warstwy w pliku PSD. Zachęcam do odkrywania więcej funkcji i możliwości biblioteki Aspose.PSD, aby wzmocnić swoje możliwości edycji obrazów.

Proszę sprawdź pełny przykład.

## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}

