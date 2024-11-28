---
title: 画像の変換
type: docs
weight: 20
url: /ja/java/converting-images/
---

## **白黒とグレースケールに画像を変換する**
印刷やアーカイブのために、カラー画像を白黒やグレースケールに変換する必要がある場合があります。この記事では、Aspose.PSD for Java APIを使用して、以下の2つの方法を用いてこれを実珅する方法を示します。

- 2値化
- グレースケール化
### **2値化**
2値化の概念を理解するには、2値画像を定義することが重要です。2値画像とは、各ピクセルに対して2つの値だけを持つデジタル画像のことです。通常、2値画像に使用される2つの色は白と黒ですが、他の2つの色を使用することもできます。2値化は、画像を2レベルに変換するプロセスであり、各ピクセルが1ビット（0または1）として格納されることを意味します。Aspose.PSD for Java APIは現在、2つの2値化メソッドをサポートしています。
#### **固定しきい値での2値化**
次のコードスニペットは、固定しきい値を使用した2値化が画像に適用される方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **オツ法しきい値での2値化**
次のコードスニペットは、オツ法しきい値を使用した2値化が画像に適用される方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **グレースケール化**
グレースケール化とは、連続トーン画像を不連続なグレー階調の画像に変換するプロセスです。次のコードスニペットは、グレースケールを使用する方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **GIF画像レイヤーをTIFF画像に変換する**
PSD画像のレイヤーを別のラスターイメージ形式に抽出して変換する必要がある場合があります。Aspose.PSD APIは、PSD画像のレイヤーを別のラスターイメージ形式に抽出および変換する機能をサポートしています。まず、画像のインスタンスを作成し、ローカルディスクからPSD画像を読み込みます。次に、Layerプロパティ内の各レイヤーを反復処理します。その後、ブロックをTIFF画像に変換します。次のコードスニペットは、PSD画像のレイヤーをTIFF画像に変換する方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **CMYK PSDをCMYK TIFFに変換する**
Aspose.PSD for Javaを使用すれば、開発者はCMYK PSDファイルをCMYK tiff形式に変換することができます。この記事では、Aspore.PSDを使用してCMYK PSDファイルをCMYK tiff形式にエクスポートまたは変換する方法を示します。Aspose.PSD for Javaを使用すると、PSD画像を読み込んでTiffOptionsクラスを使用してさまざまなプロパティを設定し、画像を保存またはエクスポートすることができます。次のコードスニペットは、こうした機能をどうやって実珅するかを示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **画像のエクスポート**
Aspose.PSDには、PSDファイル形式を他の形式に変換するための専用クラスが用意されています。このライブラリを使用すると、PSD画像の変換が非常に簡単かつ直感的に行えます。以下は、ImageOptions名前空間にあるこの目的のためのいくつかの専用クラスです。

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Aspose.PSD for Java APIを使用してPSD画像をエクスポートするのは簡単です。必要なのは、ImageOptions名前空間から適切なクラスのオブジェクトだけです。これらのクラスを使用することで、Aspose.PSD for Javaで作成、編集、または単に読み込んだ任意の画像を、サポートされている任意の形式に簡単にエクスポートできます。
## **画像の結合**
この例では、Graphicsクラスを使用して2つ以上の画像を1つの完全な画像に結合する方法を示しています。操作を実証するために、例では新しいPsdImageを作成し、Graphicsクラスによって公開されたDraw Imageメソッドを使用して、画像をキャンバスサーフェスに描画します。Graphicsクラスを使用することで、2つ以上の画像を結合して、結果のイメージが画像の部分間にスペースもページもない完全なイメージとして見えるようにすることができます。キャンバスのサイズは結果のイメージのサイズと同じである必要があります。以下は、Draw Imageメソッドを使用して画像を1つの画像に結合する方法を示すコードの実証です。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **画像の拡大とトリミング**
Aspose.PSD APIを使用すると、画像変換プロセス中に画像を拡大またはトリミングすることができます。デベロッパーは、X座標とY座標を持つ長方形を作成し、長方形ボックスの幅と高さを指定する必要があります。長方形のX、Y、幅、高さは、読み込んだ画像の拡大またはトリミングを示します。画像変換中に画像を拡大またはトリミングする必要がある場合は、次の手順を実行します:

1. RasterImageクラスのインスタンスを作成し、既存の画像をロードします。
1. ImageOptionクラスのインスタンスを作成します。
1. Rectangleクラスのインスタンスを作成し、長方形のX、Y、幅、高さを初期化します。
1. ラスターイメージクラスのSaveメソッドを呼び出し、出力ファイル名、画像オプション、および長方形オブジェクトをパラメーターとして渡します。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **画像にXMPデータを読み書きする**
XMP（Extensible Metadata Platform）はISO標準です。XMPは拡張可能なメタデータの定義および処理のためのデータモデル、シリアライゼーション形式、およびコアプロパティを標準化します。また、XMP情報をJPEGなどの一般的な画像に埋め込み、XMPをサポートしていないアプリケーションでの読み取りを中断することなく、読み込み可能にします。Aspose.PSD for Java APIを使用することで、開発者は画像にXMPメタデータを読み書きできます。この記事では、XMPメタデータを画像から読み取り、画像にXMPメタデータを書き込む方法を示します。
### **XMPメタデータの作成、書き込み、ファイルから読み取り**
XMP名前空間を使用することで、開発者はXMPメタデータオブジェクトを作成し、画像に書き込むことができます。次のコードスニペットは、XMP名前空間に含まれるXmpHeaderPi、XmpTrailerPi、XmpMeta、XmpPacketWrapper、PhotoshopPackage、DublinCorePackageパッケージの使い方を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **マルチスレッド環境で画像をエクスポート**
Aspose.PSD for Javaは現在、マルチスレッド環境での画像変換をサポートしています。Aspose.PSD for Javaは、コードの実行中に最適化されたパフォーマンスを保証し、マルチスレッド環境での操作をサポートします。Aspose.PSD for Javaのすべての画像オプションクラス（BmpOptions、TiffOptions、JpegOptionsなど）は、IDisposableインターフェースを実装しています。そのため、Sourceプロパティが設定されている場合、デベロッパーは画像オプションクラスオブジェクトを適切に破棄する必要があります。次のコードスニペットは、この機能を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSDは、マルチスレッド環境で作業する際にSyncRootプロパティをサポートしています。デベロッパーはこのプロパティを使用して、ソースストリームへのアクセスを同期することができます。次のコードスニペットは、SyncRootプロパティの使用方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

