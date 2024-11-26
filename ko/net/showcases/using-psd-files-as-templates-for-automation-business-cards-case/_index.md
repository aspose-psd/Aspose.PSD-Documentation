---
title: PSD 파일을 템플릿으로 사용하여 자동화하기 - 명함 사례
type: docs
weight: 10
url: /ko/net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **개요**
이 문서에서는 PSD/PSB 파일이 일종의 알려진 템플릿 구조를 갖는 경우 PSD 파일에서 일부 레이어를 프로그래밍 방식으로 업데이트해야 하는 경우에 자주 사용되는 사례를 설명합니다. 이는 다른 사람들을 위해 다량의 명함을 만들거나(명함 사례) PSD 파일을 다른 언어로 번역하고 그래픽 자료 일부를 대체해야 하는 경우에 사용될 수 있습니다.

이 문서를 읽고 나면 여러분은 다음을 할 수 있을 것입니다:

![할 일: 이미지 대체 텍스트](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **간단한 사례**
예를 들어, 알려진 레이어명이 포함된 PSD 템플릿이 있는 경우입니다. 따라서 C#을 통해 PSD 레이어를 변경, 업데이트하거나 교체해야 합니다. 먼저 Aspose.PSD로 템플릿 파일을 열어야 합니다.

C#을 통해 PSD 파일을 열려면?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![할 일: 이미지 대체 텍스트](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

그런 다음 원하는 레이어를 이름으로 찾아야 합니다. 다음은 이를 위한 간단한 구현 방법입니다.

레이어를 이름으로 PSD 파일에서 찾는 방법

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}

해당 레이어를 찾으면 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)를 사용하여 일반적인 방법으로 업데이트할 수 있습니다:

PSD 레이어 Graphics에 그리는 방법

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

이 경우, 새로 불러온 [PNG 이미지](https://wiki.fileformat.com/image/png/)를 기존 PSD 레이어에 그려서 새 파일에는 이전 데이터가 손실됩니다.

하지만 텍스트도 업데이트해야 하는 경우는 어떨까요? 프로세스는 유사할 것입니다. [텍스트 레이어](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer)를 이름으로 찾고, 그 후 프로그래밍 방식으로 [Photoshop 파일의 텍스트 레이어를 업데이트](/psd/ko/net/render-text-with-different-colors-in-text-layer/)해야 합니다.

C#을 사용하여 Photoshop에서 텍스트 레이어 업데이트하는 방법

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}

마지막으로 변경 사항을 저장해야 합니다:

변경된 PSD 파일을 저장하는 방법 - [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}

결과 이미지:

![할 일: 이미지 대체 텍스트](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **추가 기능이 있는 복잡한 사례**
위에서는 PSD 파일의 레이어에서 이미지를 교체하는 가장 간단한 방법을 보여주었습니다.

그러나 Aspose.PSD는 레이어 추가, 이전 레이어 제거, 다양한 스타일로 텍스트 레이어 업데이트와 같이 더 복잡한 추가 기능을 제공할 수 있습니다.

교체하려는 [레이어](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/layer)를 찾고, 레이어 목록에서 해당 인덱스를 찾아 제거한 후, [Jpeg 파일](https://wiki.fileformat.com/image/jpeg/)에서 생성된 새 레이어를 동일한 위치에 추가합니다.

파일에서 새로운 레이어를 생성하고 [Aspose.PSD](https://products.aspose.com/psd/net)을 사용하여 PSD 이미지에 삽입하는 방법

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}

이 파일의 코드 조각 끝에서 레이어 위치를 보정하고 새 레이어 배열을 Psd 이미지에 저장합니다.

[PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage) 레이어 속성 복사하는 방법

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}

마지막으로, C#으로 기존 PSD 이미지의 텍스트 레이어를 업데이트해야 합니다. Aspose.PSD는 [텍스트 레이어를 일부로 업데이트](/psd/ko/net/working-with-text-layers/)하는 기능을 지원합니다. 각 [텍스트 부분](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/text/itextportion)에는 고유한 스타일과 문단 속성 조합이 있습니다.

[PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage) 레이어 속성 복사하는 방법

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}

결과적으로, JPEG, PNG, J2K, BMP, GIF 또는 TIFF 파일에서 새 레이어 및 여러 줄 [다른 스타일의 텍스트](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs)로 PSD 템플릿을 코드를 통해 변경하였습니다.

![할 일: 이미지 대체 텍스트](using-psd-files-as-templates-for-automation-business-cards-case_4.png)

