---
title: 曝露調整レイヤー
type: docs
weight: 30
url: /ja/java/layer-types/adjustment-layer/exposure/
---

# JavaでPhotoshop曝露調整レイヤーを操作する

この記事では、Aspose.PSD for Javaを使用してAdobe® Photoshop®ドキュメントに曝露調整レイヤーを追加する方法について説明します。このライブラリは、独自の画像処理アルゴリズムを使用しているため、Photoshopエディタをインストールする必要はありません。また、ライブラリの曝露調整APIに関連する詳細も学びます。

## API概要

曝露調整レイヤーは、[ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer)クラスを介して構成されます。このクラスには曝露調整に関連する以下のプロパティが含まれています:

- フォトがどれだけの光を持っているかを定義し、ヒストグラム全体をブラックに対して圧縮または伸張することによって、主にハイライトに影響を与えます。
- 曝露オフセットは主にシャドウに影響を与えます。
- ガンマ補正は画像の輝度を補正します。

## 正しい曝露

曝露を補正するためには、クラスのいくつかのプロパティを変更するだけで済みます。ライブラリのExposure調整（a）をライブラリのアンダーエクスポージャ写真（b）に適用して、人間の目で認識できるようにするための手順を説明します。

![曝露調整レイヤーの例](exposure-adjustment-layer-figure-1.png)

全体の調整は主にガンマ補正を使用して行われます。ただし、曝露とオフセットも少し調整されます。すべきことは、既に言及したプロパティに適切な値を設定するだけです:

```java
ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
exposureLayer.setExposure(-0.03f);
exposureLayer.setOffset(-0.0005f);
exposureLayer.setGammaCorrection(1.85f);
```

曝露は-20.0から20.0の範囲内、オフセット値は-0.5から0.5の範囲内、ガンマ補正の値の範囲は9.99から0.01の間であることに注意してください。

詳細については、[Exposure調整レイヤーのAPIリファレンス](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer)を参照してください。

## 結論

この記事では、PSDファイルに曝露調整レイヤーを追加して画像を明るくする方法や、いくつかのAPIの詳細について学びました。
