---
title: Aspose.PSD를 사용한 Python에서 텍스트 레이어 작업
weight: 100
type: docs
description: PSD 파일에서 텍스트 레이어 작업 예제
keywords: [텍스트 레이어, 텍스트 업데이트, 텍스트 부분 편집, 텍스트 스타일, 텍스트 단락, psd api, python, 코드 샘플]
url: ko/python-net/text-layer-manipulation/
---

## **개요**

**개요**

Aspose.PSD for Python은 Python에서 PSD (포토샵 문서) 파일을 처리할 수 있는 강력한 라이브러리입니다. 이 라이브러리의 주요 기능 중 하나는 PSD 파일 내에서 텍스트 레이어를 편집할 수 있는 기능입니다. 이 문서에서는 Aspose.PSD for Python을 사용하여 PSD 파일에서 텍스트를 편집하는 두 가지 다른 방법을 살펴보겠습니다 - 간단한 방법과 텍스트 부분을 사용하는 더 강력한 방법.

** 텍스트 레이어 업데이트의 간단한 방법 **
Aspose.PSD for Python을 사용하여 PSD 파일의 텍스트 레이어를 업데이트하려면 TextLayer 클래스의 update_text 메서드를 사용할 수 있습니다. 이 메서드를 사용하면 텍스트 레이어의 텍스트 내용을 쉽게 업데이트할 수 있습니다. 다음은 텍스트 레이어를 업데이트하는 간단한 방법을 보여주는 코드 스니펫 예제입니다.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-text-layer-manipulation-simple.py" >}}

** 텍스트 부분 사용 수정 **

텍스트 부분을 사용한 텍스트 레이어 업데이트의 더 강력한 방법: PSD 파일에서 텍스트 레이어를 업데이트하는 간단한 방법은 기본적인 텍스트 편집에 적합합니다. 그러나 텍스트의 스타일링과 포맷 설정에 대해 좀 더 많은 제어가 필요한 경우 텍스트 부분을 사용하는 강력한 방법을 사용할 수 있습니다. 다음은 이 방법을 보여주는 코드 스니펫 예제입니다.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-text-layer-manipulation-text-portion.py" >}}

위의 코드에서 우리는 먼저 업데이트하려는 텍스트 레이어에 접근합니다 (image.layers[1]). 그런 다음 텍스트 레이어에서 텍스트 데이터 객체를 검색하여 텍스트 부분을 처리할 수 있습니다. 텍스트 부분에 사용할 기본 스타일 및 기본 단락 객체를 만듭니다.

다음으로 텍스트 레이어에 추가할 텍스트 부분을 정의합니다. 각 부분은 자체 스타일과 포맷을 가진 텍스트 세그먼트를 나타냅니다. 이 예제에서는 "E=mc", "2\r", "볼드", "이탤릭\r", "소문자텍스트"라는 다섯 개의 텍스트 부분이 있습니다. 또한 이러한 부분의 스타일을 요구에 맞게 업데이트합니다.

그런 다음 새 부분을 순회하고 add_portion 메서드를 사용하여 텍스트 데이터 객체에 추가합니다. 마지막으로 텍스트 데이터 객체의 update_layer_data 메서드를 호출하여 새로운 텍스트 부분으로 텍스트 레이어를 업데이트합니다.

**결론**
Aspose.PSD for Python은 PSD 파일에서 텍스트를 편집할 수 있는 강력한 기능을 제공합니다. 텍스트 레이어의 텍스트 내용을 업데이트하거나 더 고급스러운 스타일과 포맷을 적용해야 하는 경우 Aspose.PSD for Python을 사용하면 됩니다. 간단한 방법이나 텍스트 부분을 사용하는 보다 강력한 방법을 사용하여 PSD 파일의 텍스트 레이어를 쉽게 조작할 수 있습니다.

전체 예제를 확인해주십시오.

## **예제**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-text-layer-manipulation-full.py" >}}
