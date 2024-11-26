---
title: Adobe Illustrator 형식 조작
type: docs
weight: 50
url: /ko/java/manipulating-adobe-illustrator-formats/
---

## **AI 파일을 PSD로 내보내기**
Aspose.PSD for Java를 사용하면 개발자는 Adobe Illustrator 파일을 [PSD](https://wiki.fileformat.com/image/psd/) 형식으로 변환할 수 있습니다. 이 주제에서는 기존 Adobe Illustrator 파일을로드하고 **PsdOptions** 클래스를 사용하여 PSD로 변환하는 방법을 설명합니다.

Adobe Illustrator 파일을 PSD로 변환하는 단계는 다음과 같습니다:

- [AiImage](https://reference.aspose.com/java/psd/com.aspose.psd.fileformats.ai/AiImage) 클래스의 인스턴스를 만들고 Image 클래스의 Load 메서드를 사용하여 이미지를로드합니다.
- PsdOptions 클래스의 인스턴스를 만듭니다.
- [AiImage.Save](https://reference.aspose.com/java/psd/com.aspose.psd/Image#save--) 메서드를 목적지 경로와 PsdOptions의 인스턴스와 함께 호출합니다.

아래 제시된 샘플 코드는 Adobe Illustrator를 PSD로 내보내는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-AI-AIToPSD-AIToPSD.java" >}}

## **AI 파일을 JPEG로 내보내기**
Aspose.PSD for Java를 사용하면 개발자는 Adobe Illustrator 파일을 [JPEG](https://wiki.fileformat.com/image/jpeg/) 형식으로 변환할 수 있습니다. 이 주제에서는 기존 AI 파일을로드하고 **JpegOptions** 클래스를 사용하여 JPEG로 변환하는 방법을 설명합니다.

Adobe Illustrator 파일을 JPEG로 변환하는 단계는 다음과 같습니다:

- AiImage의 인스턴스를 만들고 Image 클래스의 Load 메서드를 사용하여 이미지를 로드합니다.
- JpegOptions 클래스의 인스턴스를 만듭니다.
- 이미지 품질을 설정합니다.
- [AiImage.save](https://reference.aspose.com/java/psd/com.aspose.psd.fileformats.ai/AiImage) 메서드를 목적지 경로와 JpegOptions의 인스턴스와 함께 호출합니다.

아래 제공된 샘플 코드는 AI를 JPEG로 내보내는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-AI-AIToJPG-AIToJPG.java" >}}

## **AI 파일을 GIF로 내보내기**
Aspose.PSD for Java는 Adobe Illustrator 파일을로드하는 **AiImage** 클래스를 제공하며 이를 사용하여 Adobe Illustrator 파일을 [GIF](https://wiki.fileformat.com/image/gif/) 형식으로 내보낼 수 있습니다. 이 예제는 Aspose.PSD for Java API를 사용하여 AI 파일을 GIF 이미지로 내보내는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-AI-AIToGIF-AIToGIF.java" >}}

## **AI 파일을 PNG로 내보내기**
Aspose.PSD for Java를 사용하면 개발자는 Adobe Illustrator 파일을 [PNG](https://wiki.fileformat.com/image/png/) 형식으로 변환할 수 있습니다. 이 주제에서는 기존 Adobe Illustrator 파일을로드하고 **PngOptions** 클래스를 사용하여 PNG로 변환하는 방법을 설명합니다.

AI 파일을 PNG로 변환하는 단계는 다음과 같습니다:

- [AiImage](https://reference.aspose.com/java/psd/com.aspose.psd.fileformats.ai/AiImage) 클래스의 인스턴스를 만들고 Image 클래스의 Load 메서드를 사용하여 이미지를 로드합니다.
- PngOptions 클래스의 인스턴스를 만듭니다.
- 색상 유형을 설정합니다.
- AiImage.save 메서드를 목적지 경로와 PngOptions의 인스턴스와 함께 호출합니다.

아래 제공된 샘플 코드는 Adobe Illustrator를 PNG로 변환하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-AI-AIToPNG-AIToPNG.java" >}}

## **AI 파일을 TIFF로 내보내기**
Aspose.PSD for Java는 Adobe Illustrator 파일을로드하는 **AiImage** 클래스를 제공하며 이를 사용하여 AI 파일을 [TIFF](https://wiki.fileformat.com/image/tiff) 형식으로 내보낼 수 있습니다. 이 예제는 Aspose.PSD for Java API를 사용하여 Adobe Illustrator 파일을 TIFF 이미지로 내보내는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-AI-AIToTIFF-AIToTIFF.java" >}}

## **AI 파일을 PDF로 내보내기**
Aspose.PSD for Java는 Adobe Illustrator 파일을로드하는 **AiImage** 클래스를 제공하며 이를 사용하여 AI 파일을 [PDF](https://docs.fileformat.com/pdf/) 형식으로 내보낼 수 있습니다. 이 예제는 Aspose.PSD for Java API를 사용하여 Adobe Illustrator 파일을 PDF 이미지로 내보내는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-AI-AIToPDF-AIToPDF.java" >}}

