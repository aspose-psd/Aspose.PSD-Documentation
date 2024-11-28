---
title: Použití Grafického API k úpravě vrstev v souborech PSD
weight: 100
type: docs
description: Příklad použití Grafického API v Aspose.PSD pro Python
keywords: [aktualizace vrstvy, kreslení kruhu, kreslení elipsy, kreslení vyplněného kruhu, grafika, psd api, python, ukázkový kód]
url: cs/python-net/graphics-api/
---

## **Přehled**
Nejprve musíte načíst soubor PSD pomocí metody Image.load() nebo vytvořit PNG obrázek od základu. V příkladu proměnná inputFile představuje cestu k vašemu souboru PSD a loadOpt představuje možnosti načítání (pokud existují).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Následně můžete přistupovat k první vrstvě obrázku PSD pomocí syntaxe psdImage.layers[0]. To vám poskytne odkaz na objekt vrstvy, se kterým můžete manipulovat.

```python 
layer = psdImage.layers[0]
```
Pro úpravu vrstvy musíte vytvořit objekt Graphics tím, že předáte vrstvu jako parametr. Tento objekt poskytuje různé metody pro kreslení tvarů a používání štětců.

```python 
graphics = Graphics(layer)
```
V kódu příkladu je vytvořen objekt Pen k definování barvy a tloušťky obrysu tvaru elipsy. Konstanta Color.alice_blue představuje barvu a můžete upravit tloušťku podle potřeby.

```python 
pen = Pen(Color.alice_blue)
```
Obdobně je vytvořen objekt LinearGradientBrush k definování barvy vyplnění tvaru elipsy. Rectangle(250, 250, 150, 100) představuje pozici a velikost tvaru elipsy a Color.red a Color.aquamarine představují začátek a konec barev gradientu.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Pro vykreslení tvaru elipsy na vrstvu můžete použít metodu graphics.draw_ellipse(). Rectangle(100, 100, 200, 200) představuje pozici a velikost tvaru elipsy.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Pro vyplnění tvaru elipsy gradientovým štětcem můžete použít metodu graphics.fill_ellipse(). Rectangle(250, 250, 150, 100) představuje pozici a velikost tvaru elipsy.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Po provedení požadovaných změn ve vrstvě můžete uložit upravený obrázek PSD pomocí metody psdImage.save(). V příkladu proměnná psdName představuje cestu k uložení upraveného souboru PSD.

```python 
psdImage.save(psdName)
```
Dodatečně můžete také uložit upravený obrázek v jiných formátech, jako je PNG, použitím třídy PngOptions. Proměnná pngName představuje cestu k uložení souboru PNG.

```python 
psdImage.save(pngName, PngOptions())
```
To je vše! Úspěšně jste použili Grafické API Aspose.PSD pro Python k úpravě vrstev v souboru PSD. Nebojte se objevovat další funkce a možnosti knihovny Aspose.PSD pro zlepšení vašich schopností úpravy obrázků.

Zkontrolujte si kompletní příklad.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentace-Python-Aspose-Psd-grafické-api.py " >}}
