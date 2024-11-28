---
title: Aspose.PSD for .NET 23.7 - リリースノート
type: docs
weight: 60
url: /ja/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

このページは、[Aspose.PSD for .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)のリリースノートを含んでいます。

{{% /alert %}}

| **キー**     | **概要**                                                                                                  | **カテゴリ** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | PSDファイルの各レイヤーをアニメーションGIFファイルにエクスポートする機能を追加                                        | 機能 |
| PSDNET-1441 | ShapeレイヤーのFillプロパティをvscgリソースから割り当てる                                                       | 機能 |
| PSDNET-1534 | 新しいワープのタイプを追加 (arc & arch)                                                                           | 機能 |
| PSDNET-1543 | UpdateMetadataプロパティがtrueに設定されている場合、PSDファイルを保存するアプリケーションをAspose.PSDに変更する       | 機能 |
| PSDNET-1567 | ワープ画像の計算領域を拡大する                                                                                | 機能 |
| PSDNET-1471 | ブラック＆ホワイト調整レイヤーがセミ透明を誤って処理する                                                  | バグ     |
| PSDNET-1505 | AllowWarpRepaintオプションが有効な場合、SmartObject ReplaceContentsが計算後2分で中断する                         | バグ     |
| PSDNET-1585 | レイヤーグループの実際の左端と上端の位置を取得する機能を追加                                                 | バグ     |
| PSDNET-1589 | レイヤーのリサイズがVogkResourceがポイント構造を持つPSDファイルで誤って動作する                             | バグ     |
| PSDNET-1608 | TextBoundが期待どおりに機能しない                                                                           | バグ     |
| PSDNET-1612 | デフォルトコンストラクターで作成されたレイヤーをPSD画像に追加すると、デフォルトのリソースが追加されない              | バグ     |
| PSDNET-1623 | Timeline.LoopsCountはアニメーションGIFにエクスポートする際に無視される                                        | バグ     |


## **パブリックAPIの変更**
# **追加されたAPI:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **削除されたAPI:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **使用例:**

**PSDNET-802. PSDファイルの各レイヤーをアニメーションGIFファイルにエクスポートする機能を追加**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // 各レイヤー用のフレームを作成する。
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // 現在の状態を更新する
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}
...
... (中略)
...
...