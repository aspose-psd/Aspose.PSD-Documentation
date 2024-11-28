---
title: テキストレイヤーの操作
type: docs
weight: 170
url: /ja/net/working-with-text-layers/
---

## **テキストレイヤーの追加**
Aspose.PSD for .NETでは、PSDファイルにテキストレイヤーを追加することができます。PSDファイルにテキストレイヤーを追加する手順は以下の通りです：

- [Imageクラス](https://reference.aspose.com/psd/net/aspose.psd/image)によって公開されているファクトリーメソッド[**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index)を使用してPSDファイルを画像としてロードします。
- テキストと[**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)クラスのインスタンスを受け入れる[**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer)メソッドを呼び出します。
- 結果を保存します。

以下のコードスニペットは、PSDファイルにテキストレイヤーを追加する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}


## **テキストレイヤーの位置設定**
Aspose.PSD for .NETでは、PSDファイルにおけるテキストレイヤーの位置を設定することができます。PSDファイルにおけるテキストレイヤーの位置を設定する手順は以下の通りです：

- [Imageクラス](https://reference.aspose.com/psd/net/aspose.psd/image)によって公開されているファクトリーメソッドLoadを使用してPSDファイルを画像としてロードします。
- テキストレイヤーの左端と上端の位置を指定してAddTextLayerメソッドを呼び出します。
- 結果を保存します。

以下のコードスニペットは、PSDファイルにおけるテキストレイヤーの位置を設定する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **テキストレイヤーからテキストプロパティを取得**
Aspose.PSD for .NETを使用して、PSDテキストレイヤーに含まれる異なる部分のテキストのプロパティを取得および更新することができます。この記事では、テキストレイヤーの段落、スタイル、およびテキストのプロパティを取得および更新する方法を説明します。

以下のコードスニペットは、この要件をどのように実現するかを示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


開発者が[Aspose.PSD for .NET](https://products.aspose.com/psd/net)を使用して[TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer)から異なるテキスト部分のテキストの書式設定を取得する方法を示す別の例が以下に示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **PSDファイル内のテキストレイヤーの更新**
Aspose.PSD for .NETを使用すると、PSDファイルのテキストレイヤーのテキストを操作することができます。PSDファイルのテキストレイヤー内のテキストを更新するには、Aspose.PSD.FileFormats.Psd.Layers.TextLayerクラスを使用してテキストを更新し、[Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index)メソッドを使用します。

以下のコードスニペットは、PSDファイルをロードし、テキストレイヤーにアクセスし、テキストを更新してPSDファイルを新しい名前で保存する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **ランタイムでのテキストレイヤーのサポート**
この記事では、PSDイメージのランタイムでテキストレイヤーを追加する方法を示しています。以下にコードスニペットを示します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
