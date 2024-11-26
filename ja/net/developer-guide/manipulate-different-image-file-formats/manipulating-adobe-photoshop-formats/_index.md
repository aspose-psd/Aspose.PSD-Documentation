---
title: Adobe Photoshopフォーマットの操作
type: docs
weight: 20
url: /ja/net/manipulating-adobe-photoshop-formats/
---

## **PSDレイヤーを他のレイヤーに統合**

## **PSDファイルへの画像エクスポート**
PSD、PhotoShop Documentは、Adobe Photoshopが画像を扱うために使用するデフォルトのファイル形式です。Aspose.PSDを使用すると、PSDファイルにファイルをロード、編集、保存して、Photoshopで開いて編集できるようにすることができます。この記事では、Aspose.PSDを使用してファイルをPSD形式で保存する方法と、保存する際に使用できる設定の一部について説明します。[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)は、PSDに画像をエクスポートするために使用される[ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)名前空間の特殊なクラスです。PSDにエクスポートするには、既存の画像ファイル（例：サムネイル）から読み込まれたImageクラスのインスタンスを作成するか、ゼロから作成します。この記事では、以下の例で画像がゼロから作成されます。作成され、ピクセルデータが代入された画像は、ImageクラスのSaveメソッドを使用して保存し、2番目の引数としてPsdOptionsオブジェクトを指定します。PsdOptionsクラスのいくつかのプロパティを設定して高度な変換が行えます。いくつかのプロパティはColorMode、[CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod)、Versionです。Aspose.PSDは、CompressionMethod列挙型を介して以下の圧縮メソッドをサポートしています:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

以下のカラーモードは、[ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes)列挙型を介してサポートされています:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

PSD v4.0、v5.0およびそれ以上のサムネイルリソース、またはPSD v4.0およびそれ以上のグリッドやガイドリソースなど、追加のリソースを追加することができます。以下のコードは、ゼロからImageファイルを作成し、ピクセルを埋め、RLE圧縮およびグレースケールカラーモードでPSDに保存します。以下のコードスニペットでは、画像をPSDにエクスポートする方法を示しています:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}

## **PSDレイヤーに画像をインポート**
この記事では、Aspose.PSDを使用してPSDレイヤーに画像を追加またはインポートする方法を示しています。Aspose.PSDのAPIには、この目標を達成するための効率的で使いやすいメソッドが公開されています。Aspose.PSDは、LayerクラスのDrawImageメソッドを使用してPSDファイルに画像を追加/インポートする機能を公開しています。DrawImageメソッドには、PSDファイルに画像を追加/インポートするための場所と画像の値が必要です。PSDレイヤーに画像をインポートする手順は以下のとおりです:

- Imageクラスによって公開されるLoadファクトリメソッドを使用して画像としてPSDファイルをロードします。
- Png、Jpeg、Tiff、Gif、Bmp、Psdまたはj2kファイルを使用してレイヤークラスのインスタンスを作成します。
- Layerクラスを使用してLayerをPsdに追加します。
- 結果を保存します。

以下のコードスニペットは、画像をPSDレイヤーにインポートする方法を示しています:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

## **PSDレイヤーでの色の置き換え**
この記事では、Aspose.PSDを使用してPSDレイヤーに画像を追加またはインポートする方法を示しています。Aspose.PSDのAPIには、この目標を達成するための効率的で使いやすいメソッドが公開されています。Aspose.PSDは、レイヤークラスのDrawImageメソッドを使用してPSDファイルに画像を追加/インポートする機能を公開しています。DrawImageメソッドには、画像が追加されるPSDファイルでの場所と画像インスタンスが指定されます。PSDレイヤーに画像をインポートする手順は以下のとおりです:

- Imageクラスによって公開されるLoadファクトリメソッドを使用して画像としてPSDファイルをロードします。
- レイヤークラスのインスタンスを作成し、PSDイメージレイヤーをそれに割り当てます。
- 追加する画像をロードするか、ゼロから作成します。
- 位置と画像インスタンスを指定してLayer.DrawImageメソッドを呼び出します。
- 結果を保存します。

以下のコードスニペットは、PSDレイヤーに画像をインポートする方法を示しています:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}

