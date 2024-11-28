---
title: 自動化のためのPSDファイルをテンプレートとして使用する - ビジネスカードケース
type: docs
weight: 10
url: /ja/net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **概要**
この記事では、PSD/PSBファイルがいくつかの既知のテンプレート構造を持つ場合に、[PSDファイル](https://wiki.fileformat.com/image/psd/)内のいくつかのレイヤーをプログラムで更新する必要がある場合によく使用されるケースについて説明しています。これは、異なる人々のために多くの名刺を作成するために使用できます（ビジネスカードケース）。または、PSDファイルを異なる言語に翻訳し、その中のいくつかのグラフィック素材を置き換える必要がある場合にも使用できます。

この記事を読んだ後、以下のことができるようになります：

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **シンプルなケース**
たとえば、既知のレイヤー名を持ついくつかのPSDテンプレートがあるとします。したがって、C#を使用してPSDレイヤーを変更、更新、または置換する必要があります。まず、Aspose.PSDでテンプレートファイルを開く必要があります。

C#を介してPSDファイルを開く方法は？

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

その後、名前でレイヤーを見つける必要があります。これのためのシンプルな実装がここにあります。

PSDファイル内のレイヤーを名前で見つける方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



レイヤーが見つかったら、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)を使用して通常の方法で更新できます。

PSDレイヤーのGraphicsに描画する方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

この場合、新たに読み込んだ[PNG画像](https://wiki.fileformat.com/image/png/)を既存のPSDレイヤーに描画して、古いデータは新しいファイルで失われます。

しかし、テキストも更新する必要がある場合はどうでしょうか？プロセスは似ています。[テキストレイヤー](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)を名前で見つけ、それからプログラムでPhotoshopファイルの[テキストレイヤーを更新](/psd/ja/net/render-text-with-different-colors-in-text-layer/)します。

C#を使用してPhotoshopでテキストレイヤーを更新する方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



最後に、変更内容を保存する必要があります：

変更されたPSDファイルを保存する方法 - [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



結果の画像：

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **追加機能を備えた複雑なケース**
先ほどは、PSDファイルのレイヤー内の画像を置換する最も簡単な方法を示しました。

しかし、Aspose.PSDには新しいレイヤーを追加したり、古いレイヤーを削除したり、異なるスタイルを使用してテキストレイヤーを更新するなど、さらに複雑な追加機能があります。

置換したい[レイヤー](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer)を見つけ、それからLayersリスト内でそのインデックスを見つけ、その後削除してから、それをJPEGファイル（https://wiki.fileformat.com/image/jpeg/）から新しいレイヤーを作成し、同じ場所に挿入できます。

ファイルから新しいレイヤーを作成し、[Aspose.PSD](https://products.aspose.com/psd/net)を使用してPSDイメージに挿入する方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



このファイルのコードスニペットの最後では、レイヤーの位置を修正し、新しいレイヤーの配列をPsdイメージに保存します。

[PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)レイヤーのプロパティをコピーする方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



そして最後に、既存のPSDイメージ内のテキストレイヤーをC#で更新する必要があります。Aspose.PSDは[TextLayer by Portionsの更新]をサポートしています。([テキストポーション](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion))は、スタイルと段落のプロパティのユニークな組み合わせを持っています。

[PsdImage ](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)レイヤーのプロパティをコピーする方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



その結果、Jpeg、Png、J2k、Bmp、Gif、またはTiffファイルから新しいレイヤーを持つPSDテンプレートをコードで変更し、各行で異なるスタイルの複数行テキストを持つtextを更新しました。

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
