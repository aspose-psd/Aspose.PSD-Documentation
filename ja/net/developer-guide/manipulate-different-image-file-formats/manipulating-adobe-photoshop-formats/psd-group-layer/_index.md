---
title: Aspose.PSD for C# でグループレイヤーを使用する例
weight: 100
type: docs
description: C#を介したPSDファイルのグループレイヤーの使用
keywords: [レイヤーグループ、グループレイヤー、レイヤーをグループに追加、psd api、C#、csharp、コードサンプル]
url: ja/net/psd-group-layer/
---

## 概要

Aspose.PSD for C# でのグループレイヤーは、PSDファイル内のレイヤーを効率的に整理して操作することを可能にします。フォルダーレイヤーを使用すると、複数のレイヤーをグループ化し、グループ全体に変換や効果を適用することができます。

この例では、`PsdImage.Create` を使用して新しいPSD画像を作成し、その後 `PsdImage` オブジェクトから `AddLayerGroup` を使用して新しい `LayerGroup` オブジェクトを作成します。グループレイヤーは「Folder」という名前が付けられ、インデックス0に挿入され、可視に設定されています。

次に、2つの `Layer` オブジェクトが作成され、それぞれの `DisplayName` プロパティが設定されます。これらのレイヤーは `AddLayer` を使用してグループレイヤーに追加されます。

グループ内のレイヤーには、`LayerGroup` オブジェクトの `Layers` プロパティを介してアクセスできます。この例では、グループ内の最初のレイヤーと2番目のレイヤーの表示名がそれぞれ「Layer 1」と「Layer 2」であることを検証しています。

グループレイヤーを変更した後、更新されたPSD画像は `PsdImage` オブジェクトの `Save` メソッドで保存されます。

この基本的な例は、Aspose.PSD for C# を使用してグループレイヤーと連携する方法を紹介しています。このライブラリは、PSDファイル内のレイヤーを操作および変換するための高度な機能を提供しています。詳細な例や機能については、Aspose.PSD for C# のドキュメントを参照してください。

以下は、Aspose.PSD for C# でのグループレイヤーの使用を示すサンプルコードです。

## 例

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

詳細な情報や例については、[Aspose.PSD for C# ドキュメント](https://docs.aspose.com/psd/ja/)をご覧ください。
