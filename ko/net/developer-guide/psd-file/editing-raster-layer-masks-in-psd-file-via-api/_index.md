---
title: API를 통한 PSD 파일의 래스터 레이어 마스크 편집
type: docs
weight: 20
url: /ko/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **개요**
**Adobe® Photoshop® 없이 PSD 형식을 자동화하고 PSD 파일을 변경하려면 아래 제공된 Aspose.PSD API를 사용할 수 있습니다. PSD 파일을 수정하는 데 도움이 되는 C# 및 .NET 코드 스니펫이 있습니다.**

PSD 레이어 및 벡터 마스크를 사용하면 레이어 픽셀을 영구적으로 삭제하지 않고 숨기거나 보여줄 수 있습니다. 래스터 마스크는 레이어 마스크 또는 사용자 마스크라고도합니다. Aspose.PSD에서 래스터 및 벡터 마스크에 액세스하려면 '[LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata)' 레이어 속성을 통해 제공됩니다. 이 속성은 추상 'LayerMaskData' 클래스의 하위 클래스 인 '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' 및 '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' 클래스가 될 수 있습니다. 레이어에 래스터 및 벡터 마스크가 모두있는 경우 [LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull) 인스턴스가 제공됩니다. 레이어에 래스터 또는 벡터 마스크만 있는 경우 [LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort) 인스턴스가 제공됩니다. LayerMaskData 속성이 null이면 레이어에 마스크가 없거나 비활성화된 벡터 마스크만 있습니다.


|![할 일: 이미지 대체 텍스트](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>래스터 마스크 및 비활성화된 벡터 마스크 LayerMaskDataShort</p><p>비활성화된 래스터 마스크 LayerMaskDataShort</p><p>래스터 마스크 및 벡터 마스크 LayerMaskDataFull</p><p>래스터 마스크 LayerMaskDataShort</p><p>벡터 마스크 LayerMaskDataShort</p><p>비활성화된 벡터 마스크 없음 (그러나 벡터 리소스가 존재함)</p>|
| :- | :- |

## **PSD 파일에서 레이어 래스터 마스크를 가져오는 방법**
먼저, 레이어에 벡터 및 레이어 마스크가 있는지 확인해야 합니다.

다음으로 제공된 샘플 코드는 레이어 래스터 마스크를 가져오는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

그렇지 않으면 LayerMaskData 레이어 속성의 타입은 LayerMaskDataShort입니다. 이 경우, 레이어가 래스터 마스크만 가지고 있는지 Flags 속성을 확인하여 확인해야 합니다. [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags) **UserMaskFromRenderingOtherData** 플래그를 포함하면 마스크는 벡터 마스크 캐시입니다.

마스크 코드 스니펫 가져오기:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

양쪽 마스크가 존재할 때도 추가 조작을 위해 레이어 마스크를 LayerMaskDataShort로 추출해야하는 경우 LayerMaskDataFull을 추출하고 LayerMaskDataShort로 변환해야합니다. 다음 코드는 두 경우에 모두 사용할 수 있습니다:

PSD에서 래스터 마스크 추출

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}

## **PSD 파일의 레이어에 래스터 마스크가 있는지 확인하는 방법**
다음 C# 코드는 레이어에 래스터 마스크가 있는지 확인하는 데 도움이 될 수 있습니다:

[PSD 레이어에 래스터 마스크가 적용되었는지 확인하는 방법](/psd/ko/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}

## **PSD 파일에서 레이어 래스터 마스크를 제거 / 추가 / 업데이트하는 방법**
레이어 MaskData를 삭제 / 추가 / 업데이트하는 것만으로는 올바르게 저장하기에는 충분하지 않습니다. 채널이 업데이트되지 않습니다. 적절한 렌더링을 제공 할 수 있지만 마스크 채널이 변경되지 않습니다:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

레이어 AddLayerMask 메서드를 사용하여 레이어 마스크를 제거 / 추가 / 업데이트해야합니다.

