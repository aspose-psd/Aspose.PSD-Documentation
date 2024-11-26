---
title: Pythonを使用したPSDフィルレイヤーの更新
weight: 100
type: docs
description: カラーフィル、グラデーションフィル、パターンフィルを含むすべての調整レイヤーの使用例
keywords: [fill layer, カラーフィル, グラデーションフィル, パターンフィル, psd api, python, コードサンプル]
url: /ja/python-net/psd-fill-layer-editing/
---

## **概要**

通常のレイヤーを作成するには、コードで提供されるcreate_regular_layer関数を使用できます。この関数は、レイヤーの位置とサイズを定義するleft、top、width、heightパラメータを取ります。新しいレイヤーを作成し、その境界を設定し、指定した色で塗りつぶします。

カラーフィルレイヤーを作成するには、FillLayer.create_instanceメソッドをFillType.COLORパラメータと共に使用できます。フィルレイヤーを作成した後、fill_settingsプロパティを使用してその塗りつぶし設定にアクセスし、ColorFillSettingsクラスのcolorプロパティを使用して色を設定できます。提供されたコードでは、色はColor.coralに設定されています。フィルレイヤーのclippingプロパティは1に設定されており、レイヤーをクリッピングマスクとして機能させます。

グラデーションフィルレイヤーを作成するには、FillLayer.create_instanceメソッドをFillType.GRADIENTパラメータと共に使用できます。カラーフィルレイヤーと同様に、fill_settingsプロパティにアクセスしてグラデーションカラーポイントと透明度ポイントを設定できます。提供されたコードでは、グラデーションカラーポイントはGradientColorPointクラスを使用して定義し、透明度ポイントはGradientTransparencyPointクラスを使用して定義します。フィルレイヤーのclippingプロパティも1に設定されています。

パターンフィルレイヤーを作成するには、FillLayer.create_instanceメソッドをFillType.PATTERNパラメータと共に使用できます。再度、fill_settingsプロパティにアクセスしてパターンデータやその他のプロパティを設定できます。提供されたコードでは、パターンデータはPatternFillSettingsクラスを使用して定義され、clippingプロパティは1に設定されています。

フィルレイヤーを作成した後、add_layerメソッドを使用してそれらをPSDイメージに追加できます。また、各フィルレイヤーに表示名やその他のプロパティを指定することもできます。

最後に、提供されたコードを使用して、PSDイメージとそれに対応するPNGイメージを保存できます。PNGオプションは、透明性のためにアルファ付きのトゥルーカラーを使用するように設定されています。

詳細な例をご確認ください。

## **例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}
