---
title: Aspose.PSD for .NET 18.10 - 发行说明
type: docs
weight: 30
url: /zh/net/aspose-psd-for-net-18-10-release-notes/
---

|**关键字**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-14|增加除Normal外的混合模式支持|功能|
|PSDNET-69|增加颜色叠加效果支持|功能|
|PSDNET-70|增加阴影效果支持|功能|
|PSDNET-71|导出颜色叠加效果的渲染|功能|
|PSDNET-72|导出阴影效果的渲染|功能|
|PSDNET-74|支持在运行时添加图层效果|功能|
|PSDNET-73|优化包含osTypeStructures的资源加载性能|错误|
|PSDNET-79|LayerAndMaskInfo中的重构和内存泄漏修复|增强功能|

## **使用示例:**

**PSDNET-14 增加除Normal外的混合模式支持**

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

        // 导出为PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // 设置透明度为50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 增加颜色叠加效果支持**

{{< highlight java >}}

     // 编辑ColorOverlay效果

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

**PSDNET-70 增加阴影效果支持**

{{< highlight java >}}

     // 编辑DropShadow效果

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



**PSDNET-71 导出颜色叠加效果的渲染**

{{< highlight java >}}

    // 编辑ColorOverlay效果

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // 保存为PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 导出阴影效果的渲染**

{{< highlight java >}}

     // 导出DropShadow效果

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

       // 保存为PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 支持在运行时添加图层效果**

{{< highlight java >}}

     // 在运行时添加颜色叠加图层效果

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



        // 保存PSD    

        im.Save(psdExportPath);



        // 保存PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

