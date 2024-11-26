---
title: Aspose.PSD for .NET 20.2 - 릴리스 노트
type: docs
weight: 110
url: /ko/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}} 

이 페이지에는 [Aspose.PSD for .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**키**|**요약**|**범주**|
| :- | :- | :- |
|PSDNET-206|텍스트 레이어에서 서로 다른 색상 텍스트를 렌더링할 수 있는 능력 향상|기능|
|PSDNET-369|clbl 리소스 지원 (레이어 리소스에 블렌딩 클리핑 요소에 대한 정보가 포함된 레이어 리소스)|기능|
|PSDNET-274 |blwh 리소스 지원 (블랙 & 화이트 조정 레이어 데이터를 포함하는 리소스)|기능|
|PSDNET-230|레이어 그룹을 Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf로 내보낼 수 있는 능력|기능|
|PSDNET-372|lspf 리소스 지원 (레이어 보호 설정에 대한 설정이 포함된 리소스)|기능|
|PSDNET-370|infx 리소스 지원 (내부 요소의 블렌딩에 관한 데이터를 포함하는 리소스)|기능|
|PSDNET-251|PsdImage 및 Layer의 변환 동작을 변경하여 리팩터링 (레이어 마스크를 따로 변환하는 경우 레이어 크기 조정/회전/자르기를 올바르게 함)|향상|
|PSDNET-276 |일부 전역화 설정에서 AI 이미지 래스터 이미지를 열 수 없음|버그|
|PSDNET-194|레이어에서 FlipRotate 작업을 수행한 후 PSD 이미지가 읽을 수 없음|버그|
|PSDNET-177. |PSD 파일 로딩 중 System.ArgumentException 발생|버그|
|PSDNET-249|레이어에 대해 변환 메서드를 사용한 후 저장된 레이어가 잘못된 경계 또는 마스크를 가짐|버그|

## **공개 API 변경**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykColor.Equals(System.Object)
- T:Aspose.PSD.CompositeException
- T:Aspose.PSD.CoreExceptions.IndexOutOFRangeException
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String)
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String,System.Exception)
- F:Aspose.PSD.FileFormat.Otg
- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000CustomException
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.IsDataStoredDiscretely
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetChannelData(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey
- T:Aspose.PSD.ImageOptions.TiffOptionsUtils
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])
- P:Aspose.PSD.ImageOptionsBase.ProgressEventHandler
- P:Aspose.PSD.LoadOptions.ProgressEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Metered.Equals(System.Object)
- T:Aspose.PSD.ProgressEventHandler
- T:Aspose.PSD.ProgressManagement.EventType
- F:Aspose.PSD.ProgressManagement.EventType.RelativeProgress
- F:Aspose.PSD.ProgressManagement.EventType.StageChange
- F:Aspose.PSD.ProgressManagement.EventType.Initialization
- F:Aspose.PSD.ProgressManagement.EventType.PreProcessing
- F:Aspose.PSD.ProgressManagement.EventType.Processing
- F:Aspose.PSD.ProgressManagement.EventType.Finalization
- T:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Description
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.EventType
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.MaxValue
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Value
- M:Aspose.PSD.RasterImage.GetSkewAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Color)
# **삭제된 API:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues

## **사용 예시:**
**PSDNET-206. 텍스트 레이어에서 서로 다른 색상 텍스트를 렌더링할 수 있는 능력 향상**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("text_ethalon_different_colors.psd"))...

{{< /highlight >}}

**PSDNET-369. clbl 리소스 지원 (레이어 리소스에 블렌딩 클리핑 요소에 대한 정보가 포함된 리소스)**

{{< highlight java >}}

        void AssertIsTrue(bool condition, string message)...

{{< /highlight >}}

**PSDNET-274. blwh 리소스 지원 (블랙 & 화이트 조정 레이어 데이터를 포함하는 리소스)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Expected property value is not equal to actual value"...

{{< /highlight >}}

**PSDNET-230. 레이어 그룹을 Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf로 내보낼 수 있는 능력**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("1.psd"))...

{{< /highlight >}}

` `**PSDNET-372. lspf 리소스 지원 (레이어 보호 설정에 대한 설정이 포함된 리소스)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Expected property value is not equal to actual value"...

{{< /highlight >}}

` `**PSDNET-370. infx 리소스 지원 (내부 요소의 블렌딩에 관한 데이터를 포함하는 리소스)**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)...

{{< /highlight >}}

**PSDNET-251. PsdImage 및 Layer의 변환 동작을 변경하여 리팩터링 (레이어 마스크를 따로 변환하는 경우 레이어 크기 조정/회전/자르기를 올바르게 함)**

