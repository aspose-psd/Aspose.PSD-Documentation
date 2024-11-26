---
title: Aspose.PSD cho .NET 23.3 - Ghi chú Phát hành
type: docs
weight: 100
url: /vi/net/aspose-psd-cho-net-23-3-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-146|Hỗ trợ Lớp Điều chỉnh Posterize|Tính năng|
|PSDNET-1366|Thực hiện hỗ trợ của VscgResource|Tính năng|
|PSDNET-1437|Thêm hỗ trợ tài nguyên PostResource cho dữ liệu của Lớp Điều chỉnh Posterize|Tính năng|
|PSDNET-931|Xuất sai lớp PNG với điều chỉnh đường cong và chế độ màu CMYK|Lỗi|
|PSDNET-1403|Kiểu Đoạn đã bị mất sau khi lưu tệp và cập nhật tệp bằng PS|Lỗi|
|PSDNET-1453|Hiệu ứng glow và shadow trên văn bản không hoạt động|Lỗi|


## **Thay đổi trong API Công cộng**
# **API Đã Thêm:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey

# **API Đã Xóa:**
- Không có


## **Ví dụ về cách sử dụng:**

**PSDNET-146. Hỗ trợ Lớp Điều chỉnh Posterize**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    foreach (Layer layer in image.Layers)
    {
        if (layer is PosterizeLayer)
        {
            ((PosterizeLayer)layer).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Xuất sai lớp PNG với điều chỉnh đường cong và chế độ màu CMYK**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // thêm ', new PsdOptions()' gây ra lỗi.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Thực hiện hỗ trợ của VscgResource**

{{< highlight csharp >}}
string sourceFile = "StrokeInternalFill_src.psd";
string outputFile = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"Giá trị không bằng nhau.\nDự kiến:{expected}\nKết quả:{current}\nSai lệch:{expected - current}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // Đỏ
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // Xanh lá cây
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // Xanh dương

    image.Save(outputFile);
}

// kiểm tra các thay đổi
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Kiểu Đoạn đã bị mất sau khi lưu tệp và cập nhật tệp bằng PS**

{{< highlight csharp >}}
string sourceFile = "PSDTest3.psd";
string outputFile = "output.psd";

string[] newText = new string[]
{
    "Tile \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer layer2 = image.AddTextLayer("Lớp mới", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var textDataTL = layer2.TextData;

    ITextStyle defaultStyleTL = textDataTL.ProducePortion().Style;

    ITextParagraph defaultParagraphTL = textDataTL.ProducePortion().Paragraph;
    ITextPortion[] newPortionsTL = textDataTL.ProducePortions(newText, defaultStyleTL, defaultParagraphTL);

    newPortionsTL[0].Style.FontSize = 14;
    newPortionsTL[0].Style.FontName = "TwCenMT-Bold";

    newPortionsTL[1].Style.Leading = 20;
    newPortionsTL[1].Style.FontSize = 10;
    newPortionsTL[1].Style.FontName = "TwCenMT-Bold";

    // Xóa văn bản cũ
    textDataTL.RemovePortion(0);

    // Thêm các phần văn bản mới
    foreach (var newPortion in newPortionsTL)
    {
        textDataTL.AddPortion(newPortion);
    }

    textDataTL.UpdateLayerData();

    image.Save(outputFile);
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(outputFile))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Data += (char)bytes[i];
    }

    string key0 = @" >> /6 0 >> >> /1 "; // tiền tố độ dài của đoạn 0
    string key1 = @" >> /6 1 >> >> /1 "; // tiền tố độ dài của đoạn 1
    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    string lenPar0 = txt2Data.Substring(index0 + key0.Length, 1);
    string lenPar1 = txt2Data.Substring(index1 + key1.Length, 3);

    string expected0 = newText[0].Length.ToString();
    string expected1 = (newText[1].Length + 1).ToString();

    if (lenPar0 != expected0 || lenPar1 != expected1)
    {
        throw new Exception(
            $"Độ dài của đoạn văn bản là không chính xác.\nDự kiến: {expected0} và {expected1}\nKết quả: {lenPar0} và {lenPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Thêm hỗ trợ tài nguyên PostResource cho dữ liệu của Lớp Điều chỉnh Posterize**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];

    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is PostResource)
        {
            ((PostResource)resource).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Hiệu ứng glow và shadow trên văn bản không hoạt động**

{{< highlight csharp >}}
string outputPsd = "effect_bug.psd";
string outputPng = "effect_bug.png";

using (var psdImage = new PsdImage(500, 500))
{
    // Thêm lớp văn bản
    Aspose.PSD.Rectangle textArea1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle textArea2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle textArea3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer textLayer1 = psdImage.AddTextLayer("Văn bản với Hiệu ứng", textArea1);
    TextLayer textLayer2 = psdImage.AddTextLayer("Văn bản với Hiệu ứng", textArea2);
    TextLayer textLayer3 = psdImage.AddTextLayer("Văn bản với Hiệu ứng", textArea3);

    // Sửa đổi lớp văn bản
    textLayer1.TextData.Items[0].Style.FontSize = 150;
    textLayer1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer1.TextData.UpdateLayerData();

    textLayer2.TextData.Items[0].Style.FontSize = 150;
    textLayer2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer2.TextData.UpdateLayerData();

    textLayer3.TextData.Items[0].Style.FontSize = 150;
    textLayer3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer3.TextData.UpdateLayerData();

    // Thêm hiệu ứng
    OuterGlowEffect glow = textLayer1.BlendingOptions.AddOuterGlow(); // sự cố
    glow.Spread = 15;
    ((ColorFillSettings)glow.FillColor).Color = Color.Red;

    var shadow = textLayer2.BlendingOptions.AddDropShadow(); // sự cố với văn bản dài
    shadow.Distance = 25;
    shadow.Color = Color.DarkBlue;

    var innerShadow = textLayer3.BlendingOptions.AddInnerShadow(); // sự cố với văn bản dài
    innerShadow.UseGlobalLight = false;
    innerShadow.Angle = -179;
    innerShadow.Distance = 10;
    innerShadow.Size = 8;
    innerShadow.Color = Color.HotPink;

    // xuất
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}