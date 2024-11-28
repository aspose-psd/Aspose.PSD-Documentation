---
title: ブラックアンドホワイト調整レイヤー
type: docs
weight: 30
url: /ja/java/layer-types/adjustment-layer/levels/
---

## JavaでPhotoshop Levels調整レイヤーを使用する

この記事では、Javaで[PSDファイル形式](/psd/ja/java/psd-format/)の写真のトーンレンジとカラーバランスをプログラムで調整する方法を学びます。Adobe® Photoshop®写真編集ソフト自体は使用しません。代わりに、Photoshopドキュメントを操作するために独自に機能するJava向けのAspose.PSDライブラリを使用します。

Aspose.PSD for Javaは、[写真の編集に十分なツール](/psd/ja/java/manipulating-images/)をサポートしていますが、**作業を行う最もシンプルで迅速な方法の1つであるLevels調整レイヤーAPIを使用**します。

## API概要

現在のLevels調整レイヤーAPIの実装（執筆時の20.6版）は、Photoshop Levelsのすべての基本機能をサポートしており、合成チャンネル（RGB）および各プライマリカラーチャンネル（赤、緑、青）の入力および出力レベルを調整するという名目のものです。

Levels調整レイヤーのAPIは直感的です。[LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer)クラスはLevels調整へのエントリーポイントです。カラーチャンネルにアクセスするためのいくつかのメソッドを含みます。getMasterChannelおよびgetChannel(int)の両方は、入力および出力レベルの操作のための対応するプロパティを持つ[LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel)を返します。違いは、getMasterChannelが合成カラーチャンネル（RGB）を調整するために役立ち、getChannelはインデックスによって特定のカラーチャンネル（赤、緑、青）にアクセスします。

## カラーモードとの互換性

Levels調整レイヤーは、Photoshop Levelsに応じて、**ほとんどのカラーモードと互換性があります**。そのため、グレースケール（グレーチャンネル）、RGB（RGB、赤、緑、青チャンネル）、CMYK（CMYK、シアン、マゼンタ、イエロー、ブラックチャンネル）、デュオトーン（モノトーンチャンネル）、LAB（明度、a、bチャンネル）のカラーモードの画像のレベルを調整できます。

## トーンレンジの調整

単純に言うと、トーン補正は画像に適用され、影とハイライトを再マップし、中間トーンをより良い配布にするものです。一般的には、**正しく行われれば画像をよりコントラスト**させることができます。たとえば、犬の写真（b）を取り、そのトーンレンジ（a - 画像をよりコントラストに見せるためにPhotoshop Levelsウィンドウからキャプチャされたスクリーンショット）を調整して、写真をよりコントラストに見せることができます（c）。

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Levelsレイヤー図1](levels-adjustment-figure-1.png)|

画像の**全体的なトーンレンジを調整**するには、マスターチャンネルの入力レベルを設定する必要があります：

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

影には0から253、中間トーンには0.01から9.99、ハイライトには2から255の範囲の入力レベルが必要です。出力レベルの範囲は0から255の間でなければなりません。

さらに例が必要ですか？[Github](https://github.com/aspose-psd/Aspose.PSD-for-Java)や[ナレッジベース](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers)で見つけることができます。

## 結論

要約すると、Aspose.PSD for Javaはほとんどすべてのカラーモードと互換性があり、画像のトーンレンジとカラーバランスを変更するための便利でシンプルなAPIを提供しています。このライブラリのLevels調整レイヤーAPIはPhotoshop Levelsに似ているため、ライブラリを使ったことがなくても簡単に始めることができます。
