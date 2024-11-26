---
title: Aspose.PSD for .NET 23.1 - リリースノート
type: docs
weight: 120
url: /ja/net/aspose-psd-for-net-23-1-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-401|vstkResource のサポート|機能|
|PSDNET-1346|IText インターフェースに編集可能な BaselineDirection/IsStandardVerticalRomanAlignmentEnabled プロパティを追加|機能|
|PSDNET-181|PSD が正しく JPEG に変換されない|バグ|
|PSDNET-958|大きなファイルの PSB から PDF への変換に失敗する|バグ|
|PSDNET-1171|クリッピングマスクの処理を調整レイヤに追加|バグ|
|PSDNET-1252|全体画像のリサイズ後に特定のレイヤのリサイズを行った後、Aspose.PSD がレイヤ保存時に例外をスローする|バグ|


## **公開 API の変更**
# **追加された API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- 他省略

# **削除された API:**
- なし


## **使用例:**

**PSDNET-181. PSD が正しく JPEG に変換されない**

{{< highlight csharp >}}
string srcFile = "helicopter.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. vstkResource のサポート**

{{< highlight csharp >}}
string srcFile = "StrokeShapeTest1.psd";
string dstFile = "StrokeShapeTest2.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile))
{
    Layer layer = image.Layers[1];
    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is VstkResource)
        {
            VstkResource vstkResource = (VstkResource)resource;
            vstkResource.StrokeStyleLineAlignment = StrokePosition.Outside;
            vstkResource.StrokeStyleLineWidth = 20;
        }
    }

    image.Save(dstFile);
}
{{< /highlight >}}

他省略
