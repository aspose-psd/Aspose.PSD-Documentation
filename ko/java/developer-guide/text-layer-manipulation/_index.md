---
title: Aspose.PSD for Java에서 텍스트 레이어 작업하기
weight: 100
type: docs
description: PSD 파일에서 텍스트 레이어 작업하는 방법 예시
keywords: [텍스트 레이어, 텍스트 업데이트, 텍스트 편집, 텍스트 스타일, 텍스트 단락, psd api, java, 코드 샘플]
url: ko/java/text-layer-manipulation/
---

## **개요**

**개요**

Aspose.PSD for Java는 Java 응용 프로그램 내에서 PSD (사진 파일 문서) 파일을 원활하게 처리하기 위해 설계된 강력한 라이브러리입니다. 이 라이브러리에는 PSD 파일 내의 텍스트 레이어를 편집하는 데 포괄적으로 지원하는 기능이 포함되어 있습니다. 이 기사에서는 Aspose.PSD for Java를 사용하여 PSD 파일에서 텍스트 편집하는 두 가지 다른 방법, 즉 간단한 방법과 텍스트 부분을 활용한 더 복잡한 방법에 대해 살펴볼 것입니다.

**텍스트 레이어 간단히 업데이트하는 방법**
Aspose.PSD for Java를 사용하여 PSD 파일의 텍스트 레이어를 업데이트하는 것은 간단합니다. TextLayer 클래스의 updateText 메서드를 사용하면 텍스트 레이어 내의 텍스트 내용을 쉽게 업데이트할 수 있습니다. 아래는 텍스트 레이어를 업데이트하는 간단한 방법을 보여주는 코드 예시입니다:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-text-layer-manipulation-simple.java" >}}

**텍스트 부분 사용하기**

텍스트 부분을 활용한 텍스트 레이어 업데이트 강화 방법: 간단한 방법은 기본 텍스트 수정에 충분하지만, 텍스트 스타일링과 서식에 대한 더 정교한 제어가 필요한 경우, 텍스트 부분을 활용하는 것이 더 강력한 솔루션을 제공합니다. 텍스트 부분을 사용하면 텍스트 레이어 내에서 다양한 스타일과 단락을 지정할 수 있습니다. 다음 코드 스니펫은 이 접근 방법을 보여줍니다:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-text-layer-manipulation-text-portion.java" >}}

제공된 코드에서 우리는 먼저 업데이트할 대상 텍스트 레이어에 액세스합니다 (예: image.getLayers()[1]). 그런 다음 텍스트 레이어에서 textData 객체를 검색하여 텍스트 부분을 조작할 수 있도록합니다. 기본 스타일과 단락 객체 (defaultStyle 및 defaultParagraph)를 만들어서 텍스트 부분의 기준 스타일 및 단락으로 사용합니다.

그런 다음 텍스트 레이어에 포함할 텍스트 부분을 정의합니다. 각 부분은 고유한 스타일과 서식을 가진 텍스트 세그먼트를 나타냅니다. 이 예에서는 "E=mc", "2\r", "볼드", "이탤릭\r" 및 "소문자 텍스트"라는 다섯 개의 텍스트 부분 및 해당 스타일을 조정합니다.

그런 다음 새 부분을 반복하고 addPortion 메서드를 사용하여 textData 객체에 추가합니다. 마지막으로, textData 객체의 updateLayerData 메서드를 호출하여 새로 정의된 텍스트 부분으로 텍스트 레이어를 업데이트할 수 있습니다.

**결론**
Aspose.PSD for Java는 PSD 파일 내에서 텍스트 조작에 강력한 기능을 제공합니다. 텍스트 내용을 업데이트하거나 고급 스타일링과 서식을 구현해야하는 경우 Aspose.PSD for Java가 필요한 도구를 제공합니다. 간단한 방법 또는 텍스트 부분을 활용한 더 정교한 방법을 사용하여 PSD 파일 내의 텍스트 레이어를 원활하게 조작할 수 있습니다.

자세한 내용은 전체 예시를 참조하십시오.

## **예시**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-text-layer-manipulation-full.java" >}}