## **PSDファイルからサムネイルを作成**
PSDはAdobeのPhotoshopアプリケーションの固有のドキュメント形式です。Adobe Photoshop（バージョン5.0以降）は、プレビュー表示用のサムネイル情報を画像リソースブロックに保存します。このリソースには、初期の28バイトのヘッダーと、RGB（赤、緑、青）の順でJFIFサムネイルが含まれます。Aspose.PSD APIは、PSDファイルのリソースにアクセスするための使いやすいメカニズムを提供しています。これらのリソースにはサムネイルリソースも含まれ、アプリケーションのニーズに応じて取得してディスクに保存することができます。以下のコードスニペットは、PSDファイルからサムネイルを作成する方法を示しています:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}

## **インデックス化PSDファイルの作成**
Aspose.PSD for .NET APIを使用して、ゼロからインデックス化されたPSDファイルを作成できます。この記事では、PsdOptionsおよび[PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage)クラスを使用して、新しく作成されたキャンバスに図形を描画しながらインデックス化されたPSDを作成する方法を示しています。インデックス化されたPSDファイルを作成するには、以下の簡単な手順が必要です:

- PsdOptionsのインスタンスを作成し、そのソースを設定します。
- PsdOptionsのColorModeプロパティをColorModes.Indexedに設定します。
- RGBスペースからカラーパレットを作成し、PsdOptionsのPaletteプロパティとして設定します。
- CompressionMethodプロパティを必要な圧縮アルゴリズムに設定します。
- PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create)メソッドを呼び出して新しいPSDイメージを作成します。
- グラフィックスを描画したり、他の操作を行います。
- すべての変更を確定するためにPsdImage.Saveメソッドを呼び出します。

以下のコードスニペットは、インデックス化されたPSDファイルの作成方法を示しています:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}

## **PSDレイヤーをラスター画像にエクスポート**
Aspose.PSD for .NETを使用すると、PSDファイル内のレイヤーをラスター画像にエクスポートできます。レイヤーを画像にエクスポートするには、[Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index)メソッドを使用してレイヤーを画像にエクスポートします。次のサンプルコードは、PSDファイルをロードし、そのレイヤーをAspose.PSD.FileFormats.Psd.Layers.Layer.Saveを使用してPNG画像にエクスポートする方法を示しています。すべてのレイヤーがPNG画像にエクスポートされたら、お好みの画像ビューアを使用してそれらを開くことができます。以下のコードスニペットは、PSDレイヤーをラスター画像としてエクスポートする方法を示しています:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}

## **PSDファイルのテキストレイヤーの更新**
Aspose.PSD for .NETを使用すると、PSDファイルのテキストレイヤー内のテキストを操作できます。PSDレイヤー内のテキストを更新するには、[Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)クラスを使用してPSDレイヤーのテキストを更新し、[Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index)メソッドを使用して新しい名前でPSDファイルを保存します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **フラット化されたPSDを検出**
Aspose.PSD for .NETを使用すると、特定のPSDファイルがフラット化されているかどうかを検出できます。Aspose.PSD.FileFormats.Psd.PsdImageクラスのIsFlattenプロパティがこの機能を実現するために導入されました。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}

## **PSDレイヤーをマージ**
This article shows how to merge layers in a PSD file while converting a PSD file to JPG with Aspose.PSD. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Once it is loaded, convert/cast the image to PsdImage. Create an instance of the JpegOptions class and set it various properties. Now call the Save method of the PsdImage instance. The following code snippet shows you how to merge PSD layers.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}

## **PSDファイルでのGrayscale with Alphaのサポート**
This article shows how to support Grayscale with Alpha for PSD file while converting a PSD file to PNG with Aspose.PSD. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Once it is loaded, convert/cast the image to PsdImage. Create an instance of the PngOptions class and set its various properties. Set the [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) property to TruecolorWithAlpha. Now call the Save method of the PngOptions instance. The following code snippet shows you how to convert to Grayscale PNG with Alpha.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.cs" >}}

## **PSDレイヤー効果のサポート**
This article shows how to support different effects like **Blur**, **Inner** **Glow**, **Outer Glow** for PSD layer. The following code snippet shows you how to support layer effects.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.cs" >}}
