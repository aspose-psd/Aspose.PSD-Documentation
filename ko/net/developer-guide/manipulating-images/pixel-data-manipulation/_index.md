---
title: C#를 사용한 Aspose.PSD를 활용한 픽셀 데이터 조작
weight: 100
type: docs
description: Aspose.PSD를 사용하여 PSD C# API를 통해 원시 픽셀 데이터를 직접적이고 빠르게 업데이트하는 방법의 예시
keywords: [픽셀 편집, psd 편집, 레이어 편집, 원시 데이터 조작, psd 데이터 수정, psd api, C#, csharp, 코드 샘플]
url: ko/net/pixel-data-manipulation/
---

## 소개

Aspose.PSD는 C#에서 Adobe Photoshop 파일 (PSD)을 다룰 수 있는 강력한 라이브러리입니다. 이 문서에서는 Aspose.PSD를 사용하여 PSD 파일에서 픽셀 데이터를 어떻게 조작하는지 살펴볼 것입니다.

## 개요

제공된 코드는 PSD 파일을 생성하고, 새 레이어를 추가하고, 픽셀 데이터를 직접적으로 조작하고 수정된 이미지를 저장하는 방법을 보여줍니다.

### 픽셀 데이터 조작 단계

1. **필요한 모듈 가져오기**:
   필요한 모듈을 가져옵니다. Aspose.PSD 라이브러리에서 `PsdImage`와 `Layer` 클래스를 가져와야 합니다.

2. **입력 및 출력 파일 경로 정의**:
   입력 및 출력 파일 경로를 지정합니다.

3. **입력 파일을 스트림으로 열기**:
   `FileStream` 클래스를 사용하여 읽기 모드로 입력 파일을 스트림으로 엽니다. 스트림을 로드하여 `PsdImage` 객체를 만듭니다.

4. **새 PSD 이미지 생성**:
   `PsdImage` 생성자를 사용하여 새 PSD 이미지를 만들고 레이어의 너비와 높이를 인수로 제공합니다.

5. **PSD 이미지에 레이어 지정**:
   레이어를 PSD 이미지의 `Layers` 속성에 할당합니다.

6. **픽셀 데이터 조작**:
   `LoadArgb32Pixels` 메서드를 사용하여 레이어에서 ARGB32 픽셀을 로드합니다. 픽셀 배열의 길이를 기반으로 인덱스 범위를 정의하고 필요에 따라 픽셀 값을 수정합니다.

7. **수정된 픽셀 데이터 저장**:
   `SaveArgb32Pixels` 메서드를 사용하여 수정된 픽셀 데이터를 다시 레이어에 저장합니다.

8. **PSD 이미지 저장**:
   `Save` 메서드를 사용하여 PSD 이미지를 출력 파일에 저장합니다.

### 예시

다음은 Aspose.PSD를 사용하여 C#에서 픽셀 데이터를 조작하는 방법을 보여주는 코드 샘플입니다:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### 요약

Aspose.PSD for C#은 PSD 파일에서 픽셀 데이터를 조작할 수 있는 강력한 기능 세트를 제공합니다. 특정 조건에 따라 픽셀을 수정하거나 복잡한 패턴을 만들어야 하는 경우, Aspose.PSD를 사용하면 이러한 작업이 간단하고 효율적으로 수행됩니다.

더 자세한 정보와 예시는 [Aspose.PSD for C# 문서](https://docs.aspose.com/psd/net/)를 참조해주세요.
