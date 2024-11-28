---
title: Utilizzo dell'API di grafica per modificare i livelli nei file PSD
weight: 100
type: docs
description: Esempio di utilizzo dell'API di grafica in Aspose.PSD per Python
keywords: [aggiornare il livello, disegnare cerchio, disegnare ellisse, disegnare cerchio di riempimento, grafica, api psd, python, esempio di codice]
url: it/python-net/api-di-grafica/
---

## **Panoramica**
Innanzitutto, è necessario caricare il file PSD utilizzando il metodo Load() dell'immagine o creare un'immagine Psd da zero. Nell'esempio, la variabile inputFile rappresenta il percorso del tuo file PSD, e loadOpt rappresenta le opzioni di caricamento (se presenti).

```python
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Successivamente, è possibile accedere al primo livello dell'immagine PSD utilizzando la sintassi psdImage.layers[0]. Ciò ti fornisce un riferimento all'oggetto livello che puoi manipolare.

```python
layer = psdImage.layers[0]
```
Per modificare il livello, è necessario creare un oggetto Grafica passando il livello come parametro. Questo oggetto fornisce vari metodi per disegnare forme e applicare pennelli.

```python
graphics = Graphics(layer)
```
Nell'esempio di codice, viene creato un oggetto Penna per definire il colore e lo spessore del contorno della forma ellisse. La costante Color.alice_blue rappresenta il colore e puoi regolare lo spessore secondo necessità.

```python
pen = Pen(Color.alice_blue)
```
Analogamente, viene creato un oggetto LinearGradientBrush per definire il colore di riempimento della forma ellisse. Il Rectangle(250, 250, 150, 100) rappresenta la posizione e le dimensioni della forma ellisse, mentre Color.red e Color.aquamarine rappresentano i colori di partenza e di fine del gradiente.

```python
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Per disegnare la forma ellisse sul livello, è possibile utilizzare il metodo graphics.draw_ellipse(). Il Rectangle(100, 100, 200, 200) rappresenta la posizione e le dimensioni della forma ellisse.

```python
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Per riempire la forma ellisse con il pennello a gradiente, è possibile utilizzare il metodo graphics.fill_ellipse(). Il Rectangle(250, 250, 150, 100) rappresenta la posizione e le dimensioni della forma ellisse.

```python
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Dopo aver apportato le modifiche desiderate al livello, è possibile salvare l'immagine PSD modificata utilizzando il metodo psdImage.save(). Nell'esempio, la variabile psdName rappresenta il percorso per salvare il file PSD modificato.

```python
psdImage.save(psdName)
```
Inoltre, è possibile salvare l'immagine modificata anche in altri formati, come PNG, utilizzando la classe PngOptions. La variabile pngName rappresenta il percorso per salvare il file PNG.

```python
psdImage.save(pngName, PngOptions())
```
È tutto! Hai utilizzato con successo l'API di grafica di Aspose.PSD per Python per modificare i livelli in un file PSD. Sentiti libero di esplorare ulteriori funzionalità della libreria Aspose.PSD per migliorare le tue capacità di modifica delle immagini.

Per favore, controlla l'esempio completo.

## **Esempio**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentazione-Python-Aspose-Psd-api-di-grafica.py" >}}
