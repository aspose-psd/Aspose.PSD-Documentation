---
title: Aspose.PSD for Javaを使用したグループレイヤーの例
weight: 100
type: docs
description: Javaを介してPSDファイルのグループレイヤーの使用
keywords: [レイヤーグループ、グループレイヤー、レイヤーをグループに追加、psd api、java、コードサンプル]
url: ja/java/psd-group-layer/
---

## **概要**

Aspose.PSD for Javaでグループレイヤーを利用することで、PSDイメージ内のレイヤーを効果的に管理・整理する能力が向上します。グループレイヤー、またフォルダレイヤーとも呼ばれるものは、複数のレイヤーを統合し、変換やエフェクトをまとめて適用することを可能にします。

まず、PsdImage.create()メソッドを使用して新しいPSDイメージを作成します。次に、PsdImageオブジェクトのaddLayerGroupメソッドを使用して、新しいLayerGroupオブジェクトを初期化します。グループレイヤーの名前（"Folder"）、挿入インデックス（0）、および表示可否（True）を指定します。

その後、二つのLayerオブジェクトを作成し、setDisplayNameメソッドを使用して表示名を設定します。addLayerメソッドを使用してこれらのレイヤーをグループレイヤーに追加します。

グループ内のレイヤーにアクセスするには、LayerGroupオブジェクトのlayersプロパティを使用します。グループ内の最初と二番目のレイヤーの表示名がそれぞれ「Layer 1」と「Layer 2」であることを確認します。

グループレイヤーを操作したら、修正されたPSDイメージをPsdImageオブジェクトのsaveメソッドを使用して保存します。

これは、Aspose.PSD for Javaを使用してグループレイヤーを操作する際の基本的な例であり、PSDイメージ内でのレイヤーの操作と変換に関する高度な機能を提供しています。グループレイヤーやその他ライブラリの機能を活用する詳細情報や例については、Aspose.PSD for Javaのドキュメントを参照してください。

Aspose.PSD for Javaでグループレイヤーを操作するには、LayerGroupクラスを使用します。以下は、グループレイヤーを作成し、レイヤーを追加し、修正されたPSDイメージを保存する方法を示すコードスニペットです。

完全な例については、次を参照してください。

## **例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}
