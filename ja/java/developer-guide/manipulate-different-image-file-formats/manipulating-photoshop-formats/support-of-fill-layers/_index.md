---
title: 色埋めレイヤーのサポート
type: ドキュメント
weight: 50
url: /ja/java/support-of-fill-layers/
---

## **色埋めレイヤーの色でのサポート**
この記事では、PSDレイヤーを色で埋める方法を説明します。Aspose.PSD.FileFormats.Psd.Layers.FillLayerを使用してPSDレイヤーに色を追加してください。次のコードスニペットは、PSDファイルを読み込み、FillLayerクラスにアクセスし、FillLayer.FillSettingsプロパティを使用して色を設定する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **グラデーション色での色埋めレイヤーのサポート**
この記事では、グラデーション色を使用してPSDレイヤーを色で埋める方法を示しています。Aspose.PSD APIには、この目標を達成するための効率的かつ使いやすいメソッドが公開されています。Aspose.PSDは、GradientColorPointおよびGradientTransparencyPointクラスを使ってレイヤーにグラデーション効果を追加しました。

PSDレイヤーをグラデーション色で埋める手順は以下のとおりです:

- Imageクラスによって公開されたLoadファクトリーメソッドを使用して画像としてPSDファイルを読み込みます。
- FillLayerオブジェクトの設定プロパティを設定します。
- 必要な色と色の位置を持つColorPointsのリストを作成します。
- 必要な不透明度と透明度ポイントの位置を持つtransparencyPointsのリストを作成します。
- FillLayer.Updateメソッドを呼び出します。
- 結果を保存します。

以下のコードスニペットは、PSDレイヤーにグラデーション色を追加する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **色でのストローク効果**
この記事では、色でストローク効果をレンダリングする方法を示しています。ストローク効果は、レイヤーや図形にストロークやボーダーを追加するために使用されます。単色の線、カラフルなグラデーション、およびパターン化されたボーダーを作成するために使用することができます。

色でストローク効果をレンダリングする手順は以下のとおりです:

- **LoadEffectsResource** プロパティを設定します。
- Imageクラスによって公開されたLoadファクトリーメソッドを使用して画像としてPSDファイルを読み込み、PsdLoadOptionsを定義します。
- **ColorFillSetting** の設定プロパティを設定します。
- 結果を保存します。

以下のコードスニペットは、色でストローク効果をレンダリングする方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}