마스크 및 채널을 추가/업데이트합니다:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

마스크 및 채널을 제거합니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}

## **PSD 이미지에서 레이어 래스터 마스크 제거**
먼저 마스크가 전형적인 형식에 있는지 확인하고 벡터 마스크가 아닌 경우 래스터 마스크를 삭제하기 위해 null을 인수로 AddLayerMask 메서드를 호출할 수 있습니다. 그러나 전체 형식의 경우 이를 짧은 형식으로 변환하여 벡터 마스크 만 남겨야합니다. 레이어 마스크를 제거하는 데 다음 C# .NET 코드 스니펫을 사용할 수 있습니다:

PSD 파일에서 레이어 마스크 제거하는 코드 스니펫.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

## **PSD 이미지에서 레이어 래스터 마스크 업데이트**
이것은 간단합니다. 형식이 짧은 형식인 경우 ImageData 및 MaskRectangle를 필요한 경우 변경해야하며, 그렇지 않으면 [UserMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata) 및 [UserMaskRectangle](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)를 변경해야합니다. 레이어 마스크를 업데이트하는 데 사용할 수있는 다음 C# .NET 코드 스니펫은 다음과 같습니다:

C#로 PSD 레이어 마스크 업데이트

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

다음은 레이어 사용자 마스크를 반전시키는 가능한 조작의 예입니다:

C#로 PSD 레이어 마스크 업데이트

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}

## **PSD 파일에서 레이어 래스터 마스크가 존재하는 경우 벡터 마스크 업데이트**
사용자가 이미 벡터 경로 리소스를 변경했다고 가정합니다. 그럼 AddLayerMask 레이어 메서드를 호출하여 벡터 마스크를 쉽게 업데이트 할 수 ​​있습니다:

[PSD 레이어 벡터 마스크](/psd/ko/net/layer-vector-mask/) 업데이트

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}

## **PSD 파일에 레이어 래스터 마스크 추가**
레이어에 마스크가 없는 경우 AddLayerMask 레이어 메서드를 호출하여 주어진 래스터 마스크를 추가 할 수 있습니다.

마스크가 [UserMaskFromRenderingOtherData**](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags) 플래그가없으면 이미 래스터 마스크가있기 때문에 방금 설명한대로 업데이트해야합니다. 그렇지 않으면 해당 마스크를 전체 형식으로 변환합니다. 그렇지 않으면 그대로 사용합니다. 그런 다음 UserMaskData, UserMaskRectangle 및 기타 속성을 주어진 마스크 속성으로 업데이트하십시오. 레이어 마스크를 추가 (업데이트)하는 데 사용할 수있는 다음 C# .NET 코드 스니펫은 다음과 같습니다:

PSD에 새로운 레이어 마스크 추가

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **레이어 마스크가 활성화되었는지 확인하는 방법**
레이어 래스터 마스크가 활성화 된 상태를 확인하기 위해 LayerMaskDataShort에있는 Flags 속성 또는 LayerMaskDataFull에있는 RealFlags에 대한 Flags 속성에서 LayerMaskFlags.Disabled 플래그 상태를 확인할 수 있습니다. 다음 C# .NET 코드 스니펫을 사용하여 레이어 마스크가 활성화 된 상태를 얻을 수 있습니다:

마스크가 활성화되었는지 확인:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}

## **래스터 레이어 마스크를 활성화 또는 비활성화하는 방법**
레이어 래스터 마스크를 활성화 또는 비활성화하려면 LayerMaskDataShort의 Flags 속성 또는 LayerMaskDataFull의 RealFlags에서 LayerMaskFlags.Disabled 플래그 상태를 변경할 수 있습니다. 다음 C# .NET 코드 스니펫은 레이어 마스크 활성화 상태를 변경하는 데 사용할 수 있습니다:

래스터 레이어 마스크 활성화 또는 비활성화:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}
