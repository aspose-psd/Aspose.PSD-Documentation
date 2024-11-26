---
title: チャネルミキサーアジャストメントレイヤー
type: ドキュメント
weight: 30
url: /ja/java/layer-types/adjustment-layer/channel-mixer/
---

# JavaでPhotoshopのチャネルミキサーアジャストメントレイヤーを使用する

今日は、JavaでPhotoshopドキュメント内のチャネルカラーをプログラムでミックスする方法を見ていきます。PhotoshopエディターはJavaスクリプティングをサポートしていないため、Aspose.PSD for Javaという特別なPSDファイル形式の操作ライブラリを使用します。

このライブラリには**カラーチャンネルを操作するAPI**が含まれています。色を混ぜる方法はいくつかありますが、この記事ではチャネルミキサーアジャストメントレイヤーに焦点を当てます。

チャネルミキサーアジャストメントレイヤーAPIを使用すると、色チャンネルを操作して色のハーモニーを作成したり、さまざまなクリエイティブな色の効果を作成したり、画像をモノクロに変換したりすることができます。次に、Aspose.PSD for Javaを使用して既存のPhotoshopドキュメントにチャネルミキサーアジャストメントを適用する方法について考えていきますが、まずは全体的なAPIの機能について話し合う必要があります。

## API概要

チャネルミキサーアジャストメントレイヤーを作成するのに特別なことはありません。[デフォルトのファクトリーメソッド](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--)を介して追加でき、これはChannelMixerLayerクラスのインスタンスを返します。このクラスにはモノクロオプションや出力チャンネルを取得するメソッドなど、一般的な機能が含まれています。特定の出力チャンネルは、[CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel)または[RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel)のいずれかになります。[MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel)のタイプは、画像の[カラーモード](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--)によって異なります。

## 画像をモノクロにする

次に、既存のPhotoshopドキュメントにチャネルミキサーアジャストメントレイヤーを適用する例を考えてみましょう。この種のアジャストメントレイヤーはまだプリセットをサポートしていませんので、**ブラック＆ホワイト赤外線（RGB）Photoshopプリセット**を再現します。このプリセットを、花が咲いている木の画像に適用します。その結果、赤外線写真の効果を実現したいと思います。

![チャネルミキサーアジャストメントレイヤーの例](channel-mixer-adjustment-psd-layer-figure-1.png) まず、ブラック＆ホワイト赤外線（RGB）Photoshopプリセットを再現するために、モノクロフラグを有効にし、各色（赤、緑、青）の適切な生の値をGray出力チャンネルに設定する必要があります：

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

コードを機能させるために画像はRGBカラーモードである必要があります（RgbMixerChannelクラスへのキャストのため）。CMYKカラーモードもサポートされていますが、対応するカラーモードの画像のみです。

各色の値とConstantプロパティは、-200から200の範囲内である必要があります。

## 結論

この記事では、Aspose.PSD for JavaのチャネルミキサーAPIを使用して、色チャンネル内の色を調整したり、画像をモノクロに変換したりする方法について考察しました。
