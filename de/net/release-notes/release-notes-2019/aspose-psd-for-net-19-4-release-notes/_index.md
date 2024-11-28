---
title: Aspose.PSD für .NET 19.4 - Versionshinweise
type: docs
weight: 90
url: /de/net/aspose-psd-für-net-19-4-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.PSD für .NET 19.4

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-87|Funktion zum Laden von JPEG/PNG/etc. Bilddateien zu PsdImage ohne direktes Laden hinzufügen (was von Aspose.PSD nicht unterstützt wird)|Funktion|
|PSDNET-120|Unterstützung des RGB-Farbraums mit 16 Bits/Kanal (64 Bits pro Farbe)|Funktion|
|PSDNET-108|Unterstützung von Vektormasken und individuellem FlipRotate für Ebenen|Funktion|
|PSDNET-99|Alle asiatischen Zeichen werden nicht korrekt gerendert|Fehler|
|PSDNET-116|Das Symbol \r\n wird als doppelte Zeilenumbruchzeichen interpretiert, das ist falsch|Fehler|
|PSDNET-117|Wenn ein TextLayer mit einem String aktualisiert wird, der Zeilenumbrüche enthält, wird die PSD-Datei unlesbar|Fehler|
|PSDNET-118|Wenn ein TextLayer mit einem String aktualisiert wird, der Tabulatorzeichen enthält, schlägt die Verarbeitung mit einer Ausnahme fehl|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
# **Entfernte APIs:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTrailer
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsPaletteSorted
- P:Aspose.PSD.FileFormats.Gif.GifImage.PaletteColorResolutionBits
- P:Aspose.PSD.FileFormats.Gif.GifImage.Width
- P:Aspose.PSD.FileFormats.Gif.GifImage.Height
- P:Aspose.PSD.FileFormats.Gif.GifImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.GifImage.Blocks
- P:Aspose.PSD.FileFormats.Gif.GifImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColorIndex
- P:Aspose.PSD.FileFormats.Gif.GifImage.PixelAspectRatio
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsCached
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.TransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasBackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.ImageOpacity
- M:Aspose.PSD.FileFormats.Gif.GifImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.CacheData
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.OrderBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.ClearBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.InsertBlock(System.Int32,Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AddBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RemoveBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Grayscale
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceNonTransparentColors(System.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double,System.Int32)
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasAlpha
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.FileFormat
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.PremultiplyComponents
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ByteOrder
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HorizontalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.VerticalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Frames
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Height
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Width
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.IsCached
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ExifData
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ImageOpacity
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.XmpData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AlignResolutions
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.SetResolution(System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.CacheData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Add(Aspose.PSD.FileFormats.Tiff.TiffImage)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrames(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.InsertFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeWidthProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeHeightProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Grayscale
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)

## **Beispiele zur Verwendung:**
**PSDNET-87. Feature zum Laden von JPEG/PNG/etc. Bilddateien zu PsdImage ohne direktes Laden hinzufügen (was von Aspose.PSD nicht unterstützt wird)**

{{< highlight java >}}

 string filePath = "PsdBeispiel.psd";

string outputFilePath = "PsdErgebnis.psd";

using(var image = new PsdImage(200, 200)) {

 using(var im = Image.Load(filePath)) {

  Layer layer = null;

  try {

   layer = new Layer((RasterImage) im);

   image.AddLayer(layer);

  } catch (Exception e) {

   if (layer != null) {

    layer.Dispose();

   }

   throw;

  }

 }

 image.Save(outputFilePath);

}  

{{< /highlight >}}

**PSDNET-120. Unterstützung des RGB-Farbraums mit 16 Bits/Kanal (64 Bits pro Farbe)**

{{< highlight java >}}

  // Unterstützung des RGB-Farbraums mit 16 Bits/Kanal (64 Bits pro Farbe)

string sourceFileName = "inRgb16.psd";

string outputFilePathJpg = "outRgb16.jpg";

string outputFilePathPsd = "outRgb16.psd";

var options = new PsdLoadOptions();

using(PsdImage image = (PsdImage) Image.Load(sourceFileName, options)) {

 image.Save(outputFilePathPsd, new PsdOptions(image));

 image.Save(outputFilePathJpg, new JpegOptions() {

  Quality = 100

 });

}

// Dateien müssen ohne Ausnahme geöffnet werden und für Photoshop lesbar sein    

using(Image image = Image.Load(outputFilePathPsd)) {}  

{{< /highlight >}}

**PSDNET-108. Unterstützung von Vektormasken und individuellem FlipRotate für Ebenen**

{{< highlight java >}}

 // Die RotateFlip-Operation funktioniert bei PSD nicht wie erwartet

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

**PSDNET-99. Alle asiatischen Zeichen werden nicht korrekt gerendert**

[**Bitte überprüfen Sie das angehängte Beispiel**](attachments/86278147/86343681.cs)

**PSDNET-116. Das Symbol \r\n wird als doppelte Zeilenumbruchzeichen interpretiert, das ist falsch**

{{< highlight java >}}

 // Das Symbol \r\n wird als doppelte Zeilenumbruchzeichen interpretiert, das ist falsch

string sourceFileName = "TextTest.psd";

string exportPath = "Ergebnis.psd";

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

  textLayer.UpdateText("Erster Absatz\r\nZweiter Absatz\rDritter Absatz\nVierter Absatz");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// Datei muss ohne Ausnahme geöffnet werden und für Photoshop lesbar sein. Sie muss 3 Zeilenumbrüche enthalten, einen zwischen jeder Zeile

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}

**PSDNET-117. Wenn ein TextLayer mit einem String aktualisiert wird, der Zeilenumbrüche enthält, wird die PSD-Datei unlesbar**

{{< highlight java >}}

 // Wenn ein TextLayer mit einem String aktualisiert wird, der Zeilenumbrüche enthält, wird die PSD-Datei unlesbar.

string sourceFileName = "TextTest.psd";

string exportPath = "Ergebnis.psd";

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

  textLayer.UpdateText("Erster Absatz\r\nZweiter Absatz\r\nDritter Absatz\r\nVierter Absatz");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// Datei muss ohne Ausnahme geöffnet werden und für Photoshop lesbar sein

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}

**PSDNET-118. Wenn ein TextLayer mit einem String aktualisiert wird, der Tabulatorzeichen enthält, schlägt die Verarbeitung mit einer Ausnahme fehl**

{{< highlight java >}}

 // Wenn ein TextLayer mit einem String aktualisiert wird, der Tabulatorzeichen enthält, schlägt die Verarbeitung mit einer Ausnahme fehl

string sourceFileName = "TextTest.psd";

string exportPath = "Ergebnis.psd";

using(Image image = Image.Load(sourceFileName)) {

 if (!(image is PsdImage)) {

  return;

 }

 PsdImage psdImage = (PsdImage) image;

 Layer[] layers = psdImage.Layers;

 for (int index = layers.Length - 1; index >= 0; index--) {

  Layer layer = layers[index];

  if (!(layer is TextLayer)) {

  