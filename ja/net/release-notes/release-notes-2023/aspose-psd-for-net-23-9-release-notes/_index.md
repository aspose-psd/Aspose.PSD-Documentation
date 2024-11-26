---
title: Aspose.PSD for .NET 23.9 - リリースノート
type: docs
weight: 40
url: /ja/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

このページには [Aspose.PSD for .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**   | **概要**                                                                             | **カテゴリ** |
|:-----------|:------------------------------------------------------------------------------------|:---------|
| PSDNET-1638 | 新しい調整レイヤーのマスクの作成を実装する                                            | 機能      |
| PSDNET-1654 | クリップレイヤーをグループのブレンディングオプションとしてサポートする                | 機能      |
| PSDNET-1194 | 16ビットカラーモードの PSD ファイルでは調整レイヤーにマスクが適用されない                | バグ      |
| PSDNET-1235 | テキストレイヤーで括弧のレンダリングが不正確である                                      | バグ      |
| PSDNET-1559 | テキストレイヤーのスタイルを更新できない                                               | バグ      |
| PSDNET-1583 | CMYK で PSD ファイルをエクスポートすると、エクスポートされた PSD の色が壊れる         | バグ      |
| PSDNET-1619 | 特定の PSB ファイルが例外 "矩形に共通処理領域がありません" をスローする               | バグ      |
| PSDNET-1648 | 画像の読み込みに失敗します。OverflowException: 算術演算がオーバーフローしました             | バグ      |


## **パブリック API 変更**
# **追加された API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **削除された API:**
- なし


## **使用例:**

**PSDNET-1638. 新しい調整レイヤーのマスクの作成を実装する**

{{< highlight csharp >}}
string srcFile = "zendeya_BW.psd";
string dstFile = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(dstFile);
}

using (var im = (PsdImage)Image.Load(dstFile))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

**PSDNET-1654. クリップレイヤーをグループのブレンディングオプションとしてサポートする**

{{< highlight csharp >}}
string sourceFile = "example_source.psd";
string outputPsd = "example_output.psd";
string outputPng = "example_output.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

... (以下略)
