---
title: Aspose.PSD for .NET 24.7 - 릴리스 노트
type: docs
weight: 60
url: /ko/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

이 페이지는 [Aspose.PSD for .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트를 포함합니다.

{{% /alert %}}

| **키**     | **요약**                                                                                      | **카테고리** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | AI 문서를 열 때 "이미지 로딩 실패." 예외 발생                                            | 버그      |
| PSDNET-2022 | 텍스트가 출력 PDF 파일에 부정확하게 렌더링됨                                                  | 버그      |
| PSDNET-2061 | 리눅스에서 주어진 파일에 대해 이미지 내보내기 실패를 해결하는 ImageSaveException 수정       | 버그      |
| PSDNET-2080 | Aspose.Drawing을 사용할 때 폰트 로딩 수정                                                      | 버그      |
| PSDNET-2085 | 큰 JPEG 사용 시 스마트 개체 레이어 생성 시 '산술 연산이 오버플로우로 나타남' 수정              | 버그      |
| PSDNET-2100 | AI 파일을 JPG 파일로 변환할 수 없음                                                           | 버그      |

## **공개 API 변경**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

## **사용 예제:**

**PSDNET-1029. AI 문서 열 때 "이미지 로딩 실패." 예외 발생**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. 텍스트가 출력 PDF 파일에 부정확하게 렌더링됨**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. 리눅스에서 주어진 파일에 대해 이미지 내보내기 실패를 해결하는 ImageSaveException 수정**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Aspose.Drawing을 사용할 때 폰트 로딩 수정**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- 업데이트 전. 설치된 폰트 수: " + installedFonts.Families.Length);
    Console.WriteLine("- 플랫폼: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- 'Arial'에 대한 Adobe 폰트 이름을 가져와서 폰트 캐시 새로 고침: "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- 업데이트 후. 설치된 폰트 수: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 큰 JPEG를 사용하여 스마트 개체 레이어를 생성할 때 '산술 연산이 오버플로우로 나타남'**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. AI 파일을 JPG 파일로 변환할 수 없음**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
