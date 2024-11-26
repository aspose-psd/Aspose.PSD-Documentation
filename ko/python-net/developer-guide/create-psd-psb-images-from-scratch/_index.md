---
title: Python를 사용하여 스크래치에서 PSD 또는 PSB 이미지 만들기
weight: 100
type: docs
description: Python을 사용하여 Aspose.PSD가 스크래치에서 Psd 이미지를 만드는 예제
keywords: [psd 만들기, psb 만들기, 새로 만들기, 레이어 만들기, 텍스트 레이어 만들기, psd api, python, 코드 샘플]
url: ko/python-net/create-psd-psb-images-from-scratch/
---

## **개요**
Python을 사용하여 Aspose.PSD가 스크래치에서 PSD 또는 PSB 파일을 만드는 방법을 살펴보겠습니다:

Aspose.PSD 라이브러리에서 필요한 모듈 및 클래스를 가져옵니다:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

출력 파일 이름과 경로를 지정합니다:
```python 
outputFile = "CreateFileFromScratchExample.psd"
```

원하는 차원으로 PSD 이미지를 만듭니다:
```python 
with PsdImage(500, 500) as img:
```

일반 PSD 레이어를 추가하고 그래픽 API를 사용하여 업데이트합니다:
```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

텍스트 레이어를 만듭니다:
```python 
textLayer = img.add_text_layer("Sample Text", Rectangle(200, 200, 100, 100))
```

텍스트 레이어에 그림자 효과를 추가합니다:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

PSD 파일을 저장합니다:
```python 
img.save(outputFile)
```

이 코드는 500x500 픽셀 크기의 PSD 이미지를 만듭니다. 레귤러 레이어를 추가하고 펜과 브러시를 사용하여 해당 레이어에 타원을 그립니다. 그런 다음 "샘플 텍스트"를 포함하는 텍스트 레이어를 추가하고 해당 레이어에 그림자 효과를 적용합니다. 마지막으로 지정된 출력 파일 이름으로 PSD 파일을 저장합니다.

이 코드가 작동하려면 Python 환경에 Aspose.PSD 라이브러리가 설치되어 있고 적절히 설정되어 있어야 합니다. 자세한 내용은 공식 Aspose.PSD 문서를 참조하세요.

전체 예제를 확인하십시오.

## **예제**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
