---
title: PSD, PSB 및 AI 파일 열기 및 PDF, PNG, TIFF, GIF, BMP, JPEG로 내보내기
weight: 100
type: docs
description: PSD, PSB 및 AI 파일을 다른 형식으로 내보내는 예제
keywords: [psd 열기, ai 열기, psb 열기, png로 내보내기, pdf로 내보내기, jpeg로 내보내기, tiff로 내보내기, psd api, python, 코드 샘플]
url: ko/python-net/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **개요**
PSD, PSB 및 AI 파일을 다른 형식으로 변환하려면 Python에서 Aspose.PSD 라이브러리를 사용할 수 있습니다. 해당 라이브러리는 변환 과정을 사용자 정의할 수 있는 다양한 옵션과 설정을 제공합니다.

먼저 Aspose.PSD 라이브러리에서 필요한 클래스 및 모듈을 가져와야 합니다. 코드를 실행하기 전에 해당 라이브러리가 설치되어 있는지 확인해야 합니다.

이 코드에서는 PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB 및 PSD와 같은 다양한 포맷을 위한 다양한 옵션을 정의합니다. 이러한 옵션을 사용하여 출력 파일을 요구 사항에 맞게 사용자 정의할 수 있습니다.

다음으로, 파일 확장자를 해당 저장 옵션으로 매핑하는 formats 사전을 정의합니다.

PSD 파일을 다른 형식으로 변환하려면 PsdImage.load()를 사용하여 PSD 파일을 로드하고 formats 사전을 반복해야 합니다. 각 포맷에 대해 출력 파일 이름을 지정하고 image.save() 메서드를 사용하여 이미지를 저장합니다.

마찬가지로, AI 파일을 다른 형식으로 변환하려면 AiImage.load()를 사용하여 AI 파일을 로드하고 formats 사전을 반복해야 합니다. 출력 파일 이름을 지정하고 image.save() 메서드를 사용하여 이미지를 저장합니다.

소스 PSD 및 AI 파일에 대한 올바른 파일 경로를 제공해야 합니다.

이제 이 코드를 사용하여 Aspose.PSD를 사용하여 PSD, PSB 및 AI 파일을 다양한 형식으로 변환할 수 있습니다.

전체 예제를 확인하세요.

## **예시**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
