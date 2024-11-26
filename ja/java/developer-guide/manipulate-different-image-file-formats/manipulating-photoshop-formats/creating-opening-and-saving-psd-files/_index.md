---
title: PSDファイルの作成、オープン、保存
type: docs
weight: 10
url: /ja/creating-opening-and-saving-psd-files/
---

## **画像をPSD形式にエクスポート**
PSD（Photoshop document）は、画像を操作するためにAdobe Photoshopで使用されるデフォルトのファイル形式です。Aspose.PSDを使用すると、PSDファイルにファイルを読み込んだり、編集したり、保存したりできるため、PhotoShopで開いて編集することができます。この記事では、Aspose.PSDでファイルをPSD形式で保存する方法と、この形式で保存する際に使用できるいくつかの設定について説明します。PsdOptionsは、PSD形式に画像をエクスポートするために使用されるImageOptionsネームスペース内の特殊なクラスです。PSDにエクスポートするには、Imageクラスのインスタンスを作成します。これは、既存の画像ファイル（サムネイルなど）からロードされるか、ゼロから作成されます。この記事では、ゼロから画像を作成する方法が説明されています。以下の例では、画像がゼロから作成されます。作成されてピクセルデータが設定されたら、ImageクラスのSaveメソッドを使用して画像を保存し、2番目の引数としてPsdOptionsオブジェクトを提供します。PsdOptionsクラスのいくつかのプロパティは、高度な変換に設定できます。いくつかのプロパティにはColorMode、CompressionMethod、Versionがあります。Aspose.PSDは、次の圧縮方法をCompressionMethod列挙型を介してサポートしています：

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

以下のカラーモードは、ColorModes列挙型でサポートされています：

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



PSD v4.0、v5.0およびそれ以上のサムネイルリソースなど、追加のリソースを追加できます。また、PSD v4.0およびそれ以上のグリッドやガイドリソースも追加できます。以下のコードは、bmpファイルをゼロから作成し、ピクセルを設定し、RLE圧縮とグレースケールカラーモードでPSDに保存するものです。以下のコードスニペットは、ImageをPSDにエクスポートする方法を示しています。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}

## **PSDレイヤーに画像をインポート**
この記事では、Aspose.PSDを使用してPSDレイヤーに画像を追加またはインポートする方法を示しています。Aspose.PSD APIは、この目標を達成するための効率的で使いやすいメソッドを公開しています。Aspose.PSDは、LayerクラスのDrawImageメソッドを公開しており、PSDファイルに画像を追加/インポートするためにこのメソッドを使用します。DrawImageメソッドには、PSD画像レイヤーを指定する必要があります。PSDレイヤーに画像をインポートする手順は以下の通りです：

- Imageクラスが公開する工場メソッドLoadを使用して画像としてPSDファイルをロードします。
- Layerクラスのインスタンスを作成し、PSD画像レイヤーを割り当てます。
- 追加する画像をロードするか、ゼロから作成します。
- 位置と画像インスタンスを指定してLayer.DrawImageメソッドを呼び出します。
- 結果を保存します。



以下のコードスニペットは、PSDレイヤーに画像をインポートする方法を示しています。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **PSDファイルからサムネイルを作成**
PSDはAdobeのPhotoshopアプリケーションのネイティブドキュメント形式です。Adobe Photoshop（バージョン5.0以降）では、プレビュー表示用のサムネイル情報が含まれるイメージリソースブロックに保存されます。Aspose.PSD APIは、PSDファイルのリソースにアクセスするための使いやすいメカニズムを提供しています。これらのリソースには、サムネイルリソースも含まれ、それを取得して必要に応じてディスクに保存できます。以下のコードスニペットは、PSDファイルからサムネイルを作成する方法を示しています。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **インデックス付きPSDファイルの作成**
Aspose.PSD for Java APIは、ゼロからインデックス付きPSDファイルを作成できます。この記事では、PsdOptionsおよびPsdImageクラスの使用方法を示し、新しく作成されたキャンバス上に図形を描画しながら、インデックス付きPSDを作成する手順を説明します。インデックス付きPSDファイルを作成するには、次の簡単な手順が必要です。

- PsdOptionsクラスのインスタンスを作成し、そのソースを設定します。
- PsdOptionsのColorModeプロパティをColorModes.Indexedに設定します。
- RGB空間から色の新しいパレットを作成し、それをPsdOptionsのPaletteプロパティとして設定します。
- 必要な圧縮アルゴリズムにCompressionMethodプロパティを設定します。
- PsdImage.Createメソッドを呼び出して新しいPSD画像を作成します。
- 必要に応じてグラフィックスを描画したり、他の操作を実行します。
- すべての変更を確定するためにPsdImage.Saveメソッドを呼び出します。


以下のコードスニペットは、インデックス付きPSDファイルを作成する方法を示しています。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}

## **PSDレイヤーをラスターイメージにエクスポート**
Aspose.PSD for Javaを使用すると、PSDファイルのレイヤーをラスターイメージにエクスポートできます。PSDレイヤーを画像にエクスポートするには、Aspose.PSD.FileFormats.Psd.Layers.Layer.Saveメソッドを使用してレイヤーを画像にエクスポートします。次のサンプルコードは、PSDファイルをロードし、各レイヤーをPNG画像にエクスポートする方法を示しています。Aspose.PSD.FileFormats.Psd.Layers.Layer.Saveを使用してすべてのレイヤーをPNG画像にエクスポートした後は、お気に入りのイメージビューアでそれらを開くことができます。以下のコードスニペットは、PSDレイヤーをラスターイメージにエクスポートする方法を示しています。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}
