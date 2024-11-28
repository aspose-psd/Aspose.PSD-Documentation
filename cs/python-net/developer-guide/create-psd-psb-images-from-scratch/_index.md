---
title: Vytvoření obrázku PSD nebo PSB od základu pomocí Pythonu
weight: 100
type: docs
description: Příklad, jak pomocí Aspose.PSD pro Python vytvořit obrazový soubor Psd od základu
keywords: [vytvořit psd, vytvořit psb, vytvořit nový, vytvořit vrstvu, vytvořit textovou vrstvu, psd api, python, ukázkový kód]
url: cs/python-net/create-psd-psb-images-from-scratch/
---

## **Přehled**
Pro vytvoření souboru PSD nebo PSB od základu pomocí Aspose.PSD pro Python můžete postupovat podle následujících kroků:

Importujte potřebné moduly a třídy z knihovny Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Specifikujte název výstupního souboru a cestu:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

Vytvořte obraz PSD s požadovanými rozměry:

```python 
with PsdImage(500, 500) as img:
```

Přidejte běžnou vrstvu PSD a aktualizujte ji pomocí grafického API:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Vytvořte textovou vrstvu:
```python 
textLayer = img.add_text_layer("Sample Text", Rectangle(200, 200, 100, 100))
```

Přidejte efekt stínovaného textu k textové vrstvě:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Uložte soubor PSD:
```python 
img.save(outputFile)
```

Tento kód vytváří obraz PSD s rozměry 500x500 pixelů. Přidává běžnou vrstvu a vykresluje na ni elipsu pomocí pera a štětce. Poté přidá textovou vrstvu s textem "Sample Text" a aplikuje na ni efekt stínování. Nakonec uloží soubor PSD s vybraným názvem výstupního souboru.

Všimněte si, že pro fungování tohoto kódu musíte mít knihovnu Aspose.PSD nainstalovanou a správně nakonfigurovanou ve svém prostředí Python. Pro více informací o instalaci a použití knihovny můžete konzultovat oficiální dokumentaci Aspose.PSD.

Zkontrolujte příklad.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
