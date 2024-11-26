---
title: Aspose.PSD for .NET 19.3 - リリースノート
type: docs
weight: 100
url: /ja/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}}

このページには、Aspose.PSD for .NET 19.3のリリースノートが含まれています。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-104|TransformMatrixによって回転させたテキストレイヤーのレンダリング|機能|
|PSDNET-96|輪郭効果をカラーフィルでエクスポートするためのレンダリングの実装|機能|
|PSDNET-112|InnerData Transformers が一部のベクトルマスクを破損させる|バグ|
|PSDNET-113|Photoshopで開いたときにPSDイメージのテキストレイヤーを更新するとエラーが発生する|バグ|

## **公開APIの変更**
# **追加されたAPI:**
- なし
# **削除されたAPI:**
- なし

## **使用例:**
**PSDNET-104. TransformMatrixによって回転させたテキストレイヤーのレンダリング**

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

**PSDNET-96. 輪郭効果をカラーフィルでエクスポートするためのレンダリングの実装**

{{< highlight java >}}

  // Implement rendering of Stroke effect with Color Fill for export

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

  // Save psd

  im.Save(exportPath, new PsdOptions());

  // Save png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. InnerData Transformers が一部のベクトルマスクを破損させる**

{{< highlight java >}}

 // InnerData Transformers が一部のベクトルマスクを破損させる

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

**PSDNET-113. Photoshopで開いたときにPSDイメージのテキストレイヤーを更新するとエラーが発生する**

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

// 例外なしでファイルを開き、Photoshopで読み取れる必要があります

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
