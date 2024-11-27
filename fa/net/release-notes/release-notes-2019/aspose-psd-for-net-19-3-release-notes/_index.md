---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 19.3
type: docs
weight: 100
url: /fa/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های نسخه Aspose.PSD برای .NET 19.3 می‌باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-104|نمایش لایه‌های متنی با ماتریس تبدیل دوراندار|ویژگی|
|PSDNET-96|پیاده‌سازی اثر Stroke با پر کردن رنگ برای صادرات|ویژگی|
|PSDNET-112|تبدیل‌کننده‌های InnerData لایه‌هایی با ماسک برداری را خراب می‌کنند|باگ|
|PSDNET-113|به‌روزرسانی لایه متنی برای تصویر PSD خطا ایجاد می‌کند هنگام باز شدن در فتوشاپ|باگ|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- هیچ
# **API‌های حذف شده:**
- هیچ

## **نمونه‌های استفاده:**
**PSDNET-104. نمایش لایه‌های متنی با ماتریس تبدیل دوراندار**

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

**PSDNET-96. پیاده‌سازی اثر Stroke با پر کردن رنگ برای صادرات**

{{< highlight java >}}

  // پیاده‌سازی اثر Stroke با پر کردن رنگ برای صادرات

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

  // ذخیره psd

  im.Save(exportPath, new PsdOptions());

  // ذخیره png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. تبدیل‌کننده‌های InnerData لایه‌هایی با ماسک برداری را خراب می‌کنند**

{{< highlight java >}}

 // تبدیل‌کننده‌های InnerData لایه‌هایی با ماسک برداری را خراب می‌کنند

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

**PSDNET-113. به‌روزرسانی لایه متنی برای تصویر PSD خطا ایجاد می‌کند هنگام باز شدن در فتوشاپ**

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

// فایل باید بدون اشکال باز شده و قابل خواندن برای فتوشاپ باشد

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
