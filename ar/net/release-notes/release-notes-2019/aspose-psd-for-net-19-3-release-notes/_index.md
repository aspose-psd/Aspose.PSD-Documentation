---
title: تحديثات الإصدار Aspose.PSD for .NET 19.3
type: docs
weight: 100
url: /ar/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على تحديثات الإصدار لـ Aspose.PSD for .NET 19.3

{{% /alert %}} 



|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-104|تقديم تدوير الطبقات النصية بواسطة TransformMatrix|ميزة|
|PSDNET-96|تنفيذ تقديم تأثير السكتة الدماغية مع ملء اللون للتصدير|ميزة|
|PSDNET-112|محولات InnerData تفسد بعض الطبقات مع قناعات الفيكتور|خطأ|
|PSDNET-113|تحديث طبقة النص لصورة PSD يثير خطأ عند فتحها في Photoshop|خطأ|



## **تغييرات واجهة برمجة التطبيقات العمومية**

### **الواجهات الجديدة:**
- لا شيء

### **الواجهات المزالة:**
- لا شيء



## **أمثلة الاستخدام:**

### **PSDNET-104. تقديم تدوير الطبقات النصية بواسطة TransformMatrix**

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



### **PSDNET-96. تنفيذ تقديم تأثير السكتة الدماغية مع ملء اللون للتصدير**

{{< highlight java >}}

  // تنفيذ تقديم تأثير السكتة الدماغية مع ملء اللون للتصدير

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

     // حفظ psd

     im.Save(exportPath, new PsdOptions());

     // حفظ png

     im.Save(exportPathPng, new PngOptions() {
         ColorType = PngColorType.TruecolorWithAlpha
     });
 }         

{{< /highlight >}}


### **PSDNET-112. محولات InnerData تفسد بعض الطبقات مع قناعات الفيكتور**

{{< highlight java >}}

 // محولات InnerData تفسد بعض الطبقات مع قناعات الفيكتور

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


### **PSDNET-113. تحديث طبقة النص لصورة PSD يثير خطأ عند فتحها في Photoshop**

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

    // يجب فتح الملف بدون استثناء ويجب أن يكون قابلاً للقراءة لبرنامج Photoshop

    using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
