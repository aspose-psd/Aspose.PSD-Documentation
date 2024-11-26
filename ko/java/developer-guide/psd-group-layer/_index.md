---
title: Aspose.PSD를 사용한 Java에서 그룹 레이어 사용 예
weight: 100
type: docs
description: Java를 통한 PSD 파일의 그룹 레이어 사용
keywords: [레이어 그룹, 그룹 레이어, 레이어를 그룹에 추가, psd api, java, 코드 샘플]
url: ko/java/psd-group-layer/
---

## **개요**

Aspose.PSD를 사용한 Java에서 그룹 레이어를 활용하면 PSD 이미지 내에서 레이어를 효과적으로 관리하고 구성할 수 있습니다. 그룹 레이어 또는 폴더 레이어로도 불리는 그룹 레이어를 사용하면 여러 레이어를 묶어 변형이나 효과를 일괄적으로 적용할 수 있습니다.

먼저 PsdImage.create() 메서드를 사용하여 새 PSD 이미지를 만듭니다. 그런 다음 PsdImage 객체의 addLayerGroup 메서드를 통해 새 LayerGroup 객체를 초기화합니다. 그룹 레이어에 원하는 이름("폴더"), 삽입 인덱스(0) 및 가시성 여부(참)를 설정합니다.

이후 두 개의 Layer 개체를 만든 다음 setDisplayName 메서드를 사용하여 표시 이름을 설정합니다. addLayer 메서드를 사용하여 이러한 레이어를 그룹 레이어에 추가합니다.

그룹 내의 레이어에 액세스하려면 LayerGroup 객체의 layers 속성을 활용합니다. 그룹 내 첫 번째 및 두 번째 레이어의 표시 이름이 각각 "Layer 1" 및 "Layer 2"인지 확인합니다.

그룹 레이어를 조작한 후에 PsdImage 객체의 save 메서드를 사용하여 수정된 PSD 이미지를 저장합니다.

이것은 Aspose.PSD를 사용한 Java에서 그룹 레이어 작업에 익숙해지는 데 도움이 되는 기본적인 예제로, PSD 이미지 내에서 레이어 조작 및 변형을 위한 많은 고급 기능을 제공합니다. 라이브러리의 그룹 레이어 및 라이브러리의 기타 기능을 활용한 예제에 대한 자세한 내용 및 예제는 Aspose.PSD를 위한 Java 설명서를 참조하십시오.

Java에서 Aspose.PSD의 그룹 레이어를 다루기 위해 LayerGroup 클래스를 사용하십시오. 아래는 그룹 레이어를 만들고 레이어를 추가하고 수정된 PSD 이미지를 저장하는 방법을 보여주는 코드 스니펫입니다.

제공된 완전한 예제를 참조하십시오.

## **예시**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}
