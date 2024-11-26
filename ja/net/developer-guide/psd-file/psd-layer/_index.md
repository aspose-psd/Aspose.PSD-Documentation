---
title: PSD レイヤー
type: docs
weight: 70
url: /ja/net/psd-layer/
---

## **概要**
Adobe® Photoshop® PSD レイヤーは、グラフィック処理における最良のコンセプトの一つです。レイヤーにはピクセルに関する情報が含まれ、異なるチャネル数を持つことができます。

Photoshop ドキュメント内のレイヤーの最も重要な部分の1つは、レイヤーリソースです。PSD からの[レイヤーリソースのリスト](/psd/ja/net/list-of-psd-layer-resources/)は当社のドキュメントでご確認いただけます。

次のスクリーンショットに、レイヤーを操作するための UI が表示されています:

![todo:image_alt_text](psd-layer_1.png)

しかし、Aspose.PSD は[Aspose.PSD+for+Java+Home](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home)を介した PSD レイヤーのプログラム的操作に特化しています。

追加のドキュメントはこの記事で見つけることができます: [画像の操作](/psd/ja/net/manipulating-images-html/)。すべての操作は PSD プレビューとレイヤーに処理され、詳細は[Aspose.PSD ラスター画像 API リファレンス](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)でご確認いただけます。
## **利用可能な PSD レイヤー API**
- レイヤーエフェクト
- レイヤー共通プロパティ
- レイヤーのメタデータ
## **C# を使用したレイヤー編集の例**
### **新しいレイヤーの追加**
開いた[PSD ファイル](/psd/ja/net/psd-file/)に空のレイヤーを追加したい場合は、次のコードを使用できます。

API を使用して PSD ファイルに新しいレイヤーを追加

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}
### **JPEG、PNG、GIF、AI、TIFF、BMP ファイルからの新しいレイヤーの追加**
任意の[サポートされているフォーマット](/psd/ja/net/supported-file-formats/)のファイルを画像に新しいレイヤーとして追加できます。ただし、直接読み込むことはできません。

以下のコードを使用して、任意のサポートされている形式のファイルから新しい PSD レイヤーをストリームから追加できます

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
### **すべてのレイヤーまたはレイヤーグループをフラット化する**
ユーザーに編集可能な PSD ファイルを提供したくない場合に便利です。また、API を通じてファイルがフラット化されたかどうかを識別できます。

PSD ファイルのレイヤーフラット化:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}
