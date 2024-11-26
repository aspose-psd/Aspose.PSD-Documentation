---
title: Python를 사용한 PSD 채우기 레이어 업데이트
weight: 100
type: docs
description: Color Fill, Gradient Fill 및 Pattern Fill을 포함한 모든 종류의 조정 레이어 사용 예시
keywords: [fill layer, Color Fill, Gradient Fill, Pattern Fill, psd api, python, code sample]
url: ko/python-net/psd-fill-layer-editing/
---

## **개요**

정규 레이어를 만들려면 코드에서 제공되는 create_regular_layer 함수를 사용할 수 있습니다. 이 함수는 레이어의 위치와 크기를 정의하는 left, top, width 및 height 매개변수를 사용합니다. 새 레이어를 만들고 해당 경계를 설정한 다음 지정된 색상으로 채웁니다.

색상 채우기 레이어를 만들려면 FillType.COLOR 매개변수를 사용하여 FillLayer.create_instance 메서드를 사용할 수 있습니다. 채우기 레이어를 만든 후 fill_settings 속성을 사용하여 채우기 설정에 액세스하고 ColorFillSettings 클래스의 color 속성을 사용하여 색상을 설정할 수 있습니다. 제공된 코드에서는 색상을 Color.coral로 설정했습니다. 채우기 레이어의 clipping 속성을 1로 설정하여 레이어가 클리핑 마스크로 작동하게 합니다.

그라데이션 채우기 레이어를 만들려면 FillType.GRADIENT 매개변수를 사용하여 FillLayer.create_instance 메서드를 사용할 수 있습니다. 색상 채우기 레이어와 유사하게 fill_settings 속성을 사용하여 채우기 설정에 액세스하고 그라데이션 색상 포인트 및 투명도 포인트를 설정할 수 있습니다. 제공된 코드에서는 그라데이션 색상 포인트는 GradientColorPoint 클래스를 사용하여 정의되며, 투명도 포인트는 GradientTransparencyPoint 클래스를 사용하여 정의합니다. 채우기 레이어의 clipping 속성도 1로 설정됩니다.

패턴 채우기 레이어를 만들려면 FillType.PATTERN 매개변수를 사용하여 FillLayer.create_instance 메서드를 사용할 수 있습니다. 다시 한번 fill_settings 속성에 액세스하여 패턴 데이터 및 기타 속성을 설정할 수 있습니다. 제공된 코드에서는 패턴 데이터가 PatternFillSettings 클래스를 사용하여 정의되며, clipping 속성은 1로 설정됩니다.

채우기 레이어를 만든 후 add_layer 메서드를 사용하여 PSD 이미지에 추가할 수 있습니다. 또한 각 채우기 레이어의 표시 이름 및 기타 속성을 지정할 수 있습니다.

마지막으로, 제공된 코드를 사용하여 PSD 이미지와 해당 PNG 이미지를 저장할 수 있습니다. PNG 옵션은 투명도를 위해 알파 채널을 사용하는 truecolor로 설정됩니다.

전체 예제를 확인해주세요.

## **예제**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}
