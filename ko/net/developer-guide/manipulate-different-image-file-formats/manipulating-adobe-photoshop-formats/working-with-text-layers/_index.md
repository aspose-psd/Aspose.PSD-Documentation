---
title: 텍스트 레이어 작업
type: 문서
weight: 170
url: /ko/net/working-with-text-layers/
---

## **텍스트 레이어 추가**
Aspose.PSD for .NET을 사용하면 PSD 파일에 텍스트 레이어를 추가할 수 있습니다. PSD 파일에 텍스트 레이어를 추가하는 단계는 아래와 같이 간단합니다:

- [**이미지 클래스**](https://reference.aspose.com/psd/net/aspose.psd/image)에서 노출된 팩토리 메소드 [**로드**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index)를 사용하여 PSD 파일을 이미지로 로드합니다.
- 텍스트와 [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle) 클래스의 인스턴스를 허용하는 [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) 메소드 호출
- 결과를 저장합니다

다음 코드 스니펫은 PSD 파일에 텍스트 레이어를 추가하는 방법을 보여줍니다

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **텍스트 레이어 위치 설정**
Aspose.PSD for .NET을 사용하면 PSD 파일에서 텍스트 레이어 위치를 설정할 수 있습니다. PSD 파일에서 텍스트 레이어 위치를 설정하는 단계는 아래와 같이 간단합니다:

- 이미지 클래스에서 노출된 팩토리 메소드 Load를 사용하여 PSD 파일을 이미지로 로드합니다.
- 텍스트 레이어의 왼쪽 및 위쪽 위치를 지정하면서 AddTextLayer 메소드를 호출합니다.
- 결과를 저장합니다

다음 코드 스니펫은 PSD 파일에서 텍스트 레이어 위치를 설정하는 방법을 보여줍니다

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}
## **텍스트 레이어에서 텍스트 속성 가져오기**
Aspose.PSD for .NET을 사용하면 PSD 텍스트 레이어에 있는 다른 텍스트 부분의 텍스트 속성을 가져오고 업데이트할 수 있습니다. 이 문서는 텍스트 레이어의 단락, 스타일 및 텍스트 속성을 가져오고 업데이트하는 방법을 보여줍니다.

아래 코드 스니펫은 이 요구 사항을 달성하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


다음은 [**Aspose.PSD for .NET**](https://products.aspose.com/psd/net)를 사용하여 [TextLayer](https://reference.aspose.com/net/psd/aspose.psd/fileformats/psd/layers/textlayer)에서 다양한 텍스트 부분의 텍스트 서식을 가져오는 개발자의 또 다른 예제입니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}
## **PSD 파일에서 텍스트 레이어 업데이트**
Aspose.PSD for .NET을 사용하면 PSD 파일의 텍스트 레이어에서 텍스트를 조작할 수 있습니다. PSD 레이어의 텍스트를 업데이트하려면 Aspose.PSD.FileFormats.Psd.Layers.TextLayer 클래스를 사용하십시오. 다음 코드 스니펫은 PSD 파일을 로드하고 텍스트 레이어에 액세스하여 텍스트를 업데이트하고, [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer/methods/updatetext/index) 메소드를 사용하여 새 이름으로 PSD 파일을 저장합니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **런타임에서 텍스트 레이어 지원**
이 문서는 PSD 이미지에 런타임에서 텍스트 레이어를 추가하는 방법을 보여줍니다. 아래에 코드 스니펫이 제공되었습니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
