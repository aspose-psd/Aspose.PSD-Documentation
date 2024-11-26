---
title: Aspose.PSD for .NET 23.4 - 릴리스 노트
type: docs
weight: 90
url: /ko/net/aspose-psd-for-net-23-4-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**분류**|
| :- | :- | :- |
|PSDNET-1409|Design RawColor class for the public API to use it in PSD API instead of obsolete Color struct|기능 향상|
|PSDNET-1332|本人调试员页面逊崇崇Use it in PSD API instead of obsolete Color structUse it in PSD API instead of obsolete Color struct|기능 추가|
|PSDNET-1448|텍스트를 Text Portions을 사용하여 편집할 때 올바른 결과를 저장하지 않음|버그|
|PSDNET-1449|ITextPortion에 의해 텍스트 레이어를 편집할 때 스타일 또는 단락의 시작과 끝이 잘못된 위치에 나타남|버그|
|PSDNET-1509|포토샵에서 편집 시 서식이 이동함|버그|


## **공용 API 변경사항**
# **추가된 API들:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor


# **삭제된 API들:**
- 없음


## **사용 예시:**

**PSDNET-1332. Probation에서 Gradient Map 조정 레이어를 주 Aspose.PSD 코드에 통합**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // 현재 값 확인
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);


    grdmResource.Reverse = true;
    // 두 번째 그라디언트 색 점용 빨간색
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // 변경된 값 확인
    AssertAreEqual(true, grdmResource.Reverse);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[3].Value);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "객체가 동일하지 않습니다.");
    }
}
{{< /highlight >}}

**PSDNET-1409. RawColor 클래스를 사용하여 PSD API에서 사용할 공용 API를 위한 디자인**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "객체가 동일하지 않습니다.");
    }
}

var color = new RawColor(PixelDataFormat.Rgba32Bpp);
var oldColor = Color.FromArgb(5, 1, 2, 3);

var argbValue = oldColor.ToArgb();
color.SetAsInt(argbValue);

AssertAreEqual("ARGB", color.GetColorModeName());
AssertAreEqual(32, color.GetBitDepth());
AssertAreEqual("A Alpha", color.Components[0].FullName);
AssertAreEqual(5, (int)color.Components[0].Value);
AssertAreEqual("R Red", color.Components[1].FullName);
AssertAreEqual(1, (int)color.Components[1].Value);
AssertAreEqual("G Green", color.Components[2].FullName);
AssertAreEqual(2, (int)color.Components[2].Value);
AssertAreEqual("B Blue", color.Components[3].FullName);
AssertAreEqual(3, (int)color.Components[3].Value);

AssertAreEqual(argbValue, color.GetAsInt());
{{< /highlight >}}

**PSDNET-1448. Text Portions를 사용하여 텍스트를 편집할 때 올바른 결과를 저장하지 않음**

{{< highlight csharp >}}
string sourceFile =  "originalv5.psd";
string psdExportPath =  "export.psd";

using (var imageTestEmail = (PsdImage)Image.Load(sourceFile))
{
    var layers = imageTestEmail.Layers;
    foreach (var layerItem in layers)
    {
        var isTextLayer = layerItem.GetType() == typeof(TextLayer) ? true : false;
        if (isTextLayer)
        {
            var layerTLToUpdateText = (TextLayer)layerItem;

            // lsak 텍스트 찾기
            if (layerTLToUpdateText.Text.Contains("lsak"))
            {
                var textDataTL = layerTLToUpdateText.TextData;

                if (textDataTL.Text.Contains("lsak") && textDataTL.Text.Contains("\r"))
                {
                    // 텍스트 교체
                    replaceLsakText(textDataTL);
                    // 스타일 텍스트
                    formatStyleText(textDataTL);
                }
            }
        }
    }

    imageTestEmail.Save(psdExportPath, new PsdOptions());
}

string[] texts = new string[]
{
        "Power play.",
        "//Πιο επεκτατικοί κόσμοι. Γρήγοροι χρόνοι φόρτωσης. Υψηλά ποσοστά καρέ και ευρύτερο φάσμα χρωμάτων. Ένας υπολογιστής με Windows ήταν πάντα η καλύτερη πλατφόρμα για παιχνίδια—και στα Windows 11, γίνεται ακόμα καλύτερος./"
};

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(psdExportPath))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 9500; i < bytes.Length; i++)
    {
        if ((char)bytes[i] == '\0')
        {
            txt2Data += "0";
        }
        else
        {
            txt2Data += (char)bytes[i];
        }
    }

    string key0 = @" >> /1 " + texts[0].Length + " >>";       // 첫 번째 텍스트 길이에 대한 접두사
    string key1 = @" >> /1 " + texts[1].Length + " >>";       // 두 번째 텍스트 길이에 대한 접두사

    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    if (index0 < 0)
    {
        throw new Exception("첫 번째 텍스트 스타일 길이를 찾을 수 없습니다. 길이가 " + texts[0].Length + "와 같아야 합니다.");
    }

    if (index1 < 0)
    {
        throw new Exception("두 번째 텍스트 스타일 길이를 찾을 수 없습니다. 길이가 " + texts[1].Length + "와 같아야 합니다."); ;
    }
}


