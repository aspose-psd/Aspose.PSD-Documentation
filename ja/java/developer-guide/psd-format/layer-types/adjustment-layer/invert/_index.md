---
title: レイヤーのタイプを反転させる
type: ドキュメント
weight: 30
url: /ja/layer-types/adjustment-layer/invert/
---

# Java で Photoshop Invert 調整レイヤーを操作する

この記事では、Java で Photoshop ドキュメント内の画像をプログラムでネガティブに変換する方法を紹介します。この目的のために、Aspose.PSD for Java という PSD ファイル形式操作用のライブラリを使用します。

色反転 API を使用することで、**画像にネガティブ効果を追加**することができます。以前、[カーブ調整レイヤーを使用して画像の色を反転させる方法](/psd/ja/java/layer-types/adjustment-layer/curves/)をご覧になった方もいるかもしれません。しかし、今日は Invert 調整レイヤーを使用した仕事をより早く簡単に行う方法を考えます。

## API 概要

**Invert 調整レイヤー API** には、[InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer) というレイヤークラス自体が含まれています。このクラスには独自の公開メンバーがないため、親クラス（[AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)）からのすべての公開メンバーを継承しています。この事実により、使用が容易になります。PSD ファイルに追加するだけで画像がネガティブになります。

## 画像の色を反転させる

したがって、明らかであるように思われるかもしれませんが、クリアリティのために、**宇宙飛行士の画像（a）に Invert 調整レイヤーを適用**してその画像にネガティブ効果を与える方法を示します。

![Invert Adjustment Layerの前後の例](invert-adjustment-layer-figure-1.png)

画像の色を反転させるには、単純に PSD に Invert 調整レイヤーを追加します:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

以上です！この種類の調整レイヤーに設定する必要のある特定のプロパティはありません。

## 結論

この記事では、Aspose.PSD for Java の Invert 調整レイヤー API について学びました。この調整レイヤーの API は公開メンバーを宣言していないため、画像をネガティブに取得するための手間のかからないツールです。
