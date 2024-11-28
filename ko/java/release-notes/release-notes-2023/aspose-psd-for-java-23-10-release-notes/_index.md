---
title: Aspose.PSD for Java 23.10 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-23-10-release-notes/
---

{{% alert color="primary" %}}이 페이지에는 [Aspose.PSD for Java 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/)에 대한 릴리스 노트가 포함되어 있습니다.{{% /alert %}}

| **Key**        | **요약**                                                                             | **카테고리** |
|:---------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-538    | 수직 텍스트 방향 지원                                                     |    기능   |
| PSDJAVA-542    | Shape Stroke 렌더링에 vstk 리소스의 스트로크 설정 사용 |    기능   |
| PSDJAVA-540    | 스트로크 모양의 내부 영역 렌더링 구현                                   |    기능   |
| PSDJAVA-541    | 변경되지 않은 경우 Shape 레이어 다시 그리지 않음                 |    기능   |
| PSDJAVA-545    | [AI 형식] PDF 기반 AI 파일에서 헤더 읽기 지원              |    기능   |
| PSDJAVA-546    | Psd 파일 해상도를 설정하는 다양한 방법 작동하지 않음                    |      버그     |
| PSDJAVA-547    | FontSettings.SetFontsFolders 작동하지 않거나 Aspose.PSD가 잘못된 글꼴 사용   |      버그     |
| PSDJAVA-548    | 회귀. Shape 레이어가있을 때 PsdImage.Save에서 Null 참조 예외 수정        |      버그     |

## **Public API 변경내역**
# **추가된 API:**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
- ...
- ...

# **제거된 API:**

- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- ...
- ...

## **사용 예시:**

** PSDJAVA-538. 수직 텍스트 방향 지원**

{{< highlight java >}}
    
    코드 예시 내용

{{< /highlight >}}

** PSDJAVA-542. Shape Stroke 렌더링에 vstk 리소스의 스트로크 설정 사용**

{{< highlight java >}}
    
    코드 예시 내용

{{< /highlight >}}

...
...
...

** PSDJAVA-546. Psd 파일 해상도 설정하는 다양한 방법 작동하지 않음**

{{< highlight java >}}
    
    코드 예시 내용

{{< /highlight >}}

** PSDJAVA-547. FontSettings.SetFontsFolders 작동하지 않거나 Aspose.PSD가 잘못된 글꼴 사용**

{{< highlight java >}}
    
    코드 예시 내용

{{< /highlight >}}

** PSDJAVA-548. 회귀. Shape 레이어가있을 때 PsdImage.Save에서 Null 참조 예외 수정**

{{< highlight java >}}
    
    코드 예시 내용

{{< /highlight >}}