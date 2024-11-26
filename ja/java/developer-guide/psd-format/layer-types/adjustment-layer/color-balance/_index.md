---
title: カラーバランス調整レイヤー
type: docs
weight: 30
url: /ja/layer-types/adjustment-layer/color-balance/
---

# JavaでPhotoshopのカラーバランス調整レイヤーを操作する

この記事では、JavaでPSDファイル形式の画像の**カラーバランスを調整**する方法について説明します。Photoshopドキュメントを操作するためのツールボックスであるAspose.PSD for Javaという特別なライブラリを使用します。

このライブラリはPSDファイル形式と連携しているため、Photoshopエディタで利用可能なほぼ[すべての機能](https://docs.aspose.com/psd/java/features/)を備えており、**カラーバランス調整レイヤー**もその例外ではありません。

カラーバランス調整レイヤーを使用すると、影、中間トーン、ハイライトにおける主要（RGB）と減法（CMY）色のバランスを簡単かつ迅速に変更することが可能です。

## カラーバランスの調整

先述のように、Aspose.PSD for Javaのカラーバランス調整レイヤーは**主要色と減法色のバランサー**であることがわかります。つまり、各色のペア（シアン/赤、マゼンタ/緑、イエロー/青）に対して3つのスケールがあります。値がそれに向かうと特定の色の強度が増加し、逆もまた然りです。さらに、これらの3つのペアは、各領域（影、中間トーン、ハイライト）に固有であり、この種の調整の柔軟性を高めます。

では、この知識を実践で活用してみましょう。例として、赤みがかった女性の顔の写真を選びました（b）。顔が赤みがかっているため、**カラーバランス調整レイヤーを追加**して赤を減らし、シアンを基本的に増やすことで、より自然な見た目にします（c）。この画像にはさらに作業が必要ですが、この記事ではこれで終わります。

![カラーバランス調整レイヤーの例](color-balance-adjustment-layer-example-figure-1.png) カラーバランス調整レイヤーのAPIはフラットなデザインを持っています。したがって、すべてが揃っている[ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer)クラスが必要です。まず、デフォルトで無効になっている明るさを保持します。その後、対応するメソッドを使用して（メソッド名は特定のトーン範囲領域名と色のペアの名前で構成されています）、影に少し緑を追加し、黄色/青のバランスを調節し、中間トーンにさらにシアンを追加し、少し青を加え、最後にハイライトにシアンをさらに追加し、少しマゼンタと青を加えます。

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

これで、望んだ画像を手に入れました！簡単でしょう？

注意が必要なのは、_各色のペアの値は-100から100の範囲内にある必要がある_ことです。これは、Photoshopエディタと同様に、減法色に負の値を、主要色に正の値を維持するためです。

詳細な技術的情報を得るには、[カラーバランス調整レイヤー](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer)に関する当社のAPIリファレンスをご参照ください。

## 結論

この記事では、JavaでAspose.PSD for Javaライブラリを使用してプログラムで画像のカラーバランスを調整する方法を考察しました。このライブラリには、Photoshop文書のカラーバランス調整レイヤーを扱うための完全な機能を備えたAPIが含まれています。
