---
title: Notatki wydania Aspose.PSD dla .NET 19.4
type: docs
weight: 90
url: /pl/net/aspose-psd-for-net-19-4-release-notes/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla Aspose.PSD dla .NET 19.4

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-87|Dodano funkcję ładowania plików obrazów JPEG/PNG/itp. do PsdImage bez bezpośredniego ładowania (co nie jest obsługiwane w Aspose.PSD)|Funkcja|
|PSDNET-120|Wsparcie dla trybu koloru RGB z 16 bitami/kanał (64 bity na kolor)|Funkcja|
|PSDNET-108|Wsparcie dla warstw wektorowych masek i niestandardowego obrotu warstwy tekstowej|Funkcja|
|PSDNET-99|Wszystkie znaki azjatyckie nie są poprawnie renderowane|Błąd|
|PSDNET-116|Symbole \r\n są interpretowane jako podwójne podziały linii, co jest błędne|Błąd|
|PSDNET-117|Jeśli warstwa tekstowa zostanie zaktualizowana za pomocą ciągu zawierającego podziały linii, plik PSD staje się nieczytelny|Błąd|
|PSDNET-118|Jeśli warstwa tekstowa zostanie zaktualizowana za pomocą ciągu zawierającego symbole tabulatorów, przetwarzanie kończy się wyjątkiem|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
# **Usunięte API:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
...
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceNonTransparentColors(System.Int32)

## **Przykłady użycia:**
**PSDNET-87. Dodaj funkcję ładowania plików obrazów JPEG/PNG/itp. do PsdImage bez bezpośredniego ładowania (co nie jest obsługiwane w Aspose.PSD)**

{{< highlight java >}}

 string filePath = "PsdExample.psd";

string outputFilePath = "PsdResult.psd";

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

**PSDNET-120. Wsparcie dla trybu koloru RGB z 16 bitami/kanał (64 bity na kolor)**

{{< highlight java >}}

  // Wsparcie dla trybu koloru RGB z 16 bitami/kanał (64 bity na kolor)

string sourceFileName = "inRgb16.psd.psd";

string outputFilePathJpg = "outRgb16.jpg";

string outputFilePathPsd = "outRgb16.psd";

var options = new PsdLoadOptions();

using(PsdImage image = (PsdImage) Image.Load(sourceFileName, options)) {

 image.Save(outputFilePathPsd, new PsdOptions(image));

 image.Save(outputFilePathJpg, new JpegOptions() {

  Quality = 100

 });

}

// Pliki muszą być otwarte bez wyjątków i czytelnego dla Photoshopa  

using(Image image = Image.Load(outputFilePathPsd)) {}  

{{< /highlight >}}

**PSDNET-108. Wsparcie dla warstw wektorowych masek i niestandardowego obrotu warstwy tekstowej**

{{< highlight java >}}

 // Operacja RotateFlip nie działa zgodnie z oczekiwaniami dla plików PSD

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

**PSDNET-99. Wszystkie znaki azjatyckie nie są poprawnie renderowane**

[**Proszę sprawdzić załączony przykład**](attachments/86278147/86343681.cs)

**PSDNET-116. Symbole \r\n są interpretowane jako podwójne podziały linii, co jest błędne**

{{< highlight java >}}

 // Symbole \r\n są interpretowane jako podwójne podziały linii, co jest błędne

string sourceFileName = "TextTest.psd";

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

  textLayer.UpdateText("First Paragraph\r\nSecond Paragraph\rThird paragraph\nFourth Paragraph");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// Plik musi być otwarty bez wyjątków i czytelny dla Photoshopa. Musi zawierać 3 podziały linii, po jednym pomiędzy każdym wierszem

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}



**PSDNET-117. Jeśli warstwa tekstowa zostanie zaktualizowana za pomocą ciągu zawierającego podziały linii, plik PSD staje się nieczytelny**

{{< highlight java >}}

 // Jeśli warstwa tekstowa zostanie zaktualizowana za pomocą ciągu zawierającego podziały linii, plik PSD staje się nieczytelny.

string sourceFileName = "TextTest.psd";

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

  textLayer.UpdateText("First Paragraph\r\nSecond Paragraph\r\nThird paragraph\r\nFourth Paragraph");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// Plik musi być otwarty bez wyjątków i czytelny dla Photoshopa

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}



**PSDNET-118. Jeśli warstwa tekstowa zostanie zaktualizowana za pomocą ciągu zawierającego symbole tabulatorów, przetwarzanie kończy się wyjątkiem**

{{< highlight java >}}

 // Jeśli warstwa tekstowa zostanie zaktualizowana za pomocą ciągu zawierającego symbole tabulatorów, przetwarzanie kończy się wyjątkiem

string sourceFileName = "TextTest.psd";

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

  textLayer.UpdateText("Starting Text\tText After Tab");

 }

 PsdOptions imageOptions = new PsdOptions(psdImage);

 psdImage.Save(exportPath, imageOptions);

}

// Plik musi być otwarty bez wyjątków i czytelny dla Photoshopa

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}