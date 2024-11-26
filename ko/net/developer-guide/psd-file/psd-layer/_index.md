---
title: PSD 레이어
type: docs
weight: 70
url: /ko/net/psd-layer/
---

## **개요**
Adobe® Photoshop® PSD 레이어는 그래픽 처리의 최고 개념 중 하나입니다. 레이어에는 픽셀에 대한 정보가 포함되어 있으며 서로 다른 채널 수를 가질 수 있습니다.

Photoshop 문서의 레이어에서 가장 중요한 부분 중 하나는 레이어 리소스입니다. PSD에서 지원하는 [레이어 리소스](/psd/ko/net/list-of-psd-layer-resources/)의 전체 목록을 문서에서 확인할 수 있습니다.

다음 스크린샷에서 레이어를 조작하는 UI를 찾을 수 있습니다:

![todo:image_alt_text](psd/ko-layer_1.png)

하지만 Aspose.PSD는 [C#](/psd/ko/net/home/) 및 [Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home)를 통해 PSD 레이어의 프로그래밍 방식 조작에 특화되어 있습니다.

추가 문서를 아래 문서에서 찾을 수 있습니다: [이미지 조작](/psd/ko/net/manipulating-images-html/). 모든 조작은 PSD 미리보기 및 레이어로 처리될 수 있으며 [Aspose.PSD 래스터 이미지 API 참조](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)에서 더 많은 정보를 얻을 수 있습니다.

## **사용 가능한 PSD 레이어 API**
- 레이어 효과
- 레이어 공통 속성
- 레이어 메타데이터

## **C#을 통한 레이어 편집 예시**
### **새 레이어 추가**
만약 열린 [PSD 파일](/psd/ko/net/psd-file/)에 빈 레이어를 추가하고 싶다면 다음 코드를 사용할 수 있습니다.

API를 사용하여 PSD 파일에 새 레이어 추가하기

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}

### **Jpeg, Png, Gif, Ai, Tiff, Bmp 파일로부터 새 레이어 추가**
어떤 [지원되는 형식](/psd/ko/net/supported-file-formats/)의 파일이라도 이미지에 새 레이어로 추가할 수 있습니다. 그러나 직접로드할 수 없습니다.

스트림에서 지원 형식의 파일로부터 새 PSD 레이어를 추가하기 위해 아래 코드를 사용할 수 있습니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

### **모든 레이어 또는 레이어 그룹 평평하게 만들기**
사용자에게 편집 가능한 PSD 파일을 제공하고 싶지 않은 경우 유용할 수 있습니다. 또한 파일이 평평화되었는지 API를 통해 식별할 수 있습니다.

PSD 파일의 레이어 평평화:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}
