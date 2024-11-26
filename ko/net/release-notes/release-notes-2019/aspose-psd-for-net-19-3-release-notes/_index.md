---
title: Aspose.PSD for .NET 19.3 - 릴리스 노트
type: docs
weight: 100
url: /ko/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}}

이 페이지는 Aspose.PSD for .NET 19.3의 릴리스 노트를 포함합니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-104|TransformMatrix로 회전된 텍스트 레이어 렌더링|기능|
|PSDNET-96|Color Fill을 사용하여 스트로크 효과 렌더링 구현|기능|
|PSDNET-112|InnerData 변환기가 일부 벡터 마스크 레이어를 손상시킴|버그|
|PSDNET-113|Photoshop에서 열 때 PSD 이미지의 텍스트 레이어 업데이트하는 경우 오류가 발생함|버그|

## **공개 API 변경사항**
# **추가된 API:**
- 없음
# **제거된 API:**
- 없음

## **사용 예제:**
**PSDNET-104. TransformMatrix로 회전된 텍스트 레이어 렌더링**

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

**PSDNET-96. Color Fill을 사용하여 스트로크 효과 렌더링 구현**

{{< highlight java >}}

  // Color Fill을 사용하여 스트로크 효과 렌더링 구현

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

  // PSD로 저장

  im.Save(exportPath, new PsdOptions());

  // PNG로 저장

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. InnerData 변환기가 일부 벡터 마스크 레이어를 손상시킴**

{{< highlight java >}}

 // InnerData 변환기가 일부 벡터 마스크 레이어를 손상시킴

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

**PSDNET-113. Photoshop에서 열 때 PSD 이미지의 텍스트 레이어 업데이트하는 경우 오류가 발생함**

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

// 파일이 예외 없이 열려야 하며 Photoshop에서 읽을 수 있어야 함

using(Image image = Image.Load(exportPath)) {}

{{< /highlight >}}
