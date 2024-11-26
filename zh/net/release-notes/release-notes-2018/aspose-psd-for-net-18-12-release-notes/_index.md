---
title: Aspose.PSD for .NET 18.12 - 发行说明
type: docs
weight: 10
url: /zh/net/aspose-psd-for-net-18-12-release-notes/
---

|**键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-76|支持笔画图层|特性|
|PSDNET-83|支持渐变效果|特性|
|PSDNET-84|支持图案效果|特性|
|PSDNET-89|使能够将新生成的常规图层添加到 PsdImage|特性|
|PSDNET-93|在更新带 \ (反斜杠) 字符的文本图层内容后，结果文件无法在 Photoshop 中打开|错误|
|PSDNET-39|在 CMYK 颜色模式下导出超大图像数据后出现破损的图像|错误|
|PSDNET-52|可能：PSD 中的旋转不起作用|错误|
|PSDNET-88|可能：Aspose.Psd 中的裁剪方法不起作用|错误|
|PSDNET-91|将 Aspose.Imaging 的更改应用到 Aspose.PSD|增强|

## **公共 API 更改**
方法    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

类    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

方法    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

方法    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

类    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

类    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

类    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

字段/枚举    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

方法    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

类    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

属性    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **使用示例：**
**PSDNET-76. 支持笔画图层**

**1) 填充类型 - 图案**

{{< highlight java >}}

     // 笔画效果。填充类型 - 图案。示例

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // 准备新数据

    var newPattern = new int[]

    {

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.To```java
// Apply changes of Aspose.Imaging to Aspose.PSD

string sourceFileName = "ImageWithEffectsSource.psd";
string exportPath = "ImageWithEffectsEdited.psd";

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    var blurRadius = 20; // Apply blur effect
    image.ApplyEffect(new GaussianBlurFilter(blurRadius));

    var noiseRadius = 10; // Apply noise effect
    image.ApplyEffect(new NoiseFilter(noiseRadius));

    var brightnessShift = 20; // Adjust brightness
    var contrastShift = 10; // Adjust contrast
    image.AdjustBrightnessContrast(brightnessShift, contrastShift);

    var hueAngle = 30; // Adjust hue
    image.AdjustHueSaturationLightness(hueAngle, 0, 0);

    image.Save(exportPath);
}


```

```java
// Gradient overlay effect. Example

string sourceFileName = "GradientOverlay.psd";
string exportPath = "GradientOverlayChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    Assert.AreEqual(BlendMode.Normal, gradientOverlay.BlendMode);
    Assert.AreEqual(255, gradientOverlay.Opacity);
    Assert.AreEqual(true, gradientOverlay.IsVisible);

    var settings = gradientOverlay.Settings;

    Assert.AreEqual(Color.Empty, settings.Color);
    Assert.AreEqual(FillType.Gradient, settings.FillType);
    Assert.AreEqual(true, settings.AlignWithLayer);
    Assert.AreEqual(GradientType.Linear, settings.GradientType);
    Assert.IsTrue(Math.Abs(33 - settings.Angle) < 0.001, "Angle is incorrect");
    Assert.AreEqual(false, settings.Dither);
    Assert.IsTrue(Math.Abs(129 - settings.HorizontalOffset) < 0.001, "Horizontal offset is incorrect");
    Assert.IsTrue(Math.Abs(156 - settings.VerticalOffset) < 0.001, "Vertical offset is incorrect");
    Assert.AreEqual(false, settings.Reverse);

    // Color Points
    var colorPoints = settings.ColorPoints;
    Assert.AreEqual(3, colorPoints.Length);

    Assert.AreEqual(Color.FromArgb(9, 0, 178), colorPoints[0].Color);
    Assert.AreEqual(0, colorPoints[0].Location);
    Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

    Assert.AreEqual(Color.Red, colorPoints[1].Color);
    Assert.AreEqual(2048, colorPoints[1].Location);
    Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

    Assert.AreEqual(Color.FromArgb(255, 252, 0), colorPoints[2].Color);
    Assert.AreEqual(4096, colorPoints[2].Location);
    Assert.AreEqual(50, colorPoints[2].MedianPointLocation);

    // Transparency points
    var transparencyPoints = settings.TransparencyPoints;
    Assert.AreEqual(2, transparencyPoints.Length);

    Assert.AreEqual(0, transparencyPoints[0].Location);
    Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);
    Assert.AreEqual(100, transparencyPoints[0].Opacity);

    Assert.AreEqual(4096, transparencyPoints[1].Location);
    Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);
    Assert.AreEqual(100, transparencyPoints[1].Opacity);

    // Test editing
    settings.Color = Color.Green;
    gradientOverlay.Opacity = 193;
    gradientOverlay.BlendMode = BlendMode.Lighten;
    settings.AlignWithLayer = false;
    settings.GradientType = GradientType.Radial;
    settings.Angle = 45;
    settings.Dither = true;
    settings.HorizontalOffset = 15;
    settings.VerticalOffset = 11;
    settings.Reverse = true;

    // Add new color point
    var colorPoint = settings.AddColorPoint();
    colorPoint.Color = Color.Green;
    colorPoint.Location = 4096;
    colorPoint.MedianPointLocation = 75;

    // Change location of previous point
    settings.ColorPoints[2].Location = 3000;

    // Add new transparency point
    var transparencyPoint = settings.AddTransparencyPoint();
    transparencyPoint.Opacity = 25;
    transparencyPoint.MedianPointLocation = 25;
    transparencyPoint.Location = 4096;

    // Change location of previous transparency point
    settings.TransparencyPoints[1].Location = 2315;

    im.Save(exportPath);
}

```
