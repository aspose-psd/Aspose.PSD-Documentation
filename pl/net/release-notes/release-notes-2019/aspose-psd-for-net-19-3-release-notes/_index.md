---
title: Aspose.PSD dla .NET 19.3 - Notatki dotyczące wydania
type: docs
weight: 100
url: /pl/net/aspose-psd-dla-net-19-3-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki dotyczące wydania Aspose.PSD dla .NET 19.3

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-104|Renderowanie obróconych warstw tekstowych przez TransformMatrix|Funkcja|
|PSDNET-96|Implementacja renderowania efektu Skalowania z wypełnieniem koloru do eksportu|Funkcja|
|PSDNET-112|Transformer InnerData psują niektóre warstwy z maskami wektorowymi|Błąd|
|PSDNET-113|Aktualizacja warstwy tekstowej w obrazie PSD powoduje błąd podczas otwierania w programie Photoshop|Błąd|

## **Zmiany w publicznym API**
# **Dodane API:**
- Brak
# **Usunięte API:**
- Brak

## **Przykłady użycia:**
**PSDNET-104. Renderowanie obróconych warstw tekstowych przez TransformMatrix**

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

**PSDNET-96. Implementacja renderowania efektu Skalowania z wypełnieniem koloru do eksportu**

{{< highlight java >}}

  // Implementacja renderowania efektu Skalowania z wypełnieniem koloru do eksportu

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

  // Zapisz psd

  im.Save(exportPath, new PsdOptions());

  // Zapisz png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Transformer InnerData psują niektóre warstwy z maskami wektorowymi**

{{< highlight java >}}

 // Transformer InnerData psują niektóre warstwy z maskami wektorowymi

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

**PSDNET-113. Aktualizacja warstwy tekstowej w obrazie PSD powoduje błąd podczas otwierania w programie Photoshop**

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

// Plik musi być otwarty bez wyjątku i musi być możliwy do odczytania przez Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
