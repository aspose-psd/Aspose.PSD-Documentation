---
title: Aspose.PSD для .NET 19.3 - Примітки до випуску
type: docs
weight: 100
url: /uk/net/aspose-psd-dlya-net-19-3-vipusknі-prіmіtkи/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до випуску Aspose.PSD для .NET 19.3

{{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-104|Відтворення обертаних шарів тексту за допомогою TransformMatrix|Функціонал|
|PSDNET-96|Реалізація відтворення ефекту Штрих з наповненням кольором для експорту|Функціонал|
|PSDNET-112|Transformer InnerData пошкоджує деякі шари з векторними масками|Помилка|
|PSDNET-113|Оновлення текстового шару для зображення PSD викликає помилку при відкритті в Photoshop|Помилка|

## **Зміни в публічному API**
# **Додані API:**
- None
# **Видалені API:**
- None

## **Приклади використання:**
**PSDNET-104. Відтворення обертаних шарів тексту за допомогою TransformMatrix**

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

**PSDNET-96. Реалізація відтворення ефекту Штрих з наповненням кольором для експорту**

{{< highlight java >}}

  // Реалізація відтворення ефекту Штрих з наповненням кольором для експорту

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

  // Зберегти psd

  im.Save(exportPath, new PsdOptions());

  // Зберегти png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Transformer InnerData пошкоджує деякі шари з векторними масками**

{{< highlight java >}}

 // Transformer InnerData пошкоджує деякі шари з векторними масками

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

**PSDNET-113. Оновлення текстового шару для зображення PSD викликає помилку при відкритті в Photoshop**

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

// Файл повинен відкриватися без винятків і доступний для читання у Photoshop

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
