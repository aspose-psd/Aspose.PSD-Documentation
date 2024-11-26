---
title: Aspose.PSD for Python via .NET 24.1 - 릴리스 노트
type: docs
weight: 10
url: /ko/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}
이 페이지에는 [Aspose.PSD for Python via .NET 24.1](https://pypi.org/project/aspose-psd/)에 대한 릴리스 노트가 포함되어 있습니다.
{{% /alert %}}

| **키**       | **요약**                                                                                                                           | **범주**     |
|:---------------|:-------------------------------------------------------------------------------------------------------------------------------------|:-------------|
|  PSDPYTHON-19 | [AI 형식] 다중 페이지 AI 이미지에 대한 기본 처리 추가                                                                           |   기능        |
|  PSDPYTHON-22 | 워프 텍스트 효과가 텍스트에 적용되지 않음                                                                                            |   버그        |
|  PSDPYTHON-23 | 특정 파일의 마스크를 잘못된 렌더링                                                                                                      |   버그        |
|  PSDPYTHON-24 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor에서 NullReferenceException 발생         |   버그        |
|  PSDPYTHON-25 | [AI 형식] AiExporterUtils에서 메모리 사용량 수정                                                                  |   버그        |


## **공개 API 변경 사항**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDPYTHON-19. [AI 형식] 다중 페이지 AI 이미지에 대한 기본 처리 추가**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # AI 이미지 로드
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # 기본적으로 ActivePageIndex는 0입니다.
            # 따라서이 속성을 변경하지 않고 AI 이미지를 저장하면 첫 번째 페이지가 렌더링되어 저장됩니다.
            image.save(firstPageOutputPng, PngOptions())

            # 활성 페이지 인덱스를 두 번째 페이지로 변경합니다.
            image.active_page_index = 1

            # AI 이미지의 두 번째 페이지를 PNG 이미지로 저장합니다.
            image.save(secondPageOutputPng, PngOptions())

            # 활성 페이지 인덱스를 세 번째 페이지로 변경합니다.
            image.active_page_index = 2

            # AI 이미지의 세 번째 페이지를 PNG 이미지로 저장합니다.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. 워프 텍스트 효과가 텍스트에 적용되지 않음**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. 특정 파일에서 마스크 렌더링이 잘못됨**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor에서 NullReferenceException 발생**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)

        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI 형식] AiExporterUtils에서 메모리 사용량 수정**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # C#의 메모리 사용량은 220이지만 파이썬의 경우 GC 활동에 직접 액세스할 수 없습니다.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # AI 이미지 로드
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # AI 이미지의 첫 번째 페이지를 PNG 이미지로 저장합니다.
            image.save(firstPageOutputPng, pngOpt)

            # 활성 페이지 인덱스를 두 번째 페이지로 변경합니다.
            image.active_page_index = 1

            # AI 이미지의 두 번째 페이지를 PNG 이미지로 저장합니다.
            image.save(secondPageOutputPng, pngOpt)

            # 활성 페이지 인덱스를 세 번째 페이지로 변경합니다.
            image.active_page_index = 2

            # AI 이미지의 세 번째 페이지를 PNG 이미지로 저장합니다.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("메모리 사용량이 너무 큽니다. {:.1f} 대신 {}입니다.".format(memoryUsed, MemoryLimit))
{{< /highlight >}}
