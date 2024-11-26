---
title: 대형 이미지 지원
type: docs
weight: 40
url: /ko/net/large-image-support/
---

## **대형 이미지 지원**
표준 .NET 라이브러리는 이미지 크기에 제한이 있기 때문에 대형 이미지 지원을 위한 새로운 메커니즘을 도입했습니다. 새로운 접근법은 제한 사항을 극복하지만 데이터 크기 제한으로 인해 생성 및 로드 지원되는 최대 차원은 2,147,483,647 x 2,147,483,647 픽셀입니다.
### **대형 이미지 작업**
Aspose.PSD는 대형 이미지의 성능과 지원을 개선했습니다. 수백 메가바이트 크기의 이미지라도 문제가 되지 않으므로 해당 이미지 위에 생성, 로드 및 그리기 작업을 수행할 수 있습니다. 그러나 메모리 예외 처리의 일부 처리 및 처리로 인해 매우 대형 이미지에서 성능이 매우 떨어질 수 있습니다. Aspose.PSD가 처리를 위해 더 작은 양의 데이터를 재할당하고 각 재할당 단계가 매우 비용이 많이 들기 때문입니다. 새 아키텍처의 이점은 다음과 같습니다:

- 이미지 크기에 제한이 없습니다.
- PC에서 사용 가능한 메모리에 제한이 없습니다.

처리 속도가 느린 경우 모든 픽셀을 메모리에 맞출 수 있도록 총 RAM 양을 늘리는 것이 좋습니다. 그렇지 않을 경우 처리는 여전히 가능하지만 느립니다. 접근 방법은 다음과 같습니다:

- 원하는 사각형과 로드된 픽셀을 받을 대리자와 함께 [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) 메서드를 호출합니다.

Aspose.PSD는 전체 사각형을 로드하려고 합니다.

- 모든 픽셀을 수용할 메모리가 있으면 모든 픽셀이 간단히 호출자에게 반환됩니다.
- 메모리가 충분하지 않으면 호출자는 지정된 사각형 내부에서 픽셀 서브셋을 수신합니다. 해당 픽셀이 처리된 후 호출자는 다음 사각형을 받습니다. 전체 사각형이 처리될 때까지 처리가 종료됩니다.

Aspose.PSD는 가능한 한 많은 줄을 추출하려고 노력합니다. 한 줄의 픽셀을 수용할 메모리가 충분하지 않은 경우 한 줄이 1 높이를 갖는 사각형에 따라 분할됩니다. 대형 이미지에 그릴 수도 있습니다. 그림 작업은 전체 원하는 사각형에 영향을 주려고 노력합니다. 메모리가 충분하지 않으면 그리기가 전체 영역이 그려질 때까지 부분적인 사각형에서 수행됩니다. 게다가 Aspose.PSD는 대형 이미지 저장 및 내보내기를 지원합니다. 원본 이미지를 디스크에 저장하거나 다른 파일 형식으로 내보냅니다. 저장 또는 내보내기 프로세스는 필요에 따라 부분 사각형을 사용하여 수행됩니다.
### **지원되는 이미지 형식**
다음 형식은 대형 이미지 처리를 지원합니다:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

위의 형식은 이미지 크기와 관계없이 생성, 수정, 그리기 작업 적용, 디스크에 저장하거나 내보내기할 수 있습니다.

