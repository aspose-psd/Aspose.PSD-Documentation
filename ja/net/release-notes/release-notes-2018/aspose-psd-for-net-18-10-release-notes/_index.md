---
title: Aspose.PSD for .NET 18.10 - リリースノート
type: docs
weight: 30
url: /ja/net/aspose-psd-for-net-18-10-release-notes/
---

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-14|通常以外のブレンドモードのサポートを追加|機能|
|PSDNET-69|カラーオーバーレイ効果のサポートを追加|機能|
|PSDNET-70|ドロップシャドウ効果のサポートを追加|機能|
|PSDNET-71|カラーオーバーレイ効果のエクスポート用のレンダリング|機能|
|PSDNET-72|ドロップシャドウ効果のエクスポート用のレンダリング|機能|
|PSDNET-74|ランタイム時のレイヤーエフェクトの追加サポート|機能|
|PSDNET-73|osTypeStructuresを含むリソースの読み込みパフォーマンスの最適化|バグ|
|PSDNET-79|LayerAndMaskInfoのリファクタリングとメモリリークの修正|強化|

## **使用例:**
**PSDNET-14 通常以外のブレンドモードのサポートを追加**

{{< highlight java >}}

 var files = new string[]

{

    "通常",

    "ディゾルブ",

    "暗算",

    "乗算",

    "色の焼きこみ",

    "線形焼きこみ",

    "ダーカーカラー",

    "明るくする",

    "スクリーン",

    "色のドッジ",

    "線形ドッジ／加算",

    "色の明るく",

    "オーバーレイ",

    "ソフトライト",

    "ハードライト",

    "ビビッドライト",

    "線形ライト",

    "ピンライト",

    "ハードミックス",

    "差",

    "除去",

    "減算",

    "分割",

    "色相",

    "彩度",

    "色",

    "輝度",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // PNGへエクスポート

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // 透明度50%に設定

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 カラーオーバーレイ効果のサポートを追加**

{{< highlight java >}}

     // カラーオーバーレイ効果の編集

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

**PSDNET-70 ドロップシャドウ効果のサポートを追加**

{{< highlight java >}}

     // ドロップシャドウ効果の編集

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



**PSDNET-71 カラーオーバーレイ効果のエクスポート用のレンダリング**

{{< highlight java >}}

    // カラーオーバーレイ効果の編集

    string sourceFileName = "ColorOverlay.psd";

    string pngExportPath = "ColorOverlay.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // PNGへ保存

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 ドロップシャドウ効果のエクスポート用のレンダリング**

{{< highlight java >}}

     // ドロップシャドウのエクスポート

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

       // PNGへ保存

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 ランタイム時のレイヤーエフェクトの追加サポート**

{{< highlight java >}}

     // ランタイムでのカラーオーバーレイレイヤーエフェクトの追加

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



        // PSDを保存    

        im.Save(psdExportPath);



        // PNGを保存

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}
