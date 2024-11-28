---
title: Aspose.PSD for .NET 22.3 - リリースノート
type: docs
weight: 100
url: /ja/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-210|レイヤーグループ用のIsOpenプロパティを追加|機能|
|PSDNET-643|ラスターレイヤーマスクを持つPSD画像が16bitのPSD画像に保存される際にマスクを破棄する|バグ|
|PSDNET-899|マスクを持つフォルダに対してDissolveブレンドモードが適用されない|バグ|
|PSDNET-1047|Aspose.PSD 21.11 で保存後、特定のファイルをPhotoshopで開けない|バグ|
|PSDNET-1068|Linear Dodge（Add）ブレンドモードを持つレイヤーが正しくレンダリングされない|バグ|
|PSDNET-1069|ロード後の更新時にPattern Fill Layerが例外をスローする|バグ|


## **パブリックAPI変更**
# **追加されたAPI:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **削除されたAPI:**
- なし


## **使用例:**

**PSDNET-210. レイヤーグループ用のIsOpenプロパティを追加**

{{< highlight csharp >}}
// ランタイムでIsOpenプロパティを読み書きする例。
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. ラスターレイヤーマスクを持つPSD画像が16bitのPSD画像に保存される際にマスクを破棄する**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. マスクを持つフォルダに対してDissolveブレンドモードが適用されない**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Aspose.PSD 21.11 で保存後、特定のファイルをPhotoshopで開けない**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Photoshopで出力PSDを手動で開く必要があります。

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // 例外は発生しません。
            }
{{< /highlight >}}

**PSDNET-1068. Linear Dodge（Add）ブレンドモードを持つレイヤーが正しくレンダリングされない**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. ロード後のPattern Fill Layerが更新時に例外をスローする**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}
