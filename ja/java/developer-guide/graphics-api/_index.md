---
title: アスポーズ.PSD for JavaでGraphics APIを使用してPSDファイルのレイヤーを編集する方法
weight: 100
type: docs
description: アスポーズ.PSD for JavaでGraphics APIを使用する例
keywords: [レイヤーを更新, 円を描く, 楕円を描く, 塗りつぶした円を描く, グラフィックス, psd api, java, コードサンプル]
url: ja/java/graphics-api/
---

## **概要**
まず、Image.load()メソッドを使用してPSDファイルをロードするか、ゼロからPsd Imageを作成します。inputFile変数を使用してPSDファイルへのパスを表し、必要に応じてloadOptで読み込みオプションを指定します。

次に、psdImage.getLayers()[0]構文を使用してPSDイメージの最初のレイヤーにアクセスし、操作用のレイヤーオブジェクトへの参照を取得します。

レイヤーを編集するために、レイヤーをパラメーターとして渡してGraphicsオブジェクトを作成します。このオブジェクトには、形状を描画してブラシを適用するためのさまざまなメソッドが提供されています。

Penオブジェクトは、形状のアウトラインの色と太さを定義するために使用されます。同様に、LinearGradientBrushなどのブラシは塗りつぶしの色を定義するために使用されます。

形状をレイヤーに描画するために、graphics.drawEllipse()などのメソッドを使用して形状のアウトラインを描画し、graphics.fillEllipse()を使用して塗りつぶします。

レイヤーに必要な変更を加えた後、変更されたPSDイメージをpsdImage.save()を使用して保存します。

さらに、適切なオプションを使用してPNGなどの他の形式で変更された画像を保存できます。

以上で、アスポーズ.PSD for JavaのGraphics APIを使用してPSDファイルのレイヤーを編集する方法が成功しました。イメージ編集機能を向上させるために、アスポーズ.PSDライブラリのさらなる機能と機能をご覧ください。

完全な例をご確認ください。

## **例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}
