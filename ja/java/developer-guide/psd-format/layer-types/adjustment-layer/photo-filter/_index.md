---
title: フォトフィルター調整レイヤー
type: docs
weight: 30
url: /ja/java/layer-types/adjustment-layer/photo-filter/
---

# Java で Photoshop のフォトフィルター調整レイヤーを操作する

今日は、Aspose.PSD for Java を使用して既存の Photoshop ドキュメントにフォトフィルター調整レイヤーを適用する方法を見ていきます。Aspose.PSD for Java は PSD ファイル形式を操作するためのライブラリです。

**フォトフィルター調整レイヤー API** は着色によって画像の色バランスを変更します。結果の画像は、実際のカメラフィルターを使用した後と同じように見えます。ライブラリのフォトフィルター調整レイヤー API は、まだ事前に定義されたフィルターがないため、Photoshop のものとわずかに異なります。ただし、その他の点では同じです。つまり、着色の色を設定し、密度を変更し、ルミナンスを保持するオプションを使用することができます。

## API 概要

フォトフィルター調整レイヤー API は非常に使いやすいです。この調整レイヤーへのエントリーポイントであるメインの [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) クラスがあり、色、密度、および調整が行われるルミナンスを保持する手段といったわずか 3 つの公開プロパティのみが含まれています。

## 色バランスを調整する

話すことがあまりないので、フォトフィルターを使用した**色バランスの調整の例**をすぐに見てみましょう。写真に温かみのある調整フィルター（a）を手動で追加し、シカの彫刻のイメージ（b）を暖かいトーン（c）にして、見栄えの良いイメージにします。

![フォトフィルター調整レイヤーの例](photo-filter-adjustment-layer-figure-1.png)

まず、他の調整レイヤーとは異なり、[ファクトリメソッド](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-)にデフォルトの引数のメソッドがないことに注目してください。したがって、ロードされた Photoshop ドキュメントにフォトフィルター調整レイヤーを追加するには、[color](https://reference.aspose.com/psd/java/com.aspose.psd/Color) という単一の引数が必要です。したがって、温かみのあるフィルター効果を再現するには、ファクトリメソッドに引数としてオレンジを渡し、対応するセッターを使用して密度を設定します：

```java
PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
photoFilterLayer.setDensity(25);
```

密度プロパティには 100 というデフォルト値があり、ルミナンスを保持するプロパティのデフォルト値は true です（このオプションを明示的に有効にしないのはそのためです）。

## 結論

この記事では、Aspose.PSD for Java のフォトフィルター調整レイヤー API の使用方法を考察しました。このツールは使いやすく、画像に可変密度の着色を追加することができます。全体の画像の色バランスを調整するためのスピーディな方法です。
