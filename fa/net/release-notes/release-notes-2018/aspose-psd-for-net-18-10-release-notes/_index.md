---
title: دوره أصدر Aspose.PSD با .NET 18.10 - یادداشت‌های انتشار
type: docs
weight: 30
url: /fa/net/aspose-psd-for-net-18-10-release-notes/
---

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-14|افزودن پشتیبانی از حالت‌های ترکیب علاوه بر عادی|ویژگی|
|PSDNET-69|افزودن پشتیبانی از اثر روکار رنگ|ویژگی|
|PSDNET-70|افزودن پشتیبانی از اثر سایه ریسه|ویژگی|
|PSDNET-71|رندر کردن برای صادرات اثر روکار رنگ|ویژگی|
|PSDNET-72|رندر کردن برای صادرات اثر سایه ریسه|ویژگی|
|PSDNET-74|پشتیبانی از اضافه کردن اثرات لایه در زمان اجرا|ویژگی|
|PSDNET-73|بهینه سازی عملکرد بارگذاری منابع دارای هسته osTypeStructures|اشکال|
|PSDNET-79|بازنویسی و رفع نشت حافظه در اطلاعات لایه و ماسک|بهبود|

## **مثال‌های استفاده:**
**PSDNET-14 افزودن پشتیبانی از حالت‌های ترکیب علاوه بر عادی**

{{< highlight java >}}

 var files = new string[]

{

    "Normal",

    "Dissolve",

    "Darken",

    "Multiply",

    "ColorBurn",

    "LinearBurn",

    "DarkerColor",

    "Lighten",

    "Screen",

    "ColorDodge",

    "LinearDodgeAdd",

    "LightenColor",

    "Overlay",

    "SoftLight",

    "HardLight",

    "VividLight",

    "LinearLight",

    "PinLight",

    "HardMix",

    "Difference",

    "Exclusion",

    "Subtract",

    "Divide",

    "Hue",

    "Saturation",

    "Color",

    "Luminosity",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // صادرات به PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // تنظیم شفافیت 50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 افزودن پشتیبانی از اثر روکار رنگ**

{{< highlight java >}}

     // ویرایش اثر روکار رنگ

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

**PSDNET-70 افزودن پشتیبانی از اثر سایه ریسه**

{{< highlight java >}}

     // ویرایش اثر سایه ریسه

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

**PSDNET-71 رندر کردن برای صادرات اثر روکار رنگ**

{{< highlight java >}}

    // ویرایش اثر روکار رنگ

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // ذخیره سازی PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 رندر کردن برای صادرات اثر سایه ریسه**

{{< highlight java >}}

     // صادرات سایه ریسه

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

       Assert.AreEqual(0, shadowEffect.Noise);

       // ذخیره سازی PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 پشتیبانی از اضافه کردن اثرات لایه در زمان اجرا**

{{< highlight java >}}

     // افزودن اثر لایه روکار رنگ در زمان اجرا

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



        // ذخیره سازی PSD    

        im.Save(psdExportPath);



        // ذخیره سازی PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}



