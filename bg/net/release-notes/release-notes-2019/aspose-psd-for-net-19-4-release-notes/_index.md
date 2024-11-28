---
title: Aspose.PSD за .NET 19.4 - Бележки за изданието
type: docs
weight: 90
url: /bg/net/aspose-psd-za-net-19-4-belezhki-za-izdanieto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на Aspose.PSD за .NET 19.4

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-87|Добавяне на функция за зареждане на файлове с изображения JPEG/PNG и т.н. в PsdImage без директно зареждане(което не се поддържа в Aspose.PSD)|Функционалност|
|PSDNET-120|Поддръжка на цветовия режим RGB с 16 бита на канал (64 бита на цвят)|Функционалност|
|PSDNET-108|Поддръжка на Векторни маски за слой и Текстов слой за персонализирано завъртане и обръщане|Функционалност|
|PSDNET-99|Всички азиатски знаци не се изобразяват правилно|Проблем|
|PSDNET-116|Символите \r\n се интерпретират като двойна нова линия, което е грешно|Проблем|
|PSDNET-117|При актуализиране на TextLayer със символен низ, който съдържа прекъсвания на реда, файлът на PSD става нечетлив|Проблем|
|PSDNET-118|При актуализиране на TextLayer със символен низ, който съдържа символи за разделение с табулации, обработката се проваля с изключение|Проблем|

## **Промени в публичния API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
# **Премахнати API:**
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

## **Примери за използване:**
**PSDNET-87. Добавяне на функция за зареждане на JPEG/PNG и т.н. файлове с изображения в PsdImage без директно зареждане (което не се поддържа в Aspose.PSD)**

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

**PSDNET-120. Поддръжка на цветовия режим RGB с 16 бита на канал (64 бита на цвят)**

{{< highlight java >}}

  // Поддръжка на цветовия режим RGB с 16 бита на канал (64 бита на цвят)

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

// Файловете трябва да бъдат отворени без изключения и да бъдат четливи за Photoshop    

using(Image image = Image.Load(outputFilePathPsd)) {}  

{{< /highlight >}}

**PSDNET-108. Поддръжка на векторни маски за слоеве и персонализирано завъртане на текстов слой**

{{< highlight java >}}

 // Операцията за завъртане и обръщане не работи, както се очаква с PSD

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

**PSDNET-99. Всички азиатски знаци не се изобразяват правилно**

[**Моля, проверете прикачения пример**](attachments/86278147/86343681.cs)

**PSDNET-116. Символите \r\n се интерпретират като двойна нова линия, което е грешно**

{{< highlight java >}}

 // Символите \r\n се интерпретират като двойна нова линия, което е грешно

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

// Файлът трябва да бъде отворен без изключение и четим за Photoshop. Трябва да съдържа 3 реда разделени с нови линии, един между всеки ред

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}

**PSDNET-117. Ако TextLayer се актуализира със символен низ, който съдържа прекъсвания на реда, файлът на PSD става нечетлив**

{{< highlight java >}}

 // Ако TextLayer се актуализира със символен низ, който съдържа прекъсвания на реда, файлът на PSD става нечетлив.

string sourceFileName = "TextTest.psd";

string exportPath = "Result.p