---
title: 레이어 작업
type: docs
weight: 150
url: /ko/net/working-with-layers/
---

## **레이어 그룹 만들기**
레이어 그룹은 하나 이상의 레이어로 이루어져 있으며 비슷하거나 관련된 레이어를 구성하는 데 도움이 됩니다. Aspose.PSD for .NET을 사용하여 레이어 그룹을 만들 수 있습니다. 이를 위해 **[AddLayerGroup 메서드](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)** 가 **[PsdImage 클래스](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** 에 추가되어 레이어 그룹을 추가합니다.

레이어 그룹을 만드는 단계는 다음과 같습니다:

- PsdImage 클래스를 사용하여 지정된 너비, 높이 및 이미지 옵션으로 이미지 인스턴스를 만듭니다.
- [LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/layers/layergroup)를 지정된 그룹 이름 및 인덱스로 생성합니다.
- Layer 클래스의 인스턴스를 만들고 PSD 이미지를 할당합니다.
- 레이어 그룹에 생성한 레이어를 LayerGroup 클래스에서 노출된 AddLayer 메서드를 사용하여 추가합니다.
- 결과를 저장합니다.

다음 코드 스니펫은 레이어 그룹을 만드는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}

## **레이어 이름 변경**
원하는 이름을 사용할 수 있지만, 일반적으로 해당 레이어에있는 개체 또는 요소에 대한 일반적인 설명을 제공하는 것이 좋습니다. 이 문서는 Aspose.PSD for .NET을 사용하여 레이어 이름을 변경하는 방법을 보여줍니다. 이를 위해 제대로 레이어 이름을 표시하기 위해 Layer 클래스에 새로운 **[DisplayName](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/displayname)** 속성이 추가되었습니다. Photoshop이 **[Name](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/name)** 속성을 사용하여 레이어 이름을 저장할 때 한국어 문자가 ASCII에서 바이트 63'?'으로 저장되는 것으로 관찰되었습니다. 따라서 레이어 이름을 제대로 표시하려면 한국어 문자를 지원하지 않는 Name 속성 대신 DisplayName 속성을 사용하십시오.

다음 코드 샘플은 레이어 이름을 변경하는 방법을 보여줍니다. 

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **링크된 레이어 지원**
레이어를 링크하는 것은 레이어를 그룹화하는 것과 같습니다. 두 개 이상의 레이어를 링크하면 링크된 레이어 모두에 일부 변경 사항을 적용할 수 있게 됩니다. 예를 들어 한 레이어에 변형을 적용하면 다른 모든 링크된 레이어에도 적용됩니다. 이 문서는 [Aspose.PSD](https://products.aspose.com/psd)를 사용하여 링크된 레이어를 가져오고 연결을 해제하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
