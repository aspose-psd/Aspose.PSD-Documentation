---
title: Aspose.PSD for .NET 23.8 - リリースノート
type: docs
weight: 50
url: /ja/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**     | **概要**                                                                                                  | **カテゴリ** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | 新しい形式の歪み (Flag) を追加します | 機能 |
| PSDNET-1621 | 新しい形式の歪みを追加: arc up, arc down, sphere | 機能 |
| PSDNET-1682 | 新しいメソッド PsdImage.AddPosterizeAdjustmentLayer を実装して、新しいポスタリゼレイヤーを追加します | 機能 |
| PSDNET-913  | 開いてすぐに保存すると PSD 情報が失われる | バグ     |
| PSDNET-1352 | 画像の読み込みに失敗する | バグ     |
| PSDNET-1553 | 画像の読み込みに失敗する: UnknownStructure タイプのオブジェクトを DescriptorStructure タイプにキャストできません | バグ     |
| PSDNET-1631 | サードパーティライブラリで変更されたファイルが PSD ファイルを破損させますが、Photoshop で開くことができます | バグ     |


## **パブリック API 変更**
# **追加された API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **削除された API:**
- なし


## **使用例:**

**PSDNET-913. 開いてすぐに保存すると PSD 情報が失われる**

{{< highlight csharp >}}
string src = "Original file.psd";
string outputPsd = "out_Original file.psd";
string outputPng = "out_Original file.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. 画像の読み込みに失敗する**

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

**PSDNET-1553. 画像の読み込みに失敗する: UnknownStructure タイプのオブジェクトを DescriptorStructure タイプにキャストできません**

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
            // 正しく読み込まれるはず
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. サードパーティライブラリで変更されたファイルが PSD ファイルを破損させますが、Photoshop で開くことができます**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. 新しい形式の歪み (Flag) を追加します**

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

**PSDNET-1621. 新しい形式の歪みを追加: arc up, arc down, sphere**

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

**PSDNET-1682. 新しいメソッド PsdImage.AddPosterizeAdjustmentLayer を実装して、新しいポスタリゼレイヤーを追加します**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// 保存された変更を確認
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
        throw new Exception(message ?? "オブジェクトが等しくありません。");
    }
}
{{< /highlight >}}
