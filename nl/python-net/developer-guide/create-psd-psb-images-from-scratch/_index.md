---
title: Maak PSD of PSB-afbeelding vanaf nul met behulp van Python
weight: 100
type: docs
description: Voorbeeld van hoe Aspose.PSD voor Python een Psd-afbeelding vanaf nul kan maken
keywords: [psd maken, psb maken, nieuwe maken, laag maken, tekstlaag maken, psd api, python, codevoorbeeld]
url: nl/python-net/maak-psd-psb-afbeeldingen-vanaf-nul/
---

## **Overzicht**
Om een PSD- of PSB-bestand vanaf nul te maken met behulp van Aspose.PSD voor Python, kunt u de onderstaande stappen volgen:

Importeer de benodigde modules en klassen uit de Aspose.PSD-bibliotheek:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Specificeer de outputbestandsnaam en -pad:

```python 
outputFile = "VoorbeeldbestandVanafNul.psd"
```
Maak een PSD-afbeelding met de gewenste dimensies:

```python 
with PsdImage(500, 500) as img:
```
Voeg een reguliere PSD-laag toe en werk deze bij met behulp van de grafische API:

```python 
reguliereLaag = img.add_regular_layer()
graphics = Graphics(reguliereLaag)
pen = Pen(Color.alice_blue)
kwast = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(kwast, Rectangle(250, 250, 150, 100))
```

Maak een tekstlaag:
```python 
tekstLaag = img.add_text_layer("Voorbeeldtekst", Rectangle(200, 200, 100, 100))
```

Voeg een schaduweffect toe aan de tekstlaag:
```python 
schaduweffect = tekstLaag.blending_options.add_drop_shadow()
schaduweffect.afstand = 0
schaduweffect.grootte = 8
schaduweffect.kleur = Color.blue
```

Sla het PSD-bestand op:
```python 
img.save(outputFile)
```

Deze code maakt een PSD-afbeelding met afmetingen van 500x500 pixels. Het voegt een reguliere laag toe en tekent hierop een ellips met behulp van een pen en een kwast. Vervolgens voegt het een tekstlaag toe met de tekst "Voorbeeldtekst" en past het een schaduweffect toe. Ten slotte slaat het het PSD-bestand op met de opgegeven outputbestandsnaam.

Let op dat je de Aspose.PSD-bibliotheek geïnstalleerd en correct geconfigureerd moet hebben in je Python-omgeving voor deze code om te werken. Je kunt de officiële Aspose.PSD-documentatie raadplegen voor meer informatie over hoe je de bibliotheek kunt installeren en gebruiken.

Controleer het volledige voorbeeld.

## **Voorbeeld**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentatie-Python-Aspose-Psd-maak-psd-psb-afbeeldingen-vanaf-nul.py" >}}
