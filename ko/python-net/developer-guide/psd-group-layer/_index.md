---
title: Aspose.PSD를 Python에서 그룹 레이어 사용 예제
weight: 100
type: docs
description: Python을 통한 PSD 파일의 그룹 레이어 사용법
keywords: [레이어 그룹, 그룹 레이어, 레이어를 그룹에 추가, psd api, python, 코드 샘플]
url: /ko/python-net/psd-group-layer/
---

## **개요**

Aspose.PSD를 Python에서 그룹 레이어를 사용하는 것은 PSD 이미지 내에서 레이어를 조직화하고 조작할 수 있는 강력한 기능입니다. 그룹 레이어 또는 폴더 레이어로도 알려진 그룹 레이어는 여러 레이어를 그룹화하고 전체 그룹에 변환 또는 효과를 적용할 수 있는 방법을 제공합니다.

이 예에서는 먼저 PsdImage.create 메서드를 사용하여 새 PSD 이미지를 만듭니다. 그런 다음 PsdImage 객체의 add_layer_group 메서드를 사용하여 새 LayerGroup 객체를 만듭니다. 그룹 레이어의 이름("폴더"), 삽입해야 할 인덱스(0), 그리고 그룹 레이어가 표시될지 여부를 나타내는 부울 플래그를 제공합니다.

다음으로 두 Layer 객체를 만들고 display_name 속성을 사용하여 표시 이름을 설정합니다. add_layer 메서드를 사용하여 이러한 레이어를 그룹 레이어에 추가합니다.

마지막으로 LayerGroup 객체의 layers 속성을 사용하여 그룹 내의 레이어에 액세스할 수 있습니다. 예에서는 그룹 내 첫 번째 레이어와 두 번째 레이어의 표시 이름이 각각 "Layer 1" 및 "Layer 2"인지 단언합니다.

그룹 레이어를 조작한 후에는 PsdImage 객체의 save 메서드를 사용하여 수정된 PSD 이미지를 저장할 수 있습니다.

이것은 Aspose.PSD를 Python에서 그룹 레이어를 사용하는 방법을 시작할 수 있는 기본적인 예제입니다. 라이브러리는 PSD 이미지 내의 레이어를 조작하고 변환하기 위한 많은 고급 기능을 제공합니다. 라이브러리의 그룹 레이어와 기타 기능에 대한 자세한 설명과 예제는 Aspose.PSD를 Python에서 사용하기 위한 문서를 참조하십시오.

Aspose.PSD를 Python에서 그룹 레이어를 사용하려면 LayerGroup 클래스를 사용할 수 있습니다. 아래는 그룹 레이어를 만들고 레이어를 추가하여 수정된 PSD 이미지를 저장하는 방법을 보여주는 예제 코드 스니펫입니다.

전체 예제를 확인하십시오.

## **예제**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}
