---
title: パソス.PSDを使用したPSDの強化のための調整レイヤー
weight: 100
type: ドキュメント
description: Java向けAspose.PSDを使用した調整レイヤーの例
keywords: [調整レイヤー, 写真強化, カーブ調整, レベル強化, 反転, 写真フィルタ, psd api, java, コードサンプル]
url: ja/adjustment-layer-enhancement/
---

## **概要**

この記事では、Java向けAspose.PSDでの調整レイヤーの編集を探索します。調整レイヤーは画像編集の中で非破壊的な変更を可能にする強力な機能であり、さまざまな画像の側面を変更するために使用できる包括的な調整レイヤークラスがAspose.PSDに提供されています。

調整レイヤーの編集をデモンストレーションするために、PSD画像を読み込んで異なる調整を適用するサンプルコードスニペットを提供します。

以下のコードスニペットでは、PsdImage.load() メソッドを使用してPSD画像を読み込みます。次に、出力PNGファイルの保存オプションを設定します。PngOptionsクラスを使用することで、出力画像のカラータイプを指定できます。

その後、PSD画像の各レイヤーを反復処理し、isAssignable() メソッドを使用してそのタイプを確認します。レイヤーが特定のタイプである場合は、cast() メソッドを使用してそのタイプにキャストし、必要な調整を適用します。たとえば、BrightnessContrastLayerの明るさとコントラストを調整し、LevelsLayerのレベルを変更し、CurvesLayerに曲線点を追加します。

他の調整を各々のレイヤーに適用するための追加コードを追加できます。Aspose.PSDは、ExposureLayer、HueSaturationLayer、ColorBalanceAdjustmentLayer、BlackWhiteAdjustmentLayer、PhotoFilterLayer、ChannelMixerLayer、InvertAdjustmentLayer、PosterizeLayer、ThresholdLayer、SelectiveColorLayerなど、幅広い調整レイヤークラスを提供しています。

最後に、PsdImageクラスのsave() メソッドを使用して変更された画像を保存します。

これは、Aspose.PSDを使用したJavaでの調整レイヤーの編集方法の基本的な概要を提供します。要件に応じて調整をカスタマイズし、APIドキュメントで利用可能なさまざまなオプションを調査できます。

以下に完全な例をご確認ください。

## **例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
