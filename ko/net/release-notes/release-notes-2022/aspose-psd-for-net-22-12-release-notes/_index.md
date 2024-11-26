---
title: Aspose.PSD for .NET 22.12 - 릴리스 노트
type: docs
weight: 10
url: /ko/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

{{% alert color="success" %}}

- 이 릴리스에서는 16비트 내보내기와 관련된 회귀가 수정되었습니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-1336|IText 인터페이스에 편집 가능한 TextOrientation 속성 추가|기능|
|PSDNET-725|레이어 마스크가 있는 특정 PSD 파일 크기 조정시 잘못된 마스크 생성|버그|
|PSDNET-1277|16 이미지에 대한 마스크를 저장하고 로드할 수 있는 기능 추가|버그|
|PSDNET-1281|16비트 이미지를 16 또는 8비트 이미지로 저장할 때 투명도 오류 수정|버그|
|PSDNET-1375|16비트 색상에서 CMYK 수정|버그|


## **공용 API 변경**
# **추가된 API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **삭제된 API:**
- 없음


## **사용 예시:**

**PSDNET-725. 레이어 마스크가 있는 특정 PSD 파일 크기 조정시 잘못된 마스크 생성**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// 출처 PSD 파일을 엽니다
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // 크기 조정 수행
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// 크기 조정된 PSD 파일을 엽니다
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // PNG로 렌더링
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. 16 이미지에 대한 마스크를 저장하고 로드할 수 있는 기능 추가**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // 16비트 색상으로 저장할 수 있는 옵션
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // PSD 파일은 투명도로 저장됩니다
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. 16비트 이미지를 16 또는 8비트 이미지로 저장할 때 투명도 오류 수정**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// 16비트 색상 PSD 파일 (투명도 포함)을 열고 16비트 색상으로 저장
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// 16비트 색상 PSD 파일로 저장된 이미지를 PNG 파일로 렌더링 (투명도 포함)
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. IText 인터페이스에 편집 가능한 TextOrientation 속성 추가**

{{< highlight csharp >}}
// 다음 코드는 새 TextOrientation 속성을 편집하는 능력을 보여줍니다.
// 현재 렌더링에는 영향을 미치지 않고 속성 값을 편집할 수 있습니다.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // 올바른 읽기
    }
    else
    {
        throw new Exception("잘못된 TextOrientation 속성 값 읽기");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // 올바른 읽기
    }
    else
    {
        throw new Exception("잘못된 TextOrientation 속성 값 읽기");
    }
}
{{< /highlight >}}

**PSDNET-1375. 16비트 색상에서 CMYK 수정**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// 변환 옵션 설정
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// 변환 및 저장
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// 변환된 파일을 열고 PNG로 렌더링
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
