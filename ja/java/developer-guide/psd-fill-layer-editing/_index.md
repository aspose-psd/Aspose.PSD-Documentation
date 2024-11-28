---
title: Javaを使用してPSD Fill Layerの更新
weight: 100
type: docs
description: カラーフィル、グラデーションフィル、パターンフィルを含むすべての調整レイヤーの使用例
keywords: [fill layer, Color Fill, Gradient Fill, Pattern Fill, psd api, java, code sample]
url: ja/java/psd-fill-layer-editing/
---

## **概要**

通常のレイヤーを作成するには、レイヤーの位置とサイズを定義するパラメーターが必要なcreateRegularLayer関数を使用します。この関数は新しいレイヤーを作成し、その境界を設定し、指定した色で塗りつぶします。

カラーフィルレイヤーの場合、FillType.Colorパラメーターを使用してFillLayer.createInstanceメソッドを使用します。フィルレイヤーが作成されたら、fill_settingsプロパティを介してその塗りつぶし設定にアクセスし、ColorFillSettingsクラスのcolorプロパティを使用して必要な色を設定します。このコンテキストでは、色はColor.getCoral()に設定されています。また、フィルレイヤーのclippingプロパティを1に設定することで、クリッピングマスクとして機能させます。

グラデーションフィルレイヤーはFillType.Gradientパラメーターを使用して同様に作成されます。カラーフィルレイヤーと同様に、fill_settingsを介して塗りつぶし設定にアクセスし、グラデーションカラーポイントと透明度ポイントを設定します。この例では、グラデーションカラーポイントはGradientColorPointクラスで定義され、透明度ポイントはGradientTransparencyPointクラスで定義されます。また、フィルレイヤーのclippingプロパティも1に設定されています。

パターンフィルレイヤーはFillType.Patternパラメーターを使用して作成されます。再度、fill_settingsを介して塗りつぶし設定にアクセスし、パターンデータやその他のプロパティを設定します。このコードでは、PatternFillSettingsクラスを使用してパターンデータを定義し、clippingプロパティを1に設定しています。

フィルレイヤーを作成したら、各フィルレイヤーの表示名やその他のプロパティを指定してPSDイメージに追加します。

最後に、提供されたコードを使用してPSDイメージとそれに対応するPNGイメージを保存します。PNGオプションは、透明度を持つ真のカラーを使用するように構成されています。

詳細については、完全な例を参照してください。

## **例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}
