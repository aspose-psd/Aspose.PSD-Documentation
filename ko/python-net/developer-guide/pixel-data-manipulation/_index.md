---
title: Aspose.PSD를 사용한 Python을 활용한 픽셀 데이터 조작
weight: 100
type: docs
description: PSD Python API를 사용하여 원시 픽셀 데이터를 직접 신속하게 업데이트하는 방법의 예시
keywords: [픽셀 편집, psd 편집, 레이어 편집, 원시 데이터 조작, psd 데이터 편집, psd api, python, 코드 샘플]
url: /ko/python-net/pixel-data-manipulation/
---

## **소개**
Aspose.PSD는 Python에서 Adobe Photoshop 파일 (PSD)을 다룰 수 있는 강력한 라이브러리입니다. 이 기사에서는 Aspose.PSD를 사용하여 PSD 파일에서 픽셀 데이터를 조작하는 방법을 살펴보겠습니다.

## **개요**
제공된 코드는 PSD 파일을 만들고, 새 레이어를 추가한 다음 픽셀 데이터를 직접 조작하고 수정된 이미지를 저장하는 방법을 보여줍니다.

필요한 모듈 가져오기: 첫 번째 단계는 필요한 모듈을 가져오는 것입니다. io 라이브러리에서 BytesIO 모듈을 가져오고, aspose.psd.fileformats.psd 및 aspose.psd.fileformats.psd.layers 모듈에서 각각 PsdImage 및 Layer 클래스를 가져옵니다.

다음으로, 입력 및 출력 파일 경로를 정의합니다.

스트림으로 입력 파일 열기: 입력 파일을 "rb" 모드로 open 함수를 사용하여 스트림으로 엽니다. 버퍼링 인수는 0으로 설정하여 버퍼링을 비활성화합니다. 파일 내용은 BytesIO 스트림으로 읽혀지며, stream.seek(0)을 사용하여 스트림을 맨 처음으로 설정합니다.

Layer 클래스 생성자에 스트림을 전달하여 PSD 레이어 객체를 생성합니다.

PsdImage 클래스 생성자를 사용하여 너비와 높이를 인수로 제공하여 새 PSD 이미지를 만듭니다.

대입 연산자(=)를 사용하여 PSD 이미지의 레이어를 layers 속성에 할당합니다.

픽셀 데이터를 조작하기 위해 먼저 load_argb_32_pixels 메서드를 사용하여 레이어에서 ARGB32 픽셀을 로드합니다. 결과를 pixels 변수에 저장합니다.

다음으로, 픽셀 배열의 길이를 기반으로 인덱스 범위 (pixelsRange)를 정의합니다. 그런 다음 인덱스를 반복하며 인덱스가 5로 나누어떨어지는지 확인합니다. 해당 인덱스에서 픽셀 값을 500000으로 설정합니다. 따라서 반복되는 패턴을 만들고자 합니다. 원하는 대로 픽셀 데이터를 변경할 수 있습니다.

그런 다음 save_argb_32_pixels 메서드를 사용하여 수정된 픽셀 데이터를 레이어에 저장합니다.

마지막으로 save 메서드를 사용하여 수정된 PSD 이미지를 출력 파일에 저장합니다.
   
본 기사에서는 Aspose.PSD를 사용하여 Python에서 PSD 파일의 픽셀 데이터를 조작하는 방법을 살펴보았습니다. 제공된 코드를 이해하면 일부 조건에 따라 픽셀을 수정하는 등 다양한 픽셀 수준의 작업을 수행할 수 있습니다. Aspose.PSD는 PSD 파일을 프로그래밍 방식으로 작업하는 데 유용한 기능 세트를 제공하여 Python에서 이미지 조작 작업에 유용한 도구가 됩니다.

제공된 코드는 이미 Aspose.PSD 라이브러리와 그 종속성이 설치되어 있다고 가정합니다. Aspose.PSD를 Python에서 설치하고 사용하는 방법에 대한 자세한 내용은 공식 문서에서 확인할 수 있습니다.

전체 예제를 확인하세요.

## **예시**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-pixel-data-manipulation.py" >}}
