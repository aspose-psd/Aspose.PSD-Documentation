---
title: レイヤーを操作する
type: ドキュメント
weight: 150
url: /ja/net/working-with-layers/
---

## **レイヤーグループの作成**
レイヤーグループは1つ以上のレイヤーで構成され、類似したレイヤーまたは関連するレイヤーを整理するのに役立ちます。Aspose.PSD for .NETを使用して、レイヤーグループを作成することができます。そのために、**PsdImage**クラスに新しいメソッド[**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)が追加され、**レイヤーグループを追加**するために使用できます。

レイヤーグループを作成する手順は以下の通りです：

- 指定した幅、高さ、および画像オプションを使用して、**PsdImage**クラスの画像インスタンスを作成します。
- 指定したグループ名とインデックスで[**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup)を作成します。
- Layerクラスのインスタンスを作成し、PSD画像をそれに割り当てます。
- LayerGroupクラスによって公開されたAddLayerメソッドを使用して作成したレイヤーをレイヤーグループに追加します。
- 結果を保存します。

以下のコードスニペットはレイヤーグループを作成する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **レイヤーの名前変更**
任意の名前を使用できますが、通常の慣行はそのレイヤーにあるオブジェクトや要素の一般的な説明を使用することです。この記事では、Aspose.PSD for .NETを使用してレイヤーの名前を変更する方法を示しています。そのために、**Layer**クラスに表示名を正しく表示するための新しいプロパティ[**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname)が追加されました。Photoshopがレイヤー名を**Name**プロパティを使用して保存すると、韓国語の文字はASCIIでバイト63 '?'として保存されることが観察されています。そのため、レイヤー名を適切に表示したい場合は**DisplayName**プロパティを使用してください。**Name**プロパティは韓国語の文字をサポートしていないためです。

以下のコードサンプルは、レイヤーの名前を変更する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **リンクレイヤーのサポート**
レイヤーをリンクすることは、レイヤーをグループ化することと同じです。2つ以上のレイヤーをリンクすると、リンクされたレイヤーの両方に特定の変更を行うことが可能になります。たとえば、1つのレイヤーに変換を適用すると、他のすべてのリンクされたレイヤーにも適用されます。この記事では、[Aspose.PSD](https://products.aspose.com/psd)を使用してリンクされたレイヤーの取得とリンク解除する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
