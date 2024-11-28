---
title: Aspose.PSD voor .NET 19.3 - Release-opmerkingen
type: docs
weight: 100
url: /nl/net/aspose-psd-voor-net-19-3-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor Aspose.PSD voor .NET 19.3

{{% /alert %}}

|**Belangrijkste**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-104|Weergave van geroteerde tekstlagen door Transformatiematrix|Functie|
|PSDNET-96|Implementeer weergave van Slageffect met Kleurvulling voor export|Functie|
|PSDNET-112|InnerData Transformers beschadigen sommige lagen met vectormaskers|Fout|
|PSDNET-113|Het bijwerken van tekstlaag voor PSD-afbeelding veroorzaakt een fout bij het openen in Photoshop|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Geen
# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-104. Weergave van geroteerde tekstlagen door Transformatiematrix**

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

**PSDNET-96. Implementeer weergave van Slageffect met Kleurvulling voor export**

{{< highlight java >}}

  // Implementeer weergave van Slageffect met Kleurvulling voor export

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

  // Sla psd op

  im.Save(exportPath, new PsdOptions());

  // Sla png op

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }

{{< /highlight >}}

**PSDNET-112. InnerData Transformers beschadigen sommige lagen met vectormaskers**

{{< highlight java >}}

 // InnerData Transformers beschadigen sommige lagen met vectormaskers

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

**PSDNET-113. Het bijwerken van tekstlaag voor PSD-afbeelding veroorzaakt een fout bij het openen in Photoshop**

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

// Bestand moet zonder uitzondering worden geopend en leesbaar zijn voor Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
