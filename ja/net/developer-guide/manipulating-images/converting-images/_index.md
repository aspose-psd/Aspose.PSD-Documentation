---
title: 画像の変換
type: ドキュメント
weight: 20
url: /ja/net/converting-images/
---

## **白黒およびグレースケールへの画像変換**
印刷や保存のために、カラー画像を白黒またはグレースケールに変換する必要がある場合があります。この記事では、Aspose.PSD for .NET APIを使用して、以下の2つの方法でこれを実珅する方法を示します。

- 二値化
- グレースケール化
### **二値化**
二値化の概念を理解するために、バイナリ画像を定義することが重要です。それは各ピクセルに2つの可能な値しか持たないデジタル画像です。通常、バイナリ画像で使用される2つの色は黒と白ですが、他の2つの色も使用できます。 二値化は画像を2値レベルに変換するプロセスであり、各ピクセルが1ビット（0または1）として保存され、0は色の欠如を、1は色の存在を示します。Aspose.PSD for .NET APIは現在、2つの二値化メソッドをサポートしています。
#### **閾値を使用した二値化**
次のコードスニペットは、画像に固定された閾値二値化を適用する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **大津の閾値を使用した二値化**
次のコードスニペットは、画像に大津の閾値二値化を適用する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **グレースケール化**
グレースケール化とは、連続トーン画像を不連続な灰色の階調の画像に変換するプロセスです。次のコードスニペットは、グレースケール化の方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Grayscaling-Grayscaling.cs" >}}
## **GIF画像のレイヤーをTIFF画像に変換**
PSD画像のレイヤーを別のラスター画像形式に抽出および変換する必要がある場合があります。Aspose.PSD APIは、PSD画像のレイヤーを別のラスター画像形式に変換する機能をサポートしています。まず、画像のインスタンスを作成し、ローカルディスクからPSD画像をロードし、次にLayerプロパティ内の各レイヤーを反復処理します。その後、ブロックをTIFF画像に変換します。次のコードスニペットは、PSD画像のレイヤーをTIFF画像に変換する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **CMYK PSDをCMYK TIFFに変換**
Aspose.PSD for .NETを使用すると、開発者はCMYK PSDファイルをCMYK TIFF形式に変換することができます。この記事では、Aspose.PSDを使用してCMYK PSDファイルをCMYK TIFF形式にエクスポート/変換する方法を示します。Aspose.PSD for .NETを使用すると、PSD画像をロードし、[TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)クラスを使用してさまざまなプロパティを設定し、画像を保存またはエクスポートすることができます。次のコードスニペットは、この機能を実珅する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **画像のエクスポート**
Aspose.PSDには、PSDファイル形式を他の形式に変換するための専用クラスが付属しています。このライブラリを使用すると、PSD画像の変換が非常に簡単で直感的になります。以下は、[ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)名前空間でこの目的のために使用されるいくつかの専用クラスです。

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Aspose.PSD for .NET APIを使用してPSD画像をエクスポートすることは簡単です。[ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)名前空間から適切なクラスのオブジェクトが必要です。これらのクラスを使用すると、Aspose.PSD for .NETで作成、編集、ただ読み込まれた任意のイメージを、サポートされているフォーマットに簡単にエクスポートできます。
## **画像の結合**
この例では、Graphicsクラスを使用して2つ以上の画像を1つの完全な画像に結合する方法を示しています。操作をデモンストレーションするために、この例では新しいPsdImageを作成し、Graphicsクラスで公開されているDraw Imageメソッドを使用して、画像をキャンバス表面に描画します。Graphicsクラスを使用すると、2つ以上の画像を結合して、結果画像が画像部分間やページ間にスペースがなく、ページがない完全な1枚のイメージに見えるようにすることができます。キャンバスのサイズは、結果画像のサイズに等しくする必要があります。次に、[DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index)メソッドの使用方法を示すコードデモンストレーションが続きます。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **画像の拡張および切り取り**
Aspose.PSD APIを使用すると、画像変換プロセス中に画像を拡張または切り取ることができます。開発者は、XおよびY座標の長方形を作成し、長方形の幅と高さを指定する必要があります。長方形のX、Y、幅、高さは、ロードされた画像の拡張または切り取りを示すものである必要があります。画像変換中に画像を拡張または切り取る必要がある場合は、次の手順を実行します。

1. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)クラスのインスタンスを作成し、既存の画像をロードします。
1. ImageOptionクラスのインスタンスを作成します。
1. [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle)クラスのインスタンスを作成し、長方形のX、Yおよび幅、高さを初期化します。
1. RasterImageクラスの[Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index)メソッドを呼び出し、出力ファイル名、画像オプション、および長方形オブジェクトをパラメータとして渡します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **画像にXMPデータを読み書きする**
XMP（Extensible Metadata Platform）はISO標準です。XMPはデータモデル、シリアル化形式、および拡張メタデータの定義と処理のためのコアプロパティを標準化しています。また、XMP情報をJPEGなどの一般的な画像に埋め込むためのガイドラインを提供し、XMPをサポートしていないアプリケーションによってその可読性が損なわれることがないようにします。Aspose.PSD for .NET APIを使用すると、開発者は画像にXMPメタデータを読み取ったり書き込んだりすることができます。この記事では、画像からXMPメタデータを読み取り、画像にXMPメタデータを書き込む方法を示しています。
### **XMPメタデータの作成、書き込み、ファイルから読み取り**
Xmp名前空間を使用することで、開発者はXMPメタデータオブジェクトを作成し、画像に書き込むことができます。次のコードスニペットは、[Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp)名前空間に含まれるXmpHeaderPi、XmpTrailerPi、XmpMeta、XmpPacketWrapper、PhotoshopPackage、DublinCorePackageパッケージの使用方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **マルチスレッド環境で画像をエクスポート**
Aspose.PSD for .NETは、マルチスレッド環境で画像を変換することをサポートしています。Aspose.PSD for .NETでは、ソースプロパティが設定されている場合は、すべての[画像オプション](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)クラス（たとえば、BmpOptions、TiffOptions、JpegOptionsなど）がIDisposableインターフェイスを実装しています。したがって、開発者はソースストリームへのアクセスを同期させるためにSyncRootプロパティを使用できます。次のコードスニペットは、SyncRootプロパティの使用方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}

