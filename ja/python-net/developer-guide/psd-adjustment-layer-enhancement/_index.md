---
title: プログラムを使用してPSDの改良を行う調整レイヤー
weight: 100
type: docs
description: Pythonを介したAspose.PSDを使用して調整層を使用する例
keywords: [調整レイヤー, 写真の強化, 曲線調整, レベルの向上, 反転, 写真フィルター, psd api, python, コードサンプル]
url: ja/python-net/adjustment-layer-enhancement/
---

## **概要**

この記事では、PythonでAspose.PSDを使用して調整層を編集する方法について説明します。調整層は、画像編集において非破壊的な変更を加えることができる強力な機能であり、あなたの画像の様々な側面を修正するために使用できる包括的な調整層クラスをAspose.PSDが提供しています。

調整レイヤーの編集をデモンストレーションするために、サンプルコードスニペットを使用します。そのコードは、PSD画像を読み込み、そのレイヤーに異なる調整を適用するものです。

以下のコードスニペットでは、PsdImage.load()メソッドを使用してPSD画像を読み込み、出力PNGファイルの設定を行います。PngOptionsクラスを使用することで、出力画像の色のタイプを指定できます。

次に、PSD画像内の各レイヤーについて反復処理を行い、is_assignable()メソッドを使用してそのタイプをチェックします。特定のタイプの場合は、cast()メソッドを使用してそのタイプにキャストし、必要な調整を適用します。例えば、BrightnessContrastLayerの明るさとコントラストを調整したり、LevelsLayerのレベルを修正したり、CurvesLayerに曲線ポイントを追加したりします。

他の調整を各レイヤーに適用するために、追加のコードを追加できます。Aspose.PSDは、[ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer)、[HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer)、[ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer)、[BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer)、[PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer)、[ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer)、[InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer)、[PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer)、[ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer)、[SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer)などの調整層クラスの幅広い範囲を提供しています。

最後に、PsdImageクラスのsave()メソッドを使用して修正された画像を保存します。

このコードは、Aspose.PSDを使用したPythonでの調整レイヤーの編集方法の基本的な概要を提供します。必要に応じて調整をカスタマイズし、APIドキュメントで利用可能なさまざまなオプションを探索してください。

フルな例をご確認ください。

## **例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
