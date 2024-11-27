
---
title: Aspose.PSD for .NET 18.10 - ملاحظات الإصدار
type: docs
weight: 30
url: /ar/net/aspose-psd-for-net-18-10-release-notes/
---

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-14|إضافة دعم أوضاع الدمج بجانب العادي|ميزة|
|PSDNET-69|إضافة دعم تأثير تغطية اللون|ميزة|
|PSDNET-70|إضافة دعم تأثير الظل المسقط|ميزة|
|PSDNET-71|التقديم لتصدير تأثير تغطية اللون|ميزة|
|PSDNET-72|التقديم لتصدير تأثير الظل المسقط|ميزة|
|PSDNET-74|دعم إضافة تأثيرات الطبقة في وقت التشغيل|ميزة|
|PSDNET-73|تحسين أداء تحميل الموارد التي تحتوي على هياكل نوع النظام|خطأ|
|PSDNET-79|إعادة هيكلة وإصلاح تسريبات الذاكرة في معلومات الطبقة والقناع|تحسين|

## **أمثلة الاستخدام:**
**PSDNET-14 إضافة دعم أوضاع الدمج بجانب العادي**

{{< highlight java >}}

 var files = new string[]

{

    "عادي",

    "تفكك",

    "مظلم",

    "ضرب",

    "حرق اللون",

    "ضرب خطي",

    "لون أغمق",

    "تفتيح",

    "الشاشة",

    "تجنب اللون",

    "ضرب خطي",

    "لون تفتيح",

    "تراكم",

    "ناعم",

    "صارم",

    "ضوء حي",

    "ضوء خطي",

    "تثبيت الضوء",

    "خليط صارم",

    "فرق",

    "استبعاد",

    "طرح",

    "قسمة",

    "صبغة",

    "تشبع",

    "لون",

    "سطوع",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // تصدير إلى PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // تحديد الشفافية 50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 إضافة دعم تأثير تغطية اللون**

{{< highlight java >}}

     // تحرير تأثير تغطية اللون

    string sourceFileName = "ColorOverlay.psd";

    string psdPathAfterChange = "ColorOverlayChanged.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlay)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       colorOverlay.Color = Color.Green;

       colorOverlay.Opacity = 128;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}

**PSDNET-70 إضافة دعم تأثير الظل المسقط**

{{< highlight java >}}

     // تحرير تأثير الظل المسقط

    string sourceFileName = "Shadow.psd";

    string psdPathAfterChange = "ShadowChanged.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.AreEqual(0, shadowEffect.Noise);

       shadowEffect.Color = Color.Green;

       shadowEffect.Opacity = 128;

       shadowEffect.Distance = 11;

       shadowEffect.UseGlobalLight = false;

       shadowEffect.Size = 9;

       shadowEffect.Angle = 45;

       shadowEffect.Spread = 3;

       shadowEffect.Noise = 50;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}



**PSDNET-71 التقديم لتصدير تأثير تغطية اللون**

{{< highlight java >}}

    // تحرير تأثير تغطية اللون

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);

       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // حفظ بصيغة PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 التقديم لتصدير تأثير الظل المسقط**

{{< highlight java >}}

     // تصدير الظل المسقط

    string sourceFileName = "Shadow.psd";

    string pngExportPath = "Shadow.png";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);

       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.assertEquals(0, shadowEffect.Noise);

       // حفظ بصيغة PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 دعم إضافة تأثيرات الطبقة في وقت التشغيل**

{{< highlight java >}}

     // إضافة تأثير تغطية اللون في الطبقة في وقت التشغيل

    string sourceFileName = "ThreeRegularLayersWithLayerEffect.psd";

    string psdExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

    string pngExportPath = "ThreeRegularLayersWithLayerEffectChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };



    var testFolder = string.Empty;

    var im = (PsdImage)Image.Load(testPath, loadOptions) 

    using (im)

    {

        var effect = im.Layers[1].BlendingOptions.AddColorOverlay();

        effect.Opacity = 128;

        effect.Color = Color.Green;

        effect.BlendMode = BlendMode.Normal;

        var effect = im.Layers[1].BlendingOptions.AddDropShadow();

        effect.Color = Color.Red;

        effect.Opacity = 128;

        effect.BlendMode = BlendMode.Normal;



        // حفظ بصيغة PSD    

        im.Save(psdExportPath);



        // حفظ بصيغة PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}
