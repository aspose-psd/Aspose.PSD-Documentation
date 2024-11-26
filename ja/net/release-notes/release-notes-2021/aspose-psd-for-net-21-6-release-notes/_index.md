---
title: Aspose.PSD for .NET 21.6 - リリースノート
type: docs
weight: 70
url: /ja/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-546|グループのクリッピングマスクが正しくレンダリングされない|バグ|
|PSDNET-547|レイヤーグループの通常またはベクターマスクがレンダリング時に無視される|バグ|
|PSDNET-647|無効になっているベクターレイヤーマスクを含むPSD画像を保存すると、ベクターマスクが有効になる|バグ|
|PSDNET-786|255文字を超えるテキストを含むTextLayerを作成すると例外が発生する|バグ|
|PSDNET-900|TextレイヤーのテキストをLinux上でレンダリングできない|機能強化|

## **パブリック API の変更**
# **追加されたAPI:**
- なし

# **削除されたAPI:**
- なし

## **使用例:**

**PSDNET-546. グループのクリッピングマスクが正しくレンダリングされない**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. レイヤーグループの通常またはベクターマスクがレンダリング時に無視される**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. 無効になっているベクターレイヤーマスクを含むPSD画像を保存すると、ベクターマスクが有効になる**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. 255文字を超えるテキストを含むTextLayerを作成すると例外が発生する**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
