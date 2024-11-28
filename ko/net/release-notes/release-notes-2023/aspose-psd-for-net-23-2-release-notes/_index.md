---
title: Aspose.PSD for .NET 23.2 - 릴리스 노트
type: docs
weight: 110
url: /ko/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**범주**|
| :- | :- | :- |
|PSDNET-1359|텍스트 렌더링 재작업을 통한 텍스트 위치, 렌더링 및 지원 향상|개선|
|PSDNET-1270|Public API를 통해 와프 효과 처리 기능 추가|기능|
|PSDNET-1391|문단 설정에서 하단-하단 및 상단-상단 선탑지원 추가|기능|
|PSDNET-912|TextLayer PSD의 글꼴 및 색상 변경|버그|
|PSDNET-1022|테스트 TextUpdateTests의 텍스트를 잘못 내보내어 텍스트가 누락됨|버그|
|PSDNET-1221|더 큰 PSD 이미지의 크기 조정 후 추가 작은 텍스트 누락|버그|
|PSDNET-1301|Aspose.Psd for .NET의 textLayer.UpdateText()는 서로 다른 데이터 세트에 대해 무작위로 대시(-)를 밑줄로 인쇄|버그|
|PSDNET-1379|ResolutionSettings은 PSD에서 PDF로 내보낼 때 적용되지 않음|버그|


## **Public API 변경**
# **추가된 API:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **제거된 API:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **사용 예시:**

**PSDNET-912. TextLayer PSD의 글꼴 및 색상 변경**

{{< highlight csharp >}}
string fontsFolder = "Fonts";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "result.psd";
string outputPng = "result.png";

FontSettings.SetFontsFolder(fontsFolder);

using (var image = (PsdImage)Image.Load(srcFile))
{
    TextLayer nameLayer = (TextLayer)image.Layers[9];
    var textPortion = nameLayer.TextData.Items[0];

    textPortion.Text = "MODESTO SR";
    textPortion.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textPortion.Style.FillColor = Color.Red;

    nameLayer.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. 테스트 TextUpdateTests의 텍스트를 잘못 내보내어 텍스트가 누락됨**

{{< highlight csharp >}}
string srcFile = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample.psd";
string outputPng = "TextUpdateComplexKerningExample.png";

using (var image = (PsdImage)Image.Load(srcFile))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var layer = image.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("텍스트가 업데이트되었습니다");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. 더 큰 PSD 이미지의 크기 조정 후 추가 작은 텍스트 누락**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Public API를 통해 와프 효과 처리 기능 추가**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string pngWarpedExport = "warped.png";
string psdWarpedExport = "warpFile.psd";

var warpLoadOptions = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(sourceFile, warpLoadOptions))
{
    image.Save(pngWarpedExport, new PngOptions());
    image.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd for .NET textLayer.UpdateText()는 서로 다른 데이터 세트에 대해 무작위로 대시(-)를 밑줄로 인쇄**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "NAME":
                    textLayer.UpdateText("MR. JACK SMITH");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNATION":
                    textLayer.UpdateText("OFFICER-001");
                    break;
                case "BLOODGROUP":
                    textLayer.UpdateText("AB-");
                    break;
                case "ADDRESS":
                    textLayer.UpdateText("BLOCK-A, STREET-7, APPT NO - 047, SECTOR-024");
                    break;
                case "PERMADDRESS":
                    textLayer.UpdateText("HOUSE NO - 42, LANE -025, PALM GREENS VIEW HOUSING SOCIETY, SECTOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. ResolutionSettings은 PSD에서 PDF로 내보낼 때 적용되지 않음**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var image = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting resolutionSetting = new ResolutionSetting(300, 300);

    image.Save(output, new PdfOptions()
    {
        ResolutionSettings = resolutionSetting
    });
}
{{< /highlight >}}

**PSDNET-1391. 문단 설정에서 하단-하단 및 상단-상단 선탑지원 추가**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var textPortion in text1.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.TopToTop; // LeadingType 값 변경   
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var textPortion in text2.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.BottomToBottom; // LeadingType 값 변경   
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}
