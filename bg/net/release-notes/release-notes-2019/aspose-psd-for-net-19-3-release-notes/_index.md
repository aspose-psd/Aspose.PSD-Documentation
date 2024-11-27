---
title: Aspose.PSD за .NET 19.3 - Бележки за версията
type: docs
weight: 100
url: /bg/net/aspose-psd-za-net-19-3-belejki-za-versijata/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за версията на Aspose.PSD за .NET 19.3

{{% /alert %}} 

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-104|Визуализация на текстови слоеве, завъртени с TransformMatrix|Функционалност|
|PSDNET-96|Изпълнение на визуализиране на ефект на обиране с цветно попълване за износ|Функционалност|
|PSDNET-112|InnerData Transformers разваля някои слоеве с векторни маски|Проблем|
|PSDNET-113|Актуализация на текстов слой за PSD изображение предизвиква грешка при отваряне в Photoshop|Проблем|

## **Промени в публичното API**
# **Добавени API:**
- Няма
# **Премахнати API:**
- Няма

## **Примери за използване:**
**PSDNET-104. Визуализация на текстови слоеве, завъртени с TransformMatrix**

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

**PSDNET-96. Изпълнение на визуализиране на ефект на обиране с цветно попълване за износ**

{{< highlight java >}}

  // Изпълнение на визуализиране на ефект на обиране с цветно попълване за износ

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

  // Запазване на psd

  im.Save(exportPath, new PsdOptions());

  // Запазване на png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. InnerData Transformers разваля някои слоеве с векторни маски**

{{< highlight java >}}

 // InnerData Transformers разваля някои слоеве с векторни маски

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

**PSDNET-113. Актуализация на текстов слой за PSD изображение предизвиква грешка при отваряне в Photoshop**

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

// Файлът трябва да може да бъде отворен без изключение и да бъде четлив за Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