void replaceLsakText(IText textData)
{
    var countPortions = textData.Items.Length;
    ITextStyle defaultStyle = textData.Items[0].Style;
    ITextParagraph defaultParagraph = textData.Items[0].Paragraph;

    var textToReplace = textData.Text;

    // 이전 부분 제거
    for (int i = 0; i < (countPortions); i++)

    {
        textData.RemovePortion(0);
    }

    ITextPortion newPortion = textData.ProducePortion();
    newPortion.Paragraph.Apply(defaultParagraph);
    newPortion.Style.Apply(defaultStyle);
    newPortion.Text = ReplaceText(textToReplace);
    textData.AddPortion(newPortion);
    textData.UpdateLayerData();
}

void formatStyleText(IText textData)
{
    // 태그가 있는지 확인
    Regex tagRegex = new Regex(@"<[^>]+>");
    bool hasTags = tagRegex.IsMatch(textData.Text);
    var countPortions = textData.Items.Length;
    ITextStyle defaultStyle = textData.Items[0].Style;
    ITextParagraph defaultParagraph = textData.Items[0].Paragraph;

    if (hasTags)
    {
        var tagRegex2 = @"[^<>]+|<\s*([^ >]+)[^>]*>.*?<\s*/\s*\1\s*>";
        var matchesImgSrc = Regex.Matches(textData.Text, tagRegex2, RegexOptions.IgnoreCase | RegexOptions.Singleline);
        var listlsaks = new List<string>();
        foreach (Match m in matchesImgSrc)
        {
            listlsaks.Add(m.Value);
        }
        string[] textSplit = listlsaks.ToArray();

        for (int i = 0; i < (countPortions); i++)
        {
            textData.RemovePortion(0);
        }

        for (int i = 0; i < textSplit.Length; i++)
        {
            ITextPortion newPortion = textData.ProducePortion();
            newPortion.Paragraph.Apply(defaultParagraph);
            newPortion.Style.Apply(defaultStyle);
            bool hasTagsIsaks = false;
            hasTagsIsaks = tagRegex.IsMatch(textSplit[i]);

            if (hasTagsIsaks)
            {
                if (textSplit[i].Contains("pt"))
                {
                    newPortion.Style.FontSize = 72;
                };

                newPortion.Text = Regex.Replace(textSplit[i], "<.*?>", String.Empty).Replace("br/", "//");
                textData.AddPortion(newPortion);
            }
            else
            {
                newPortion.Text = Regex.Replace(textSplit[i], "<.*?>", String.Empty).Replace("br/", "//");
                textData.AddPortion(newPortion);
            }
        }
    }
    else
    {
        var textToReplace = textData.Text;
        for (int i = 0; i < (countPortions); i++)
        {
            textData.RemovePortion(0);
        }

        ITextPortion newPortion = textData.ProducePortion();
        newPortion.Paragraph.Apply(defaultParagraph);
        newPortion.Style.Apply(defaultStyle);
        newPortion.Text = textToReplace.Replace("\r", "").Replace("br/", "//");
        textData.AddPortion(newPortion);
    }

    textData.UpdateLayerData();

}

string ReplaceText(string lsak)
{
    StringBuilder sb = new StringBuilder(lsak);
    sb.Replace("#lsak_007#", "Power play.");
    sb.Replace("#lsak_008#", "Πιο επεκτατικοί...");

    // 다른 내용 생략

    sb.Replace("\r", "");
    return sb.ToString();
}
{{< /highlight >}}

**PSDNET-1449. ITextPortion에 의해 텍스트 레이어를 편집할 때 스타일 또는 단락의 시작과 끝이 잘못된 위치에 나타남**

{{< highlight csharp >}}
string sourceFilePSDEmail = "inputv2.psd";
string outputFile = "export.psd";

using (PsdImage imageTestEmail = (PsdImage)Aspose.PSD.Image.Load(sourceFilePSDEmail))
{
    var layers = imageTestEmail.Layers;

    foreach (var layerItem in layers)
    {
        var layerTLToUpdateText = layerItem as TextLayer;

        if (layerTLToUpdateText == null)
        {
            continue;
        }

        // lsak 텍스트 찾기
        if (!layerTLToUpdateText.Text.Contains("lsak") ||
            !layerTLToUpdateText.TextData.Text.Contains("lsak"))
        {
            continue;
        }

        var textDataTL = layerTLToUpdateText.TextData;

        // 단계: 텍스트 교체
        ReplaceLsakFourthMethod(textDataTL);

        System.Console.WriteLine("교환된 텍스트