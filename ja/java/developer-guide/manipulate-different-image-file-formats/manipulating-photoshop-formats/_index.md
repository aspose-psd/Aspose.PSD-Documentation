---
title: Photoshop形式の操作
type: ドキュメント
weight: 10
url: /ja/java/manipulating-photoshop-formats/
---

## **PSDレイヤーの背景色の変更**
Aspose.PSD for Javaを使用すると、PSDファイルの各レイヤーの背景色を変更することができます。PSDレイヤーの背景色を変更するには、Aspose.PSD.FileFormats.Psd.Layers.BackgroundColorクラスを使用してください。次のコードスニペットは、PSDファイルをロードし、レイヤーにアクセスし、背景色を更新してPSDファイルを保存する方法を示しています。

## **PSDファイル内のテキストレイヤーの更新**
Aspose.PSD for Javaを使用すると、PSDファイルのテキストレイヤーのテキストを操作することができます。PSDレイヤーのテキストを更新するには、Aspose.PSD.FileFormats.Psd.Layers.TextLayerクラスを使用してください。次のコードスニペットは、PSDファイルをロードし、テキストレイヤーにアクセスし、テキストを更新してAspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateTextメソッドを使用して新しい名前でPSDファイルを保存する方法を示しています。

## **フラットにされたPSDの検出**
Aspose.PSD for Javaを使用すると、指定したPSDファイルがフラットにされたかどうかを検出することができます。この機能を実現するためにAspose.PSD.FileFormats.Psd.PsdImageクラスにIsFlattenプロパティが導入されています。次のコードスニペットは、PSDファイルをロードし、IsFlattenプロパティにアクセスする方法を示しています。

## **PSDレイヤーのマージ**
この記事では、Aspose.PSDを使用してPSDファイル内のレイヤーをマージする方法を示します。以下の例では、既存のPSDファイルがImageクラスのstatic Loadメソッドにファイルパスを渡すことでロードされます。ロードされた後、イメージをPsdImageに変換/キャストします。JpegOptionsクラスのインスタンスを作成し、さまざまなプロパティを設定します。今すぐPsdImageインスタンスのSaveメソッドを呼び出します。次のコードスニペットは、PSDレイヤーをマージする方法を示しています。