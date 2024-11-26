---
title: PSD 파일 만들기, 열기 및 저장
type: docs
weight: 10
url: /ko/java/creating-opening-and-saving-psd-files/
---

## **이미지를 PSD로 내보내기**
PSD, 포토샵 문서,은 Adobe 포토샵이 이미지 작업에 사용하는 기본 파일 형식입니다. Aspose.PSD를 사용하면 PSD 파일을 로드, 편집하고 저장하여 포토샵에서 열고 편집할 수 있습니다. 본 문서에서는 Aspose.PSD로 파일을 PSD 형식으로 저장하는 방법과 이 형식으로 저장할 때 사용할 수 있는 일부 설정에 대해 설명합니다. PsdOptions는 ImageOptions 네임스페이스 내에서 이미지를 PSD로 내보내는 데 사용되는 특수한 클래스입니다. PSD로 내보내려면 Image 클래스의 인스턴스를 만들어야 합니다. 이는 기존 이미지 파일로부터로드된 인스턴스(예: 썸네일)이나 처음부터 작성된 인스턴스일 수 있습니다. 이 문서에서는 이러한 과정을 설명합니다. 아래 예에서는 처음부터 이미지를 작성합니다. 이미지가 생성되고 픽셀 데이터가 채워지면 Image 클래스 Save 메서드를 사용하여 이미지를 저장하고 두 번째 인수로 PsdOptions 객체를 제공하세요. PsdOptions 클래스의 여러 속성은 고급 변환을 위해 설정할 수 있습니다. 일부 속성은 ColorMode, CompressionMethod 및 Version 등입니다. Aspose.PSD는 CompressionMethod 열거형을 통해 다음 압축 방법을 지원합니다:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

다음 색상 모드는 ColorModes 열거형을 통해 지원됩니다:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



PSD v4.0, v5.0 및 더 높은 버전의 썸네일 리소스와 같은 추가 리소스를 추가할 수 있습니다. 또는 PSD v4.0 이상의 그리드 및 가이드 리소스를 추가할 수 있습니다. 아래 코드는 처음부터 BMP 파일을 작성하고 픽셀을 채우며 RLE 압축 및 회색조 색상 모드로 PSD로 저장하는 예시입니다. 다음 코드 스니펫은 이미지를 PSD로 내보내는 방법을 보여줍니다.


## **PSD 레이어로 이미지 가져오기**
본 문서에서는 Aspose.PSD를 사용하여 이미지를 PSD 레이어에 추가하거나 가져오는 방법을 설명합니다. Aspose.PSD API는 이러한 목표를 달성하는 효율적이고 사용하기 쉬운 방법을 노출시켰습니다. Aspose.PSD는 PSD 파일에 이미지를 추가/가져오기하기 위해 Layer 클래스의 DrawImage 메서드를 노출했습니다. DrawImage 메서드는 이미지를 PSD 파일에 추가/가져오기하기 위해 위치 및 이미지 값을 필요로 합니다. PSD 레이어에 이미지를 가져오기 위한 단계는 다음과 같습니다:

- Image 클래스에 의해 제공된 factory 메서드 Load를 사용하여 이미지로 PSD 파일을로드합니다.
- Layer 클래스의 인스턴스를 만들고 PSD 이미지 레이어를 할당합니다.
- 추가해야 할 이미지를로드하거나 처음부터 만듭니다.
- Layer.DrawImage 메서드를 호출하고 위치 및 이미지 인스턴스를 지정합니다.
- 결과를 저장합니다.

다음 코드 스니펫은 PSD 레이어로 이미지를 가져오는 방법을 보여줍니다.

## **PSD 파일에서 썸네일 생성**
PSD는 Adobe의 포토샵 응용 프로그램의 네이티브 문서 형식입니다. Adobe 포토샵(버전 5.0 이상)은 RGB(빨강, 녹색, 파랑) 순서의 JFIF 썸네일을 포함하는 이미지 리소스 블록에 미리보기 표시용 썸네일 정보를 저장합니다. Aspose.PSD API는 PSD 파일의 리소스에 액세스할 수 있는 쉬운 메커니즘을 제공합니다. 이러한 리소스에는 응용프로그램 요구에 따라 가져와 디스크에 저장할 수있는 썸네일 리소스가 포함됩니다. 다음 코드 스니펫은 PSD 파일에서 썸네일을 생성하는 방법을 보여줍니다.

## **색인화된 PSD 파일 생성**
Aspose.PSD for Java API를 사용하면 처음부터 색인화된 PSD 파일을 만들 수 있습니다. 이 문서는 PsdOptions 및 PsdImage 클래스를 사용하여 Canvas를 생성하면서 색인화된 PSD를 만드는 방법을 설명합니다. 색인화된 PSD 파일을 만들기 위해 다음 단계가 필요합니다.

- PsdOptions의 인스턴스를 만들고 소스를 설정합니다.
- PsdOptions의 ColorMode 속성을 ColorModes.Indexed로 설정합니다.
- RGB 공간에서 일련의 색상을 만든 다음 PsdOptions의 Palette 속성으로 설정합니다.
- 필요한 압축 알고리즘으로 CompressionMethod 속성을 설정합니다.
- PsdImage.Create 메서드를 호출하여 새 PSD 이미지를 만듭니다.
- 그래픽을 그리거나 다른 작업을 수행합니다.
- 모든 변경 사항을 커밋하기 위해 PsdImage.Save 메서드를 호출합니다.


다음 코드 스니펫은 색인화된 PSD 파일을 생성하는 방법을 보여줍니다.

## **PSD 레이어를 래스터 이미지로 내보내기**
Java용 Aspose.PSD를 사용하면 PSD 파일의 레이어를 래스터 이미지로 내보낼 수 있습니다. PSD 파일을로드하고 각 레이어를 Aspose.PSD.FileFormats.Psd.Layers.Layer.Save를 사용하여 PNG 이미지로 내보내는 샘플 코드입니다. 모든 레이어를 PNG 이미지로 내보낸 후 원하는 이미지 뷰어에서 열 수 있습니다. 아래 코드 스니펫은 PSD 레이어를 래스터 이미지로 내보내는 방법을 보여줍니다.
