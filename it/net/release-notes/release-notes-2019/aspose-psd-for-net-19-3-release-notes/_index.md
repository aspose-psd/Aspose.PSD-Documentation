---
title: Note sulla release di Aspose.PSD per .NET 19.3
type: docs
weight: 100
url: /it/net/aspose-psd-per-net-19-3-note-sulla-release/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla release di Aspose.PSD per .NET 19.3

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-104|Rendering di livelli di testo ruotati da TransformMatrix|Funzionalità|
|PSDNET-96|Implementa il rendering dell'effetto Stroke con riempimento colore per l'esportazione|Funzionalità|
|PSDNET-112|I trasformatori InnerData corrompono alcuni livelli con maschere vettoriali|Errore|
|PSDNET-113|L'aggiornamento del livello di testo per l'immagine PSD genera un errore quando aperto in Photoshop|Errore|

## **Modifiche all'API pubblica**
# **API aggiuntive:**
- Nessuna
# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**
**PSDNET-104. Rendering di livelli di testo ruotati da TransformMatrix**

{{< highlight java >}}

 string sourceFileName = "TestoTrasformato.psd";

string exportPath = "EsportazioneTestoTrasformato.psd";

string exportPathPng = "EsportazioneTestoTrasformato.png";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 im.Save(exportPath);

 im.Save(exportPathPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Implementa il rendering dell'effetto Stroke con riempimento colore per l'esportazione**

{{< highlight java >}}

  // Implementa il rendering dell'effetto Stroke con riempimento colore per l'esportazione

 string sourceFileName = "StrokeComplesso.psd";

 string exportPath = "RenderingStrokeComplesso.psd";

 string exportPathPng = "RenderingStrokeComplesso.png";

 var loadOptions = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(sourceFileName, loadOptions)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var effect = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var settings = (ColorFillSettings) effect.FillSettings;

   settings.Color = Color.DeepPink;

  }

  // Salva psd

  im.Save(exportPath, new PsdOptions());

  // Salva png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. I trasformatori InnerData corrompono alcuni livelli con maschere vettoriali**

{{< highlight java >}}

 // I trasformatori InnerData corrompono alcuni livelli con maschere vettoriali

var sourceFile = "1.psd";

var pngPath = "RotateFlipTest2617.png";

var psdPath = "RotateFlipTest2617.psd";

var flipType = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(sourceFile))) {

 im.RotateFlip(flipType);

 im.Save(pngPath, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(psdPath);

}

{{< /highlight >}}

**PSDNET-113. L'aggiornamento del livello di testo per l'immagine PSD genera un errore quando aperto in Photoshop**

{{< highlight java >}}

 string sourceFileName = "Test.psd";

string exportPath = "Risultato.psd";

using(Image image = Image.Load(sourceFileName)) {

 if (!(image is PsdImage)) {

  return;

 }

 PsdImage psdImage = (PsdImage) image;

 Layer[] layers = psdImage.Layers;

 for (int index = layers.Length - 1; index >= 0; index--) {

  Layer layer = layers[index];

  if (!(layer is TextLayer)) {

   continue;

  }

  TextLayer textLayer = (TextLayer) layer;

  textLayer.UpdateText("\\()");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// Il file deve essere aperto senza eccezioni e deve essere leggibile per Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
