---
title: 이미지에 서명 추가하기
type: 문서
weight: 70
url: /ko/net/adding-a-signature-to-an-image/
---

## **서명 추가**

이미지에 서명을 추가하는 것은 때로 디지털로 이미지에 서명하여 위조를 방지해야 하는 경우가 있습니다. 다른 이유는 이미지를 갤러리에 표시되는 것처럼 다루는 것일 수 있습니다. 그 이유가 무엇이든, Aspose.PSD API는 아래에 설명된 간단한 메커니즘을 사용하여 이미지에 서명을 추가할 수 있는 기능을 제공합니다. 이 예제는 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스를 사용하여 기본 이미지의 표면에 서명이 있는 다른 이미지를 그리는 것을 보여줍니다. 작업을 설명하기 위해 디스크에서 PSD 이미지를 로드하고 Graphics 클래스의 [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) 메서드를 사용하여 기본 이미지의 표면에 서명이 있는 다른 이미지를 그립니다. 우리는 [PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions) 클래스를 사용하여 PNG 형식으로 결과 이미지를 저장할 것입니다. 아래는 이미지에 서명을 추가하는 방법을 보여주는 코드 예제입니다. 이 예제 소스 코드는 쉽게 따라갈 수 있도록 여러 부분으로 나뉘어져 있습니다. 단계별로, 예제는 다음 항목에 대해 보여줍니다:

- 기본 및 보조 (서명) 이미지 로드하기
- Graphic 객체 생성 및 초기화하기
- Graphics 클래스의 DrawImage 메서드를 사용해 이미지 그리기
- 결과를 PNG 형식으로 저장하기
### **프로그램 샘플**
#### **이미지 로드**
먼저 Image 클래스의 인스턴스를 만들어 디스크에서 샘플 이미지를 로드합니다.
#### **Graphic 객체 생성 및 초기화**
이미지를 로드한 후, 기본 이미지의 객체를 사용하여 Graphics 클래스 객체를 생성하고 초기화합니다.
#### **기본 이미지 위에 보조 이미지 그리기**
그런 다음 Graphics 클래스의 DrawImage 메서드를 사용하여 보조 이미지를 기본 이미지 위에 추가합니다. DrawImage 메서드에는 첫 번째 매개변수로 Image 객체를 사용하는 다양한 오버로드가 있으며, 나머지 모든 매개변수는 이미지를 그릴 위치에 해당합니다. 예제를 위해 아래 코드는 DrawImage의 오버로드 버전을 사용하고, 두 번째 매개변수로 Point 객체를 사용하여 기본 이미지의 오른쪽 하단 모서리에 서명을 그리려고 시도합니다.
#### **이미지 저장**
마지막으로 PngOptions 클래스를 사용하여 이미지를 PNG 파일로 로컬 디스크에 다시 저장합니다.
#### **전체 소스**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
