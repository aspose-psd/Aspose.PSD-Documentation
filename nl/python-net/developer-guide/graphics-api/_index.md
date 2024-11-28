---
title: Gebruik van Graphics API om lagen in PSD-bestanden te bewerken
weight: 100
type: docs
description: Voorbeeld van het gebruik van de Graphics API in Aspose.PSD voor Python
keywords: [update laag, cirkel tekenen, ellips tekenen, gevulde cirkel tekenen, graphics, psd api, python, voorbeeldcode]
url: nl/python-net/graphics-api/
---

## **Overzicht**
Allereerst moet je het PSD-bestand laden met behulp van de Image.load() methode of een Psd Image vanaf nul maken. In het voorbeeld vertegenwoordigt de variabele inputFile het pad naar je PSD-bestand, en loadOpt vertegenwoordigt de laadopties (indien aanwezig).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Vervolgens kun je toegang krijgen tot de eerste laag van de PSD-afbeelding met behulp van de syntaxis psdImage.layers[0]. Dit geeft je een referentie naar het laagobject dat je kunt manipuleren.

```python 
layer = psdImage.layers[0]
```
Om de laag te bewerken, moet je een Graphics-object maken door de laag als parameter door te geven. Dit object biedt verschillende methoden om vormen te tekenen en penselen toe te passen.

```python 
graphics = Graphics(layer)
```
In het codevoorbeeld wordt een Pen-object gemaakt om de kleur en dikte van de omtrek van het ellipsvormige te definiëren. De constante Color.alice_blue vertegenwoordigt de kleur, en je kunt de dikte aanpassen zoals nodig is.

```python 
pen = Pen(Color.alice_blue)
```
Op vergelijkbare wijze wordt een LinearGradientBrush-object gemaakt om de vulkleur van de ellipsvormige te definiëren. De Rectangle(250, 250, 150, 100) vertegenwoordigt de positie en grootte van de ellipsvormige, en Color.red en Color.aquamarine vertegenwoordigen de start- en eindkleuren van de gradiënt.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Om de ellipsvormige te tekenen op de laag, kun je de methode graphics.draw_ellipse() gebruiken. De Rectangle(100, 100, 200, 200) vertegenwoordigt de positie en grootte van de ellipsvormige.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Om de ellipsvormige te vullen met de gradiëntkwast, kun je de methode graphics.fill_ellipse() gebruiken. De Rectangle(250, 250, 150, 100) vertegenwoordigt de positie en grootte van de ellipsvormige.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Nadat de gewenste wijzigingen aan de laag zijn aangebracht, kun je de aangepaste PSD-afbeelding opslaan met behulp van de methode psdImage.save(). In het voorbeeld vertegenwoordigt de variabele psdName het pad om het aangepaste PSD-bestand op te slaan.

```python 
psdImage.save(psdName)
```
Daarnaast kun je de aangepaste afbeelding ook opslaan in andere indelingen, zoals PNG, door de PngOptions-klasse te gebruiken. De variabele pngName vertegenwoordigt het pad om het PNG-bestand op te slaan.

```python 
psdImage.save(pngName, PngOptions())
```
Dat is het! Je hebt succesvol de Graphics API van Aspose.PSD voor Python gebruikt om lagen in een PSD-bestand te bewerken. Voel je vrij om meer functies en mogelijkheden van de Aspose.PSD-bibliotheek te verkennen om je beeldbewerkingsmogelijkheden te verbeteren.

Bekijk alsjeblieft het volledige voorbeeld.

## **Voorbeeld**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}
