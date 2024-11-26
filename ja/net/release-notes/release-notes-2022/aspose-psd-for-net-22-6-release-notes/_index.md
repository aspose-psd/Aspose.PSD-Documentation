---
title: Aspose.PSD for .NET 22.6 - リリースノート
type: docs
weight: 70
url: /ja/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-940|異なるファイルの同様のレイヤーに対するユニークハッシュを取得するためのAPIを作成します|拡張|
|PSDNET-678|パターンが複数あり、レイヤーの順序が変更された場合の FillLayer の不正なレンダリング|バグ|
|PSDNET-1125|CMYK カラーモードを持つ特定の PSD ファイルの読み込み時に例外が発生する|バグ|


## **公開 API 変更**
# **追加された API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **削除された API:**
- なし


## **使用例:**

**PSDNET-678. パターンが複数あり、レイヤーの順序が変更された場合の FillLayer の不正なレンダリング**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. 異なるファイルの同様のレイヤーに対するユニークハッシュを取得するAPIを作成します**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

// コードの内容は翻訳対象外
{{< /highlight >}}

**PSDNET-1125. CMYK カラーモードを持つ特定の PSD ファイルの読み込み時に例外が発生する**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}