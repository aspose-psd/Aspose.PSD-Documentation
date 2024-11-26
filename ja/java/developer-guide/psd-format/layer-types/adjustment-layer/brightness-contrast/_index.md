---
title: ブライトネスコントラスト調整レイヤー
type: ドキュメント
weight: 30
url: /ja/java/layer-types/adjustment-layer/brightness-contrast/
---

# JavaでPhotoshopのBrightness/Contrast調整レイヤーを操作する

本記事では、Aspose.PSD for Java®ライブラリを使用してAdobe® Photoshop®ドキュメントにBrightness/Contrast調整を適用します。また、この種の調整レイヤーに関連するライブラリの機能についても紹介していきます。

しかし、まずは少しだけ理論から。

Brightness/Contrast調整レイヤーは画像の明るさとコントラストを変更します。ところが、これは具体的にどういう意味でしょうか？ 明るさを上げると、色値が白に向かって明るくなり、明るさを下げると色値が黒に向かって暗くなります。対して、コントラストを上げると明るい色と暗い色の差が増え、コントラストを下げるとその差が減少します。すなわち、明るい色がより明るく、暗い色がより暗くなるということです。

## カラーモードのサポート

このライブラリでは、RGB、CMYK、またはLabカラーモードの画像にBrightness/Contrast調整レイヤーを追加することができます。

## 現在の挙動と旧式の挙動

現在のライブラリの実装（執筆時点でのバージョン20.6）は、シャドウからハイライトまでのフルトーンレンジを保持するPhotoshopのデフォルトアルゴリズムを使用していますが、まだ旧式の挙動には対応していません。つまり、このライブラリはPhotoshopの最新バージョン（CS4以降）で作成されたドキュメントにおいてBrightness/Contrast調整レイヤーをサポートしています。ただし、必要であれば、[フォーラム](https://forum.aspose.com/c/psd)でBrightness/Contrast調整レイヤーの旧式の実装をリクエストすることができます。

## 明るさとコントラストの調整

さて、Brightness/Contrast調整レイヤーのハイレベルAPIがどのように機能するかを説明します（前もって言っておきますが、APIはわかりやすい構造です）。PsdImageクラスには、BrightnessContrastLayerクラスをインスタンス化するためのファクトリーメソッド（addBrightnessContrastAdjustmentLayer）が含まれており、これは明るさとコントラストの調整の入り口となります。BrightnessContrastLayerクラスには、明るさとコントラストのプロパティにアクセスするためのゲッターとセッターのペアが含まれており、その値を変更することができます。

![|PSDでのBrightness/Contrast調整レイヤーの例](brightness-contrast-psd-adjustment-layer-figure-1.png)

したがって、例えば犬の画像(b)の明るさを調整1し、コントラストを調整2する(a)ことで、対応する引数を用いてファクトリーメソッドを実行するだけで、より鮮明なイメージ(c)を得ることができます。

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

注：

1. 明るさの値は-150から150の範囲内である必要があります。
2. コントラストの値は-50から100の範囲内である必要があります。

詳細については、[BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer)のドキュメントを参照してください。

## 結論

この記事では、Brightness/Contrast調整レイヤーの概要を把握し、ファクトリーメソッドを使用して画像の明るさとコントラストを調整する方法を学びました。

もっと学ぶために、Aspose.PSD for Javaの[調整レイヤーAPIに関するシリーズの記事](/psd/ja/java/layer-types/adjustment-layer/)を参照してください。
