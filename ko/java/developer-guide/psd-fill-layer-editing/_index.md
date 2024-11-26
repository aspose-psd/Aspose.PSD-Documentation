---
title: 자바를 사용하여 PSD 채움 레이어 업데이트
weight: 100
type: docs
description: 컬러 채움, 그라디언트 채움 및 패턴 채움을 포함한 모든 조정 레이어 유형 사용 예제
keywords: [채움 레이어, 컬러 채움, 그라디언트 채움, 패턴 채움, psd api, 자바, 코드 샘플]
url: ko/java/psd-fill-layer-editing/
---

## **개요**

일반 레이어를 생성하는 것은 createRegularLayer 함수를 사용하여, 레이어의 위치 및 크기를 정의하는 매개변수가 필요합니다. 이 함수는 새로운 레이어를 생성하고 그 경계를 설정하며 지정된 색상으로 채웁니다.

컬러 채움 레이어의 경우 FillLayer.createInstance 메서드를 사용하고 FillType.Color 매개변수를 사용합니다. 채움 레이어가 생성되면 fill_settings 속성을 통해 채움 설정에 액세스하고 ColorFillSettings 클래스의 color 속성을 사용하여 원하는 색상을 설정합니다. 이 문맥에서는 색상이 Color.getCoral()로 설정됩니다. 또한 채움 레이어의 클리핑 속성을 1로 설정하여 클리핑 마스크로 작동하도록합니다.

그라디언트 채움 레이어는 FillLayer.create_instance 메서드를 사용하여 유사하게 생성되지만 FillType.Gradient 매개변수를 사용합니다. 컬러 채움 레이어와 마찬가지로 fill_settings를 통해 채움 설정에 액세스하고 그라디언트 색점 및 투명도 색점을 설정합니다. 이 예에서 그라디언트 색점은 GradientColorPoint 클래스로 정의되고 투명도 색점은 GradientTransparencyPoint 클래스로 정의됩니다. 또한 채움 레이어의 클리핑 속성도 1로 설정됩니다.

패턴 채움 레이어는 FillLayer.createInstance를 사용하여 FillType.Pattern 매개변수로 생성됩니다. 다시 한 번 fill_settings를 통해 채움 설정에 액세스하고 패턴 데이터 및 기타 속성을 설정합니다. 이 코드에서는 패턴 데이터가 PatternFillSettings 클래스를 사용하여 정의되고 클리핑 속성이 1로 설정됩니다.

채움 레이어를 생성한 후 각 채움 레이어에 대한 디스플레이 이름 및 기타 속성을 지정하여 PSD 이미지에 추가합니다.

마지막으로 제공된 코드를 사용하여 PSD 이미지와 해당 PNG 이미지를 저장합니다. PNG 옵션은 투명도를 위해 알파와 함께 트루 색상을 사용하도록 구성됩니다.

자세한 내용은 전체 예제를 참조하십시오.

## **예제**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}
