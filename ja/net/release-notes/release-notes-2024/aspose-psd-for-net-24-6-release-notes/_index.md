---
title: Aspose.PSD for .NET 24.6 - リリースノート
type: docs
weight: 70
url: /ja/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**    | **概要**                                                                             | **カテゴリ** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | グラデーションマップレイヤーのサポートを実装する                                                                          | 機能      |
| PSDNET-1670 | [AIフォーマット] AIフォーマットにXPacketメタデータのサポートを追加する                                                                          | 機能      |
| PSDNET-1831 | Inflate、Squeeze、Twistタイプのワープを実装する                                                                          | 機能      |
| PSDNET-1653 | ArtBoardレイヤを含むファイルでRgbとLabモードは3チャンネル未満または4チャンネルを超過することはできない                                                                          | バグ      |
| PSDNET-1775 | 特定のファイルの処理中、処理領域の上部は正でなければなりません (パラメータ 'areaToProcess')                                                                          | バグ      |
| PSDNET-2052 | キャンバスイメージの拡張部分が保存後に切り取られる。データが失われますが、プレビューは正常に見えます                                                                          | バグ      |

## **パブリックAPI変更**
# **追加されたAPI:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **削除されたAPI:**
- なし

## **使用例:**

**PSDNET-1450. グラデーションマップレイヤーのサポートを実装する**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // グラデーションマップ調整レイヤを追加
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// 保存された変更を確認
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "オブジェクトが等しくありません。");
    }
}
{{< /highlight >}}

**PSDNET-1670. [AIフォーマット] AIフォーマットにXPacketメタデータのサポートを追加する**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("オブジェクトが等しくありません。");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("テストオブジェクトはnullです。");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Xmpメタデータが追加されました。
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // ここでAIファイルのXmpパッケージにアクセスできるようになりました。
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // これらのパッケージのコンテンツにアクセスできるようになりました。
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. Inflate、Squeeze、Twistタイプのワープを実装する**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. ArtBoardレイヤを含むファイルでRgbとLabモードは3チャンネル未満または4チャンネルを超過することはできない**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // ここには例外が発生しないはずです
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. 特定のファイルの処理中、処理領域の上部は正でなければなりません (パラメータ 'areaToProcess')**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // 例外が発生すべきではありません
}
{{< /highlight >}}

**PSDNET-2052. 保存後、キャンバスイメージが拡張され、切り取られる。データが失われますが、プレビューは正常に見えます**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // ここでエラーが発生すべきではありません
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // ここでエラーが発生すべきではありません
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
