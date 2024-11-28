---
title: הערות גרסה של Aspose.PSD עבור .NET 19.3
type: מסמכים
weight: 100
url: /he/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל את הערות הגרסה עבור Aspose.PSD עבור .NET 19.3

{{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-104|עיבוד שכבות טקסט באמצעות TransformMatrix שסובבות|תכונה|
|PSDNET-96|יישום עיבוד של אפקט Stroke עם Color Fill לייצוא|תכונה|
|PSDNET-112|משנה מתפזרת של מהטמות InnerData פוגעת במספר שכבות עם מסכות וקטוריות|תקלה|
|PSDNET-113|עידכון שכבת טקסט עבור תמונת PSD גורם לשגיאה בפתיחה בפוטושופ|תקלה|

## **שינויים ב- API הציבורי**
# **APIs שנוספו:**
- אין
# **APIs שהוסרו:**
- אין

## **דוגמאות לשימוש:**
**PSDNET-104. עיבוד של שכבות טקסט שסובבות באמצעות TransformMatrix**

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

**PSDNET-96. יישום של אפקט Stroke עם Color Fill לייצוא**

{{< highlight java >}}

  // יישום של אפקט Stroke עם Color Fill לייצוא

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

  // שמירה בפורמט psd

  im.Save(exportPath, new PsdOptions());

  // שמירה בפורמט png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. המהפכניות של InnerData מפגינות תקלות במספר שכבות עם מסכות וקטוריות**

{{< highlight java >}}

 // המהפכניות של InnerData מפגינות תקלות במספר שכבות עם מסכות וקטוריות

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

**PSDNET-113. עדכון שכבת טקסט בתמונת PSD מפיץ תקלה בפתיחה בפוטושופ**

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

// הקובץ צריך להיפתח ללא תקלות ולהיות נקרא על ידי פוטושופ

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
