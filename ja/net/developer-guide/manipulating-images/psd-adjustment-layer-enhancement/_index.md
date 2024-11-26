---
title: PSDの向上のための調整レイヤーの使用
weight: 100
type: docs
description: Aspose.PSDを使用してC#で調整レイヤーを使用する例
keywords: [調整レイヤー, 写真強調, カーブ調整, レベルの向上, 反転, 写真フィルタ, PSD API, C#, シャープ, コードサンプル]
url: ja/net/adjustment-layer-enhancement/
---

## 概要

本記事では、Aspose.PSDを使用してC#で調整レイヤーの編集を探索します。調整レイヤーは画像編集での強力な機能であり、画像に対して非破壊的な変更を行うことができます。Aspose.PSDは、さまざまな要素を変更するために使用できる調整レイヤークラスの包括的なセットを提供しています。

調整レイヤーの編集をデモンストレーションするために、このページの最後にPSDイメージをロードし、そのレイヤーに異なる調整を適用するサンプルコードスニペットを使用します。

以下のコードスニペットでは、'PsdImage.Load()' メソッドを使用して PSD イメージをロードしてから、出力 PNG ファイルの設定を行います。'PngOptions' クラスを使用すると、出力イメージの色タイプを指定できます。

次に、PSD イメージ内の各レイヤーを反復し、'IsAssignable()' メソッドを使用してそのタイプを確認します。レイヤーが特定のタイプである場合、'Cast()' メソッドを使用してそのタイプにキャストし、必要な調整を適用します。たとえば、'BrightnessContrastLayer' の明るさとコントラストを調整し、'LevelsLayer' のレベルを変更し、'CurvesLayer' に曲線ポイントを追加し、などです。

他の調整を適用するために追加のコードを追加できます。Aspose.PSDは、[ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer)、[HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer)、[ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer)、[BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer)、[PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer)、[ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer)、[InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer)、[PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer)、[ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer)、[SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) など、幅広い調整レイヤークラスを提供しています。

最後に、変更されたイメージを 'PsdImage' クラスの 'Save()' メソッドを使用して保存します。

このコードは、Aspose.PSDを使用したC#での調整レイヤーの編集方法の基本的な概要を提供しています。調整をカスタマイズし、APIドキュメントで利用可能なさまざまなオプションを探索できます。

## 例

以下は、Aspose.PSDを使用したC#で調整レイヤーを使用する方法を示すコードサンプルです:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

より詳細な情報や例については、[Aspose.PSD for C#のドキュメント](https://docs.aspose.com/psd/net/)をご覧ください。
