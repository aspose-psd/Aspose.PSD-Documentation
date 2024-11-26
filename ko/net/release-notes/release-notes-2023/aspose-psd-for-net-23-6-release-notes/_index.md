---
title: Aspose.PSD for .NET 23.6 - 릴리스 노트
type: docs
weight: 70
url: /ko/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**     | **개요**                                                                                                                                      | **카테고리** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | 타임 라인 API 리팩토링                                                                                                                            | 기능 향상  |
| PSDNET-1517 | 와프 렌더링시 아티팩트 제거                                                                                                               | 기능 향상  |
| PSDNET-1528 | 와프 렌더링 최적화                                                                                                                      | 기능 향상  |
| PSDNET-147  | 임계값 조정 레이어 지원                                                                                                            | 기능      |
| PSDNET-149  | 선택적 색상 조정 레이어 지원                                                                                                      | 기능      |
| PSDNET-801  | PSD 타임 라인을 애니메이티드 GIF 파일로 내보내는 기능                                                                      | 기능      |
| PSDNET-1555 | 사각형 테두리가 없는 TextLayer 지원                                                                              | 기능      |
| PSDNET-1582 | ShapeLayer 지원                                                                                                                  | 기능      |
| PSDNET-864  | 스마트 객체에 이미지를 교체하면 업데이트되지 않음                                                                      | 버그      |
| PSDNET-1404 | 다음 예외와 함께 PSD 파일을 PSD로 저장할 수 없음: Rgb 및 Lab 모드는 3채널보다 적거나 4채널 이상 포함할 수 없음   | 버그      |
| PSDNET-1546 | Photoshop의 편집 모드로 TextLayer를 열 때 텍스트 정렬이 손실됨                                                                        | 버그      |
| PSDNET-1548 | PSD 파일 저장 시 Null 참조 예외                                                                                                  | 버그      |
| PSDNET-1578 | ShapeLayer 로딩 중 예외 발생: 벡터 원점 바운드의 포인트는 아직 지원되지 않음                                                             | 버그      |
| PSDNET-1579 | VogkResource 로드 중 예외 발생: 포인트는 DoubleStructures로 저장되었지만 UnitStructures로 읽음                                                                   | 버그      |
| PSDNET-1581 | ShapeLayer의 LayerType이 비어 있음                                                                                                      | 버그      |


## **공개 API 변경 내용**
# **추가된 API:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **제거된 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **사용 예:**

**PSDNET-147. 임계값 조정 레이어 지원**

{{< highlight csharp >}}
string sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
string outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
string outputPngWithThresholdLayer = "flowers_threshold_output.png";

string sourceFileWithoutThresholdLayer = "flowers_source.psd";
string outputPsdWithoutThresholdLayer = "flowers_output.psd";
string outputPngWithoutThresholdLayer = "flowers_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("객체가 동일하지 않습니다.");
    }
}

// 이미지에서 임계값 조정 레이어 가져오기 및 수정하기
using (var image = (PsdImage)Image.Load(sourceFileWithThresholdLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // 임계값 조정 레이어 가져오기
            ThresholdLayer thrsLayer = (ThresholdLayer)layer;
            var level = thrsLayer.Level;

            // 레이어 매개변수 확인
            AssertAreEqual(level, (short)115);

            // 레이어 매개변수 설정
            thrsLayer.Level = 50;

            image.Save(outputPsdWithThresholdLayer);
            image.Save(outputPngWithThresholdLayer, new PngOptions());
        }
    }
}

// 이미지에 임계값 조정 레이어 추가 및 설정하기
using (var image = (PsdImage)Image.Load(sourceFileWithoutThresholdLayer))
{
    // 임계값 조정 레이어 추가
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // 레이어 매개변수 설정
    thresholdLayer.Level = 115;

    image.Save(outputPsdWithoutThresholdLayer);
    image.Save(outputPngWithoutThresholdLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. 선택적 색상 조정 레이어 지원**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-801. PSD 타임 라인을 애니메이티드 GIF 파일로 내보내는 기능**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-864. 스마트 객체에 이미지를 교체하면 업데이트되지 않음**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}}

**PSDNET-1401. 타임라인 API 리팩토링**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}}

**PSDNET-1404. RGB 및 Lab 모드가 3채널 미만 또는 4채널 이상 포함할 수 없어 PSD 파일을 PSD로 저장할 수 없을 때 발생하는 예외**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}}

**PSDNET-1517. 와프 렌더링시 아티팩트 제거**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}}  

**PSDNET-1528. 와프 렌더링 최적화**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-1546. Photoshop의 편집 모드로 TextLayer를 열 때 텍스트 정렬이 손실됨**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-1548. PSD 파일 저장 시 Null 참조 예외**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-1555. 사각형 테두리가 없는 TextLayer 지원**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-1578. ShapeLayer 로딩 중 예외가 발생하는 경우: 벡터 원점 바운드의 포인트는 아직 지원되지 않음**

**PSDNET-1579. VogkResource 로딩 중 예외가 발생하는 경우: 포인트가 DoubleStructures로 저장되어 있지만 UnitStructures로 읽음**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-1581. ShapeLayer의 LayerType이 비어 있음**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}} 

**PSDNET-1582. ShapeLayer 지원**

{{< highlight csharp >}}
// 코드 삽입
{{< /highlight >}}