{{< highlight java >}}

             var enums = (RotateFlipType[])Enum.GetValues(typeof(RotateFlipType))...

{{< /highlight >}}

**PSDNET-276. 일부 전역화 설정에서 AI 이미지 래스터 이미지를 열 수 없음**

{{< highlight java >}}

        string sourceFileName = "form_raster_8.ai"...

{{< /highlight >}}

**PSDNET-194. 레이어에서 FlipRotate 작업을 수행한 후 PSD 이미지가 읽을 수 없음**

{{< highlight java >}}

             string sourceFileName = GetFileInCustomFolderRelativeToBase(@"testdata\Issues\IMAGINGNET-2617\1.psd")...

{{< /highlight >}}

**PSDNET-177. PSD 파일 로딩 중 System.ArgumentException 발생**

{{< highlight java >}}

         string sourcePath = "1.psd"...

{{< /highlight >}}

**PSDNET-249. 레이어에 대해 변환 메서드를 사용한 후 저장된 레이어가 잘못된 경계 또는 마스크를 가짐**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)...

{{< /highlight >}}```json
{
  "content": "----\r\ntitle: Aspose.PSD for .NET 20.2 - 릴리스 노트\r\ntype: docs\r\nweight: 110\r\nurl: /ko/net/aspose-psd-for-net-20-2-release-notes/\r\n----\r\n\r\n{{% alert color=\"primary\" %}} \r\n\r\n이 페이지에는 [Aspose.PSD for .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.\r\n\r\n{{% /alert %}} \r\n\r\n|**키**|**요약**|**범주**|\r\n| :- | :- | :- |\r\n|PSDNET-206|텍스트 레이어에서 서로 다른 색상 텍스트를 렌더링할 수 있는 능력 향상|기능|\r\n|PSDNET-369|clbl 리소스 지원 (레이어 리소스에 블렌딩 클리핑 요소에 대한 정보가 포함된 레이어 리소스)|기능|\r\n|PSDNET-274 |blwh 리소스 지원 (블랙 & 화이트 조정 레이어 데이터를 포함하는 리소스)|기능|\r\n|PSDNET-230|레이어 그룹을 Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf로 내보낼 수 있는 능력|기능|\r\n|PSDNET-372|lspf 리소스 지원 (레이어 보호 설정에 대한 설정이 포함된 리소스)|기능|\r\n|PSDNET-370|infx 리소스 지원 (내부 요소의 블렌딩에 관한 데이터를 포함하는 리소스)|기능|\r\n|PSDNET-251|PsdImage 및 Layer의 변환 동작을 변경하여 리팩터링 (레이어 마스크를 따로 변환하는 경우 레이어 크기 조정/회전/자르기를 올바르게 함)|향상|\r\n|PSDNET-276 |일부 전역화 설정에서 AI 이미지 래스터 이미지를 열 수 없음|버그|\r\n|PSDNET-194|레이어에서 FlipRotate 작업을 수행한 후 PSD 이미지가 읽을 수 없음|버그|\r\n|PSDNET-177. |PSD 파일 로딩 중 System.ArgumentException 발생|버그|\r\n|PSDNET-249|레이어에 대해 변환 메서드를 사용한 후 저장된 레이어가 잘못된 경계 또는 마스크를 가짐|버그|\r\n\r\n## **공개 API 변경**\r\n# **추가된 API:**\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle\r\n- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height\r\n- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Reds\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyans\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blues\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue\r\n- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Save(Aspose.PSD.StreamContainer,System.Int32)\r\n- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Length\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Reds\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Yellows\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Greens\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Cyans\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Blues\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Magentas\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.UseTint\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor\r\n- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues\r\n- T:Aspose.PSD.AggregateException\r\n- M:Aspose.PSD.CmykColor.Equals(System.Object)\r\n- T:Aspose.PSD.CompositeException\r\n- T:Aspose.PSD.CoreExceptions.IndexOutOFRangeException\r\n- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String)\r\n- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String,System.Exception)\r\n- F:Aspose.PSD.FileFormat.Otg\r\n- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000CustomException\r\n- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Int32)\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Byte[])\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Length\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion\r\n- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.IsDataStoredDiscretely\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetChannelData(System.Int32)\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Save(Aspose.PSD.StreamContainer,System.Int32)\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager\r\n- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey\r\n- T:Aspose.PSD.ImageOptions.TiffOptionsUtils\r\n- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor\r\n- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])\r\n- P:Aspose.PSD.ImageOptionsBase.ProgressEventHandler\r\n- P:Aspose.PSD.LoadOptions.ProgressEventHandler\r\n- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)\r\n- M:Aspose.PSD.Metered.Equals(System.Object)\r\n- T:Aspose.PSD.ProgressEventHandler\r\n- T:Aspose.PSD.ProgressManagement.EventType\r\n- F:Aspose.PSD.ProgressManagement.EventType.RelativeProgress\r\n- F:Aspose.PSD.ProgressManagement.EventType.StageChange\r\n- F:Aspose.PSD.ProgressManagement.EventType.Initialization\r\n- F:Aspose.PSD.ProgressManagement.EventType.PreProcessing\r\n- F:Aspose.PSD.ProgressManagement.EventType.Processing\r\n- F:Aspose.PSD.ProgressManagement.EventType.Finalization\r\n- T:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo\r\n- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Description\r\n- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.EventType\r\n- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.MaxValue\r\n- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Value\r\n- M:Aspose.PSD.RasterImage.GetSkewAngle\r\n- M:Aspose.PSD.RasterImage.NormalizeAngle\r\n- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Color)\r\n# **삭제된 API:**\r\n- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose\r\n- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle\r\n- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)\r\n- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues\r\n\r\n## **사용 예시:**\r\n**PSDNET-206. 텍스트 레이어에서 서로 다른 색상 텍스트를 렌더링할 수 있는 능력 향상**\r\n\r\n{{< highlight java >}}\r\n\r\n  using (var psdImage = (PsdImage)Image.Load(\"text_ethalon_different_colors.psd\"))...\r\n\r\n{{< /highlight >}}\r\n\r\n**PSDNET-369. clbl 리소스 지원 (레이어 리소스에 블렌딩 클리핑 요소에 대한 정보가 포함된 리소스)**\r\n\r\n{{< highlight java >}}\r\n\r\n        void AssertIsTrue(bool condition, string message)...{{< /highlight >}}\r\n\r\n**PSDNET-274. blwh 리소스 지원 (블랙 & 화이트 조정 레이어 데이터를 포함하는 리소스)**\r\n\r\n{{< highlight java >}}\r\n\r\n         const string ActualPropertyValueIsWrongMessage = \"Expected property value is not equal to actual value\"...\r\n{{< /highlight >}}\r\n\r\n**PSDNET-230. 레이어 그룹을 Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf로 내보낼 수 있는 능력**\r\n\r\n{{< highlight java >}}\r\n\r\n  using (var psdImage = (PsdImage)Image.Load(\"1.psd\"))...\r\n{{< /highlight >}}\r\n\r\n` **PSDNET-372. lspf 리소스 지원 (레이어 보호 설정에 대한 설정이 포함된 리소스)**\r\n\r\n{{< highlight java >}}\r\n\r\n         const string ActualPropertyValueIsWrongMessage = \"Expected property value is not equal to actual value\"...\r\n{{< /highlight >}}\r\n\r\n` **PSDNET-370. infx 리소스 지원 (내부 요소의 블렌딩에 관한 데이터를 포함하는 리소스)**\r\n\r\n{{< highlight java >}}\r\n\r\n         void AssertIsTrue(bool condition, string message)...{{< /highlight >}}\r\n\r\n**PSDNET-251. PsdImage 및 Layer의 변환 동작을 변경하여 리팩터링 (레이어 마스크를 따로 변환하는 경우 레이어 크기 조정/회전/자르기를 올바르게 함)**\r\n\r\n{{< highlight java >}}\r\n\r\n             var enums = (RotateFlipType[])Enum.GetValues(typeof(RotateFlipType))...{{< /highlight >}}\r\n\r\n**PSDNET-276. 일부 전역화 설정에서 AI 이미지 래스터 이미지를 열 수 없음**\r\n\r\n{{< highlight java >}}\r\n\r\n        string sourceFileName = \"form_raster_8.ai\"...{{< /highlight >}}\r\n\r\n**PSDNET-194. 레이어에서 FlipRotate 작업을 수행한 후 PSD 이미지가 읽을 수 없음**\r\n\r\n{{< highlight java >}}\r\n\r\n             string sourceFileName = GetFileInCustomFolderRelativeToBase(@\"testdata\\Issues\\IMAGINGNET-2617\\1.psd\")...{{< /highlight >}}\r\n\r\n**PSDNET-177. PSD 파일 로딩 중 System.ArgumentException 발생**\r\n\r\n{{< highlight java >}}\r\n\r\n         string sourcePath = \"1.psd\"...{{< /highlight >}}\r\n\r\n**PSDNET-249. 레이어에 대해 변환 메서드를 사용한 후 저장된 레이어가 잘못된 경계 또는 마스크를 가짐**\r\n\r\n{{< highlight java >}}\r\n\r\n         void AssertIsTrue(bool condition, string message)...{{< /highlight >}}"
}
```