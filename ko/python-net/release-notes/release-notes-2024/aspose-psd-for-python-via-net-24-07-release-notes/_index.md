---
title: Aspose.PSD Python via .NET 24.7 - 릴리스 노트
type: docs
weight: 10
url: /ko/python-net/aspose-psd-python을-통한-net-24-7-릴리스-노트/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD Python via .NET 24.7](https://pypi.org/project/aspose-psd/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**      | **요약**                                                                                                       | **카테고리** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | AI 문서를 열 때 "이미지 로딩 실패." 예외 발생                                         | 버그       |
| PSDPYTHON-87 | 텍스트가 출력 PDF 파일에서 부정확하게 렌더링됨                                               | 버그       |
| PSDPYTHON-88 | 리눅스에서 주어진 파일에 대한 이미지 내보내기 실패 수정                      | 버그       |
| PSDPYTHON-89 | Aspose.Drawing을 사용할 때 글꼴 로딩 수정                                             | 버그       |
| PSDPYTHON-90 | 대형 JPEG 사용 시 스마트 오브젝트 레이어 생성 시 '산술 연산 오버플로우 발생' | 버그       |
| PSDPYTHON-91 | AI 파일을 JPG 파일로 변환할 수 없음                                                    | 버그       |

## **공개 API 변경 사항**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDPYTHON-86. AI 문서를 열 때 "이미지 로딩 실패." 예외 발생**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. 텍스트가 출력 PDF 파일에서 부정확하게 렌더링됨**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. 리눅스에서 주어진 파일에 대한 이미지 내보내기 실패 수정**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Aspose.Drawing을 사용할 때 글꼴 로딩 수정**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- 업데이트 전. 설치된 글꼴 수: " + str(len(installedFonts.families)))
            print("- 'Arial'의 Adobe 글꼴 이름을 가져와서 글꼴 캐시를 새로고침: ")
            FontSettings.get_adobe_font_name("Arial")
            print("- 업데이트 후. 설치된 글꼴 수: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 대형 JPEG 사용 시 스마트 오브젝트 레이어 생성 시 '산술 연산 오버플로우 발생'**
{{< highlight python >}}
        # 수정은 되었지만, 해당 테스트를 제한하는 Aspose.PSD for Python의 다른 문제가 있음
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "테스트 레이어"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. AI 파일을 JPG 파일로 변환할 수 없음**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}
