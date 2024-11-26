---
title: Utwórz obraz PSD lub PSB od podstaw używając Pythona
weight: 100
type: docs
description: Przykład tworzenia obrazu Psd Image od podstaw za pomocą Aspose.PSD dla Pythona
keywords: [utwórz psd, utwórz psb, utwórz nowy, utwórz warstwę, utwórz warstwę tekstową, psd api, python, przykład kodu]
url: pl/python-net/utworz-obrazy-psd-psb-od-podstaw/
---

## **Opis**
Aby stworzyć plik PSD lub PSB od podstaw za pomocą Aspose.PSD dla Pythona, wystarczy postępować zgodnie z poniższymi krokami:

Zaimportuj wymagane moduły i klasy z biblioteki Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Określ nazwę i ścieżkę pliku wyjściowego:

```python 
outputFile = "PrzykladowyPlik.psd"
```

Utwórz obraz PSD o pożądanych wymiarach:

```python 
with PsdImage(500, 500) as img:
```

Dodaj zwykłą warstwę PSD i zaktualizuj ją przy użyciu interfejsu graficznego:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Utwórz warstwę tekstową:
```python 
textLayer = img.add_text_layer("Przykładowy Tekst", Rectangle(200, 200, 100, 100))
```

Dodaj efekt cienia opadającego do warstwy tekstowej:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Zapisz plik PSD:
```python 
img.save(outputFile)
```

Ten kod tworzy obraz PSD o wymiarach 500x500 pikseli. Dodaje zwykłą warstwę i rysuje na niej elipsę przy użyciu pióra i pędzla. Następnie dodaje warstwę tekstową z tekstem "Przykładowy Tekst" oraz dodaje efekt cienia opadającego do niej. Na końcu zapisuje plik PSD z określoną nazwą pliku wyjściowego.

Zauważ, że aby ten kod działał, musisz mieć zainstalowaną bibliotekę Aspose.PSD i właściwie skonfigurowane środowisko Pythona. Możesz odnieść się do oficjalnej dokumentacji Aspose.PSD w celu uzyskania dalszych informacji na temat instalacji i użycia tej biblioteki.

Proszę sprawdź pełny przykład.

## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentacja-Python-Aspose-Psd-utworz-obrazy-psd-psb-od-podstaw.py" >}}
