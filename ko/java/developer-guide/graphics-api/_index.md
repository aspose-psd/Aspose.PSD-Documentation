---
title: PSD 파일에서 레이어를 편집하는 그래픽 API 사용
weight: 100
type: docs
description: Java에서 Aspose.PSD의 Graphics API를 사용하는 예제
keywords: [레이어 업데이트, 원 그리기, 타원 그리기, 채워진 원 그리기, 그래픽, psd api, java, 코드 샘플]
url: ko/java/graphics-api/
---

## **개요**
먼저 Image.load() 메소드를 사용하여 PSD 파일을 로드하거나 처음부터 Psd Image를 생성하여 시작합니다. inputFile 변수를 사용하여 PSD 파일의 경로를 나타내고 필요한 경우 loadOpt로 로딩 옵션을 지정합니다.

다음으로 psdImage.getLayers()[0] 문법을 사용하여 PSD 이미지의 첫 번째 레이어에 액세스하여 조작을 위한 레이어 객체에 대한 참조를 얻습니다.

레이어를 편집하려면 레이어를 매개변수로 전달하여 Graphics 객체를 생성합니다. 이 객체는 다양한 모양을 그리고 브러시를 적용할 수 있는 다양한 메소드를 제공합니다.

Pen 객체는 모양의 외곽선의 색상과 두께를 정의하는 데 사용됩니다. 마찬가지로 LinearGradientBrush와 같은 브러시는 채우기 색상을 정의하는 데 사용됩니다.

graphics.drawEllipse()와 같은 메소드를 사용하여 레이어에 모양을 그리고 graphics.fillEllipse()를 사용하여 채웁니다.

레이어에 원하는 변경 사항을 적용한 후에는 psdImage.save()를 사용하여 수정된 PSD 이미지를 저장합니다.

또한 적절한 옵션을 사용하여 PNG와 같은 다른 형식으로 수정된 이미지를 저장할 수 있습니다.

이제! Java에서 Aspose.PSD의 Graphics API를 사용하여 PSD 파일의 레이어를 편집하는 데 성공했습니다. 이미지 편집 능력을 향상시키기 위해 Aspose.PSD 라이브러리의 더 많은 기능과 기능을 살펴보세요.

전체 예제를 확인하세요.

## **예제**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}
