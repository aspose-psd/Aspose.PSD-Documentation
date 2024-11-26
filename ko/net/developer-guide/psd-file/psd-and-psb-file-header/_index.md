---
title: PSD 및 PSB 파일 헤더
type: docs
weight: 40
url: /ko/net/psd-and-psb-file-header/
---

## **설명**
Adobe Photoshop 파일 헤더에는 파일 버전 정보(PSD는 1, PSB는 2), 채널 수, 색상 모드 및 비트 깊이에 대한 정보가 포함되어 있습니다.

관련 기사에서 Aspose.PSD가 지원하는 색상 모드 및 비트 깊이 조합을 알아볼 수 있습니다.

파일 헤더에는 이미지의 기본 속성이 포함되어 있습니다.

|**길이**|**설명**|
| :- | :- |
|4|서명: 항상 *"8BPS"*와 동일합니다.|
|2|[PSD 버전](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): PSD 파일에 대해 1, PSB 파일에 대해 2일 것입니다. Aspose.PSD는 파일 형식의 버전을 감지하고 올바르게 읽을 수 있습니다.|
|6|예약된 영역: 반드시 0이어야 합니다.|
|2|이미지의 채널 수, 알파 채널 포함. 지원 범위는 1에서 56까지입니다.|
|4|이미지의 높이(픽셀 단위). 지원 범위는 1에서 30,000까지입니다. PSB 파일은 최대 300,000 픽셀까지 지원합니다. Aspose.PSD도 PSB 파일을 지원합니다.|
|4|이미지의 너비(픽셀 단위). 지원 범위는 1에서 30,000까지입니다. PSB 파일은 최대 300,000 픽셀까지 지원합니다. 대용량 PSD/PSB 파일의 일괄 처리도 Aspose.PSD에서 지원됩니다.|
|2|깊이: 채널 당 비트 수. 지원하는 값은 1, 8, 16, 32입니다. 그러나 모든 색상 모드가 모든 깊이와 함께 작동하지는 않습니다.|
|2|파일의 [PSD 색상 모드](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes). 지원되는 값은: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotone = 8; Lab = 9.|
Aspose.PSD의 [PSD API 참조](https://reference.aspose.com/psd)를 확인할 수 있습니다.
