---
title: Aspose.PSD for .NET 23.8 - 릴리스 노트
type: docs
weight: 50
url: /ko/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**     | **요약**                                                                                                  | **카테고리** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | 새로운 유형의 와프 (Flag) 추가 | 기능 |
| PSDNET-1621 | 새로운 유형의 와프 추가: 위쪽 아치, 아래쪽 아치, 구형 | 기능 |
| PSDNET-1682 | 새로운 메서드 PsdImage.AddPosterizeAdjustmentLayer를 구현하여 새로운 Posterize 레이어 추가| 기능 |
| PSDNET-913  | PSD 정보가 열고 저장하는 것만으로 손실됨 | 버그     |
| PSDNET-1352 | 이미지 로딩 실패 | 버그     |
| PSDNET-1553 | 이미지 로딩 실패: 알 수 없는 유형의 객체를 DescriptoStructure 유형으로 캐스팅할 수 없음 | 버그     |
| PSDNET-1631 | 제 3자 라이브러리에서 파일 변경이 PSD 파일을 손상시키지만 Photoshop에서 열 수 있음 | 버그     |


## **공개 API 변경 사항**
# **추가된 API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **제거된 API:**
- 없음


## **사용 예시:**

**PSDNET-913. PSD 정보가 열고 저장하는 것만으로 손실됨**

{{< highlight csharp >}}
string src = "원본 파일.psd";
string outputPsd = "out_원본 파일.psd";
string outputPng = "out_원본 파일.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. 이미지 로딩 실패**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. 이미지 로딩 실패: 알 수 없는 유형의 객체를 DescriptorStructure 유형으로 캐스팅할 수 없음**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Should load correctly
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. 제 3자 라이브러리에서 파일 변경이 PSD 파일을 손상시키지만 Photoshop에서 열 수 있음**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. 새로운 유형의 와프 (Flag) 추가**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. 새로운 유형의 와프 추가: 위쪽 아치, 아래쪽 아치, 구형**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ArcUpper_export.png";
string outputFileArcLower = "ArcLower_export.png";
string outputFileBulge = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. 새로운 메서드 PsdImage.AddPosterizeAdjustmentLayer를 구현하여 새로운 Posterize 레이어 추가**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// 저장된 변경 사항 확인
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "객체가 동일하지 않습니다.");
    }
}
{{< /highlight >}}
