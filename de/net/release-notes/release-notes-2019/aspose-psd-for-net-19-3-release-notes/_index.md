---
title: Aspose.PSD für .NET 19.3 - Versionshinweise
type: docs
weight: 100
url: /de/net/aspose-psd-für-net-19-3-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält die Versionshinweise für Aspose.PSD für .NET 19.3

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-104|Rendering von Textebenen, die durch TransformMatrix rotiert sind|Feature|
|PSDNET-96|Implementierung der Darstellung des Strich-Effekts mit Farbfüllung für den Export|Feature|
|PSDNET-112|InnerData Transformers beschädigen einige Ebenen mit Vektormasken|Fehler|
|PSDNET-113|Aktualisierung der Textebene für PSD-Bild wirft einen Fehler auf, wenn sie in Photoshop geöffnet wird|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- Keine
# **Entfernte APIs:**
- Keine

## **Beispiel zur Verwendung:**
**PSDNET-104. Rendering von Textebenen, die durch TransformMatrix rotiert sind**

{{< highlight java >}}

 string sourceFileName = "TransformedText.psd";

string exportPath = "TransformedTextExport.psd";

string exportPathPng = "TransformedTextExport.png";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 im.Save(exportPath);

 im.Save(exportPathPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Implementierung der Darstellung des Strich-Effekts mit Farbfüllung für den Export**

{{< highlight java >}}

  // Implementierung der Darstellung des Strich-Effekts mit Farbfüllung für den Export

 string sourceFileName = "StrokeComplex.psd";

 string exportPath = "StrokeComplexRendering.psd";

 string exportPathPng = "StrokeComplexRendering.png";

 var loadOptions = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(sourceFileName, loadOptions)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var effect = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var settings = (ColorFillSettings) effect.FillSettings;

   settings.Color = Color.DeepPink;

  }

  // PSD speichern

  im.Save(exportPath, new PsdOptions());

  // PNG speichern

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. InnerData Transformers beschädigen einige Ebenen mit Vektormasken**

{{< highlight java >}}

 // InnerData Transformers beschädigen einige Ebenen mit Vektormasken

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

**PSDNET-113. Aktualisierung der Textebene für PSD-Bild wirft einen Fehler auf, wenn sie in Photoshop geöffnet wird**

{{< highlight java >}}

 string sourceFileName = "Test.psd";

string exportPath = "Result.psd";

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

// Datei muss ohne Ausnahme geöffnet und für Photoshop lesbar sein

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
