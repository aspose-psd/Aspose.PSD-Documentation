---
title: TIFF画像の操作
type: docs
weight: 40
url: /ja/java/manipulating-tiff-images/
---

## **異なる設定でフレームを追加**
TIFFは非常に柔軟なフォーマットであり、異なるフレームを異なる寸法、圧縮およびその他の設定で追加することができます。Aspose.PSDのAPIを使用すると、複雑なドキュメントの作成に役立つ任意のサイズのTIFFフレームを追加できます。追加プロセス中にフレームをすべて均等にする必要がある場合、次の手順を実行します：

- 望ましいオプションで新しい空のフレームを作成するか、CreateFrameFromメソッドを使用して出力オプションが指定されたソースフレームをコピーします。
- Resizeメソッドを使用してソースフレーム/画像を望ましい寸法にリサイズします。
- ソースフレーム/画像のピクセルを新しいフレームに追加します。
- 新しいフレームを出力TIFF画像に追加します。

## **PSD画像のレイヤーをマルチページTIFFファイル形式にエクスポート**
PSD画像のレイヤーをマルチページTIFFファイル形式にエクスポートする必要があることがあります。この記事では、Aspose.PSD for Java APIを使用してこのタスクを実行する方法を示します。まず、ディスクからPSD画像をロードします。次に、PSD画像のレイヤーを繰り返し処理し、対応するレイヤーからTiffFrameを作成します。最後に、結果のTIFF画像をディスク上の単一ファイルに保存します。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **TiffOptionsの構成**


開発者はTiffoptionsクラスの異なるプロパティを調整して、望ましい結果を得ることができます。このドキュメントでは、結果画像の属性を制御する4つの主要なプロパティに焦点を当てます。

以下にこれらのプロパティをリストします。

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

空のTiffoptions構造体を初期化すると、各オプションはデフォルト値に設定されます。たとえば、圧縮はNoneに設定され、BitsPerSampleは1に設定され、PhotometricはMinIsWhiteに設定されます。この形式で保存すると、最終的な画像は白黒になります。これはこのようなオプションの組み合わせの期待される動作です。カラーの結果を得るには、上記に記載されたプロパティすべてを望ましいカラースペースに対応する値に設定するか、後述の記事で説明されている事前定義の設定でTiffoptions構造体を初期化する必要があります。以下に、望ましい結果を達成するために設定できる想定パラメータ値を説明する表が示されています。望ましい結果を達成するには、Tiffoptionsを介してすべての4つの列を設定する必要があります。

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/非圧縮|1/4/8/16（パレット、カラーモード）単一チャネルのみ|None|
|MinIsWhite/MinIsBlack|LZW/非圧縮|1/4/8/16（グレースケールモード）単一チャネルのみ|None|
|Palette|LZW/非圧縮|8（パレット、カラーモード）単一チャネルのみ|Horizontal（LZWに対して同じパターンでより多くの圧縮が実現されます）|
|MinIsWhite/MinIsBlack|LZW/非圧縮|8（グレースケールモード）単一チャネルのみ|Horizontal（LZWに対して同じパターンでより多くの圧縮が実現されます）|
|RGB|LZW/非圧縮|[8,8,8]（3つのRGBチャネル）|None/Horizontal|
|RGB|LZW/非圧縮|[8,8,8,8]（3つのRGBチャネルと追加のアルファチャネルはTiffOptions.AlphaStorageを介して設定できます）実際には、追加のチャネル数はサポートされていますが、各チャネルは[8,8,8,8,8,8]のように8ビットのサイズでなければなりません|None/Horizontal|
すべての4つのプロパティはTiffOptionsを介して設定する必要があります。異なる組み合わせを使用すると、一部のビューア（Windows Photo Viewerを含む）は限られたサポートしか提供しないため、結果の画像をレンダリングできない場合があります。そのような場合は、テスト用に異なるビューアを選択してください。
### **TiffOptionsクラスの事前定義された設定**
ユーザーの利便性を図り、Tiffoptionsインスタンスの誤構成を回避するために、Aspose.PSD for Java APIはTiffExpectedFormat型のパラメータを受け入れる別のコンストラクタを公開しています。TiffExpectedFormat列挙から選択した値に基づいて、APIは所望の結果を生成するためにTiffoptionsインスタンスのすべての必須プロパティを自動設定します。サンプルコードに移る前に、使用方法をよりよく理解するために、TiffExpectedFormatフィールドとその詳細の一覧が以下に示されています。



