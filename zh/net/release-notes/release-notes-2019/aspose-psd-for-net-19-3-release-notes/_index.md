---
title: Aspose.PSD for .NET 19.3 - 发行说明
type: docs
weight: 100
url: /zh/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

此页面包含 Aspose.PSD for .NET 19.3 的发行说明

{{% /alert %}} 

|**关键字**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-104|通过 TransformMatrix 旋转的文本图层的渲染|特性|
|PSDNET-96|实现使用 Color Fill 导出带有描边效果的渲染|特性|
|PSDNET-112|InnerData 转换器损坏带有矢量蒙版的一些图层|错误|
|PSDNET-113|在 Photoshop 中打开时为 PSD 图像更新文本图层会引发错误|错误|

## **公共 API 更改**
# **新增的 API:**
- 无
# **移除的 API:**
- 无

## **使用示例:**
**PSDNET-104. 通过 TransformMatrix 旋转的文本图层的渲染**

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

**PSDNET-96. 实现使用 Color Fill 导出带有描边效果的渲染**

{{< highlight java >}}

  // 实现使用 Color Fill 导出带有描边效果的渲染

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

  // 保存 psd

  im.Save(exportPath, new PsdOptions());

  // 保存 png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. InnerData 转换器损坏带有矢量蒙版的一些图层**

{{< highlight java >}}

 // InnerData 转换器损坏带有矢量蒙版的一些图层

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

**PSDNET-113. 在 Photoshop 中打开时为 PSD 图像更新文本图层会引发错误**

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

// 文件必须在不出现异常的情况下打开，并且必须能够被 Photoshop 读取

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
