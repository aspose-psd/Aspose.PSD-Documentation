---
title: Aspose.PSD для .NET 19.3 - Примечания к выпуску
type: docs
weight: 100
url: /ru/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for Aspose.PSD для .NET 19.3

{{% /alert %}} 

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-104|Рендеринг повернутых слоев текста по TransformMatrix|Функция|
|PSDNET-96|Реализация рендеринга эффекта обводки с заполнением цветом при экспорте|Функция|
|PSDNET-112|Перегрузка слоев с векторными масками InnerData Transformers|Ошибка|
|PSDNET-113|Обновление слоя текста для изображения PSD вызывает ошибку при открытии в Photoshop|Ошибка|

## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет
# **Удаленные API:**
- Нет

## **Примеры использования:**
**PSDNET-104. Рендеринг повернутых слоев текста по TransformMatrix**

{{< highlight java >}}

string sourceFileName = "TransformedText.psd";

string exportPath = "TransformedTextExport.psd";

string exportPathPng = "TransformedTextExport.png";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 im.Save(exportPath);

 im.Save(exportPathPng, new PngOptions() {

  ColorType = PngColorType.TrueColorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Реализация рендеринга эффекта обводки с заполнением цветом при экспорте**

{{< highlight java >}}

// Реализация рендеринга эффекта обводки с заполнением цветом при экспорте

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

 // Сохранить psd

 im.Save(exportPath, new PsdOptions());

 // Сохранить png

 im.Save(exportPathPng, new PngOptions() {

  ColorType = PngColorType.TrueColorWithAlpha

 });

 }         

{{< /highlight >}}

**PSDNET-112. Перегрузка слоев с векторными масками InnerData Transformers**

{{< highlight java >}}

 // Перегрузка слоев с векторными масками InnerData Transformers

var sourceFile = "1.psd";

var pngPath = "RotateFlipTest2617.png";

var psdPath = "RotateFlipTest2617.psd";

var flipType = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(sourceFile))) {

 im.RotateFlip(flipType);

 im.Save(pngPath, new PngOptions() {

  ColorType = PngColorType.TrueColorWithAlpha

 });

 im.Save(psdPath);

}

{{< /highlight >}}

**PSDNET-113. Обновление слоя текста для изображения PSD вызывает ошибку при открытии в Photoshop**

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

// Файл должен быть открыт без ошибок и читаемым for Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