- TiffExpectedFormat.Default: Defaultフィールドを設定すると、他のフォーマット固有のプロパティを望ましい結果に従って手動で設定する場合に、Tiffoptionsクラスのデフォルトコンストラクタと同様に機能します。必要に応じて他のフォーマット固有のプロパティを手動で設定する場合は、このフィールドを使用することが推奨されます。
- TiffExpectedFormat.TiffCcitRle: 結果を1ビットパーピクセル（白黒）TIFF形式で保存する際に、RLEエンコーディングに特化したものです。
- TiffExpectedFormat.TiffCcittFax3: 結果を1ビットパーピクセル（白黒）TIFF形式で保存する際に、CCITT Fax3エンコーディングに特化したものです。
- TiffExpectedFormat.TiffCcittFax4: 結果を1ビットパーピクセル（白黒）TIFF形式で保存する際に、CCITT Fax4エンコーディングに特化したものです。
- TiffExpectedFormat.TiffDeflateBW: 結果を1ビットパーピクセル（白黒）TIFF形式で保存する際に、Deflate圧縮に特化したものです。
- TiffExpectedFormat.TiffDeflateRGB: 結果をRGB（カラー）TIFF形式で保存する際に、Deflate圧縮に特化したものです。
- TiffExpectedFormat.TiffJpegRGB: 結果をRGB（カラー）TIFF形式で保存する際に、Jpeg圧縮に特化したものです。
- TiffExpectedFormat.TiffJpegYCBCR: 結果をYCBCR（カラー）TIFF形式で保存する際に、Deflate圧縮に特化したものです。
- TiffExpectedFormat.TiffLzwBW: 結果を1ビットパーピクセル（白黒）TIFF形式で保存する際に、LZW圧縮に特化したものです。
- TiffExpectedFormat.TiffLzwRGB: 結果をRGB（カラー）TIFF形式で保存する際に、LZW圧縮に特化したものです。
- TiffExpectedFormat.TiffLzwRGBA: 結果をRGBA（透過付きカラー）TIFF形式で保存する際に、LZW圧縮に特化したものです。
- TiffExpectedFormat.TiffNoCompressionBW: 結果を1ビットパーピクセル（白黒）に保存する際に、非圧縮TIFF形式に特化したものです。
- TiffExpectedFormat.TiffNoCompressionRGB: 結果をRGB（カラー）に保存する際に、非圧縮TIFF形式に特化したものです。
- TiffExpectedFormat.TiffNoCompressionRGBA: 結果をRGBA（透過付きカラー）に保存する際に、非圧縮TIFF形式に特化したものです。



以下のコードスニペットは、Tiffoptionsクラスのインスタンスを作成する際にTiffExpectedFormatフィールドの使用法を詳しく説明しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **DeflateおよびAdobe Deflate圧縮のサポート**
TIFF（Tagged Image File Format）ファイル形式はさまざまな種類の圧縮をサポートしており、圧縮タイプはファイル内のタグ（整数値）として保存されます。そのような圧縮方法の1つがAdobe Deflate（以前はDeflateとして知られていた）です。Aspose.PSD for Java APIは、TIFF画像のエクスポートおよび作成にこの圧縮方法をサポートしています。
### **Deflate圧縮を使用してTIFFへ画像を保存**
ロードされた画像をDeflate/Adobe Deflate圧縮を使用してTIFF形式に変換することは次のとおりです。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Adobe Deflate圧縮を使用してTiffImageを作成**
以下に示すサンプルは、Aspose.PSD for Java APIを使用してAdobe Deflate圧縮を使用してスクラッチから画像を作成する方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **TIFF画像の圧縮**
Aspose.PSD for Java APIを使用してPSD画像をTIFF画像形式に変換し、結果のTIFF画像の圧縮を変更することができます。APIはまた、イメージをアーカイブ目的でTIFFイメージのフレームとして保存し、画像を最小のデータサイズに圧縮することもできます。いかなる場合でも、画像の圧縮は、使用される圧縮アルゴリズムにかかわらず、ソースデータサイズを減らすことで実行する必要があります。最高の圧縮比を達成するには、インデックスカラースペースを使用することができます。以下のコードスニペットは、16色のインデックスしか使用せずに最高の圧縮を実行し、ただしソースカラーはわずかにディザリングされている場合の最適な圧縮を実行します。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
