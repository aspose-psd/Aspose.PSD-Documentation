---
title: Aspose.PSD for Pythonを使用したグループレイヤーの例
weight: 100
type: docs
description: Pythonを介したPSDファイルのGroup Layerの使用
keywords: [layer group, group layer, add layer to group, psd api, python, code sample]
url: ja/python-net/psd-group-layer/
---

## **概要**

Aspose.PSD for Pythonでグループレイヤーを使用することは、PSD画像内のレイヤーを組織化および操作する強力な機能です。グループレイヤー(フォルダレイヤーとも呼ばれる)は、複数のレイヤーを1つのグループにまとめ、グループ全体に変換や効果を適用する方法を提供します。

この例では、最初にPsdImage.createメソッドを使用して新しいPSDイメージを作成します。それから、PsdImageオブジェクトのadd_layer_groupメソッドを使用して新しいLayerGroupオブジェクトを作成します。グループレイヤーの名前("Folder")、挿入するインデックス(0)、およびグループレイヤーを表示する必要があるかどうかを示すブールフラグを指定します。

次に、2つのLayerオブジェクトを作成し、display_nameプロパティを使用してそれらの表示名を設定します。これらのレイヤーをadd_layerメソッドを使用してグループレイヤーに追加します。

最後に、LayerGroupオブジェクトのlayersプロパティを使用してグループ内のレイヤーにアクセスできます。この例では、グループ内の最初と2番目のレイヤーの表示名がそれぞれ "Layer 1" および "Layer 2" であることをアサートしています。

グループレイヤーを操作した後は、PsdImageオブジェクトのsaveメソッドを使用して変更されたPSDイメージを保存できます。

これは、Aspose.PSD for Pythonを使用してグループレイヤーを操作するための基本的な例です。このライブラリは、PSDイメージ内のレイヤーを操作および変換するためのさらに高度な機能を提供しています。グループレイヤーやその他のライブラリの機能についての詳細や例については、Aspose.PSD for Pythonのドキュメントを参照してください。

Aspose.PSD for Pythonでグループレイヤーを操作するには、LayerGroupクラスを使用します。以下に、グループレイヤーを作成し、レイヤーを追加し、変更されたPSDイメージを保存する方法を示すコードスニペットの例があります。

フルの例を確認してください。

## **例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}
