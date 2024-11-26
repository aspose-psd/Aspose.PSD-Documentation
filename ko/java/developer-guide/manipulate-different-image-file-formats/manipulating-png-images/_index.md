---
title: PNG 이미지 조작
type: docs
weight: 30
url: /ko/java/manipulating-png-images/
---

## **PNG 이미지의 투명도 지정**
PNG 형식으로 이미지를 저장하는 장점 중 하나는 PNG가 투명 배경을 가질 수 있다는 것입니다. Aspose.PSD for Java는 아래 섹션에서 설명하는 대로 PngImage 및 RasterImage 클래스의 투명도 지정 기능을 제공합니다. Aspose.PSD for Java API를 사용하여 새 PNG 이미지를 생성하거나 기존 이미지를 PNG 형식으로 변환하면서 특정 색상을 투명하게 설정할 수 있습니다. 이를 위해 Aspose.PSD for Java API는 투명색상 속성 및 PngColorType 열거형을 노출시켜 PNG 이미지에서 투명하게 렌더링할 색상을 지정할 수 있습니다. 아래 제공된 코드 스니펫은 기존 PSD 이미지를 PngImage 오버로드된 생성자를 사용하여 PNG 이미지로 변환하고 원하는 색상을 투명하게 지정하는 방법을 보여줍니다.

## **PNG 이미지의 해상도 설정**
Aspose.PSD for Java는 PNG를 포함한 모든 이미지 형식에 대해 해상도를 설정할 수 있는 ResolutionSetting 클래스를 노출합니다. 이 문서는 Aspose.PSD for Java API의 사용법을 보여주며 PNG 이미지 형식의 가로 및 세로 해상도 매개변수를 설정합니다. 아래 코드 스니펫은 기존 PSD 이미지를 로드하고 PNG 형식으로 변환하면서 해상도를 변경하는 방법을 보여줍니다.

## **PNG 파일 압축**
Portable Network Graphic (PNG)은 비트맵을 네트워크 상에서 전송하기 위한 무손실 압축 형식입니다. 어떤 프로그램에서 이미지를 PNG 파일로 저장할 때 최대 수준까지 범위 내에서 압축 수준을 선택하라는 요청을 받을 수 있습니다. 이 값 설정은 실제로 파일 크기를 압축하고 이미지 품질을 감소시키지 않습니다. 이 문서는 Aspose.PSD API가 PNG 파일 크기를 제어할 수 있도록 하는 방법에 대해 설명합니다. Aspose.PSD API를 사용하여 PngOptions 클래스를 통해 PNG 파일 형식의 압축 수준을 설정할 수 있습니다. 이 속성은 0부터 9까지의 값인 CompressionLevel 속성을 가지고 있습니다. 이 속성은 0부터 9까지의 값 중 9가 최대 압축을 나타냅니다. 아래 제공된 코드 스니펫은 Aspose.PSD for Java API를 사용하여 압축 수준을 설정하는 방법을 보여줍니다.

## **PNG 이미지의 비트 깊이 지정**
이미징에서의 비트 깊이는 비트맵 이미지의 단일 픽셀의 색상을 나타내는 데 사용된 비트 수입니다. 다른 모든 비트맵 형식과 마찬가지로, PNG 색 깊이도 비트로 표시됩니다. 예를 들어 1비트 (2색), 2비트 (4색), 4비트 (16색) 및 8비트 (256색)와 같이 말이죠. Aspose.PSD for Java API는 PngOptions 클래스에서 노출된 BitDepth 속성을 사용하여 PNG 이미지의 비트 깊이를 설정할 수 있습니다. 현재 BitDepth 속성은 회색조 및 인덱스된 색상 유형에 대해 1, 2, 4 또는 8비트로 설정할 수 있습니다. 다른 모든 색상 유형에 대해서는 8비트만 지원됩니다. 아래 제공된 코드 스니펫은 PNG 이미지의 비트 깊이를 설정하는 방법을 보여줍니다.

## **PNG 이미지에 필터 방법 적용**
Aspose.PSD for Java는 PNG 이미지의 필터 타입을 설정하는 데 사용할 수 있는 PngFilterType 열거형을 노출합니다. 아래 제공된 코드 스니펫은 PngFilterType를 사용하여 기존 PSD 파일에 필터를 적용하여 PNG 이미지로 변환하는 방법을 보여줍니다.

## **투명한 PNG 이미지의 배경색 변경**
PNG 형식 이미지는 투명 배경을 갖을 수 있습니다. Aspose.PSD for Java는 투명 배경을 갖는 PNG 이미지의 배경색을 변경할 수 있는 기능을 제공합니다. Aspose.PSD for Java API를 사용하여 투명 PNG 이미지의 배경색을 설정/변경할 수 있습니다. 아래 제공된 코드 스니펫은 투명한 PNG 이미지의 배경색을 설정/변경하는 방법을 보여줍니다.
