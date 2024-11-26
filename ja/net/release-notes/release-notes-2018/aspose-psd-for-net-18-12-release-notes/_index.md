---
title: Aspose.PSD for .NET 18.12 - リリースノート
type: docs
weight: 10
url: /ja/net/aspose-psd-for-net-18-12-release-notes/
---

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-76|ストロークレイヤーのサポート|機能|
|PSDNET-83|グラデーションエフェクトのサポート|機能|
|PSDNET-84|パターンエフェクトのサポート|機能|
|PSDNET-89|新しく生成された通常レイヤーをPsdImageに追加する機能を追加|機能|
|PSDNET-93|テキストレイヤーのコンテンツの更新後、バックスラッシュ文字で結果ファイルをPhotoshopで開くことができなくなる|バグ|
|PSDNET-39|CMYKカラーモードで画像データがオーバーサイズのままエクスポートされた後、画像が壊れる|バグ|
|PSDNET-52|可能：PSD内での回転が機能しない|バグ|
|PSDNET-88|可能：Aspose.Psdのクロップメソッドが機能しない|バグ|
|PSDNET-91|Aspose.Imagingの変更をAspose.PSDに適用|強化|

## **パブリックAPIの変更**
Method    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Class    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Method    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Method    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Property```
Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

## **使用例:**
**PSDNET-76. ストロークレイヤーのサポート**

**1) フィルタイプ - パターン**

{{< highlight java >}}

     // ストロークエフェクト。フィルタイプ - パターン。例

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokePatternChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // 新しいデータを準備

    var newPattern = new int[]

    {

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

    };

   var newPatternBounds = new Rectangle(0, 0, 4, 4);

   var guid = Guid.NewGuid();

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

         var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Normal, patternStroke.BlendMode);

         Assert.AreEqual(255, patternStroke.Opacity);

         Assert.AreEqual(true, patternStroke.IsVisible);

         var fillSettings = (PatternFillSettings)patternStroke.FillSettings;

         Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

         patternStroke.Opacity = 127;

         patternStroke.BlendMode = BlendMode.Color;

         PattResource resource;

         foreach (var globalLayerResource in im.GlobalLayerResources)

         {

             if (globalLayerResource is PattResource)

             {

                  resource = (PattResource)globalLayerResource;

                  resource.PatternId = guid.ToString();

                  resource.Name = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";        

                  resource.SetPattern(newPattern, newPatternBounds);               

             }

         }

         ((PatternFillSettings)patternStroke.FillSettings).PatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";

         ((PatternFillSettings)patternStroke.FillSettings).PatternId = guid.ToString() + "\0";

        im.Save(exportPath);

    }

    // 編集後のファイルのテスト

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

        PattResource resource = null;

        foreach (var globalLayerResource in im.GlobalLayerResources)

        {

            if (globalLayerResource is PattResource)

            {

                resource = (PattResource)globalLayerResource;

            }

        }

        if (resource == null)

        {

            throw new Exception("PattResource not found");

        }

        // パターンデータを確認

        Assert.AreEqual(newPattern, resource.PatternData);

        Assert.AreEqual(newPatternBounds, new Rectangle(0, 0, resource.Width, resource.Height));

        Assert.AreEqual(guid.ToString(), resource.PatternId);

        Assert.AreEqual(BlendMode.Color, patternStroke.BlendMode);

        Assert.AreEqual(127, patternStroke.Opacity);

        Assert.AreEqual(true, patternStroke.IsVisible);

        var fillSettings = (PatternFillSettings)patternStroke.FillSettings;

        Assert.AreEqual(FillType.Pattern, fillSettings.FillType);

    }

{{< /highlight >}}

**フィルタイプ - グラデーション**

{{< highlight java >}}

     // ストロークエフェクト。フィルタイプ - グラデーション。例

    string sourceFileName = "Stroke.psd";

    string exportPath = "StrokeGradientChanged.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, gradientStroke.BlendMode);

        Assert.AreEqual(255, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Black, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        Assert.AreEqual(true, fillSettings.AlignWithLayer);

        Assert.AreEqual(GradientType.Linear, fillSettings.GradientType);

        Assert.IsTrue(Math.Abs(90 - fillSettings.Angle) < 0.001, "角度が正しくありません");

        Assert.AreEqual(false, fillSettings.Dither);

        Assert.IsTrue(Math.Abs(0 - fillSettings.HorizontalOffset) < 0.001, "水平オフセットが正しくありません");

        Assert.assertTrue(Math.abs(0 - fillSettings.VerticalOffset) < 0.001, "垂直オフセットが正しくありません");

        Assert.AreEqual(false, fillSettings.Reverse);

        // カラーポイント

        var colorPoints = fillSettings.ColorPoints;

        Assert.AreEqual(2, colorPoints.Length);

        Assert.AreEqual(Color.Black, colorPoints[0].Color);

        Assert.AreEqual(0, colorPoints[0].Location);

        Assert.AreEqual(50, colorPoints[0].MedianPointLocation);

        Assert.AreEqual(Color.White, colorPoints[1].Color);

        Assert.AreEqual(4096, colorPoints[1].Location);

        Assert.AreEqual(50, colorPoints[1].MedianPointLocation);

        // 透明度ポイント

        var transparencyPoints = fillSettings.TransparencyPoints;

        Assert.AreEqual(2, transparencyPoints.Length);

        Assert.AreEqual(0, transparencyPoints[0].Location);

        Assert.AreEqual(50, transparencyPoints[0].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[0].Opacity);

        Assert.AreEqual(4096, transparencyPoints[1].Location);

        Assert.AreEqual(50, transparencyPoints[1].MedianPointLocation);

        Assert.AreEqual(100, transparencyPoints[1].Opacity);

        // 編集をテストする

        fillSettings.Color = Color.Green;

        gradientStroke.Opacity = 127;

        gradientStroke.BlendMode = BlendMode.Color;

        fillSettings.AlignWithLayer = false;

        fillSettings.GradientType = GradientType.Radial;

        fillSettings.Angle = 45;

        fillSettings.Dither = true;

        fillSettings.HorizontalOffset = 15;

        fillSettings.VerticalOffset = 11;

        fillSettings.Reverse = true;

        // 新しいカラーポイントを追加

        var colorPoint = fillSettings.AddColorPoint();

        colorPoint.Color = Color.Green;        

        colorPoint.Location = 4096;

        colorPoint.MedianPointLocation = 75;

        // 以前のポイントの位置を変更

        fillSettings.ColorPoints[1].Location = 1899;

        // 新しい透明度ポイントを追加

        var transparencyPoint = fillSettings.AddTransparencyPoint();

        transparencyPoint.Opacity = 25;

        transparencyPoint.MedianPointLocation = 25;

        transparencyPoint.Location = 4096;

        // 以前の透明度ポイントの位置を変更

        fillSettings.TransparencyPoints[1].Location = 2411;

        im.Save(exportPath);

    }

    // 編集後のファイルのテスト

    using (var im = (PsdImage)Image.Load(exportPath, loadOptions))

    {

        var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, gradientStroke.BlendMode);

        Assert.AreEqual(127, gradientStroke.Opacity);

        Assert.AreEqual(true, gradientStroke.IsVisible);

        var fillSettings = (GradientFillSettings)gradientStroke.FillSettings;

        Assert.AreEqual(Color.Green, fillSettings.Color);

        Assert.AreEqual(FillType.Gradient, fillSettings.FillType);

        // カラーポイントの確認

        Assert.AreEqual(3, fillSettings.ColorPoints.Length);

        var point = fillSettings.ColorPoints[0];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.Black, point.Color);

        Assert.AreEqual(0, point.Location);

        point = fillSettings.ColorPoints[1];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.White, point.Color);

        Assert.AreEqual(1899, point.Location);

        point = fillSettings.ColorPoints[2];

        Assert.AreEqual(75, point.MedianPointLocation);

        Assert.AreEqual(Color.Green, point.Color);

        Assert.AreEqual(4096, point.Location);

        // 透明度ポイントの確認

        Assert.AreEqual(3, fillSettings.TransparencyPoints.Length);

        var transparencyPoint = fillSettings.TransparencyPoints[0];

        Assert.AreEqual(50, transparencyPoint.MedianPointLocation);

        Assert.AreEqual(100, transparencyPoint.Opacity);
        
        Assert.AreEqual(0, transparencyPoint.Location);

        transparencyPoint = fillSettings.TransparencyPoints[1];

        Assert.AreEqual(50, transparencyPoint.MedianPointLocation);

        Assert.AreEqual(100, transparencyPoint.Opacity);

        Assert.AreEqual(2411, transparencyPoint.Location);

        transparencyPoint = fillSettings.TransparencyPoints[2];

        Assert.AreEqual(25, transparencyPoint.MedianPointLocation);
        
        Assert.AreEqual(25, transparencyPoint.Opacity);
        
        Assert.AreEqual(4096, transparencyPoint.Location);
    }

{{< /highlight >}}
```