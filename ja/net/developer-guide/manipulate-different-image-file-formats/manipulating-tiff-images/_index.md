---
title: TIFF画像の操作
type: docs
weight: 50
url: /ja/net/manipulating-tiff-images/
---

## **異なる設定でフレームを追加**
TIFFは非常に柔軟な形式であり、異なる寸法、圧縮、およびその他の設定で異なるフレームを追加することができます。Aspose.PSDのAPIを使用すると、複雑なドキュメントを作成するのに役立つ任意のサイズのTIFFフレームを追加できます。すべてを均等にするためにフレームを調整する必要がある場合は、以下の手順を実行してください：

- 所望のオプションで新しい空のフレームを作成するか、CreateFrameFromメソッドを使用して出力オプションを指定してソースフレームをコピーする。
- Resizeメソッドを使用してソースフレーム/画像を所望の寸法にリサイズする。
- ソースフレーム/画像のピクセルを新しいフレームに追加する。
- 新しいフレームを出力TIFF画像に追加する。
## **PSD画像のレイヤーをMulti-Page Tiffファイル形式にエクスポート**
PSD画像のレイヤーをMulti-Page TIFFファイル形式にエクスポートする必要がある場合があります。この記事では、Aspose.PSD for .NET APIを使用してこのタスクを実行する方法を示します。まず、ディスクからPSD画像を読み込みます。次に、PSD画像のレイヤーを反復処理し、対応するレイヤーからTiffFrameを作成します。最後に、結果のTiff画像をディスク上の単一ファイルに保存します。
  
  
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **TiffOptionsの設定**
開発者は、[TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)クラスのさまざまなプロパティを調整して、必要な結果を得ることができます。このドキュメントでは、生成画像属性を制御する4つの主要なプロパティに焦点を当てます。

次に、これらのプロパティがリストされています。

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

空のTiffOptions構造を初期化すると、各オプションはデフォルト値に設定されます。たとえば、圧縮はNoneに、BitsPerSampleは1に、PhotometricはMinIsWhiteに設定されます。この形式で保存すると、最終イメージが白黒になり、このようなオプションの組み合わせに対する予想される動作です。カラーの結果を得るには、上記のすべてのプロパティを、所望のカラースペースに対応する値に設定するか、後述の方法でTiffOptions構造を初期化する必要があります。以下に、所望の結果を得るために設定できる想定パラメータ値を示す表を示します。保存するロード/作成画像をTIFFファイル形式にするには、TiffOptionsを介してすべての4つの列を設定する必要があります。

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|パレット|LZW/非圧縮|1/4/8/16 (パレット、カラーモード) シングルチャンネルのみ|None|
|MinIsWhite/MinIsBlack|LZW/非圧縮|1/4/8/16 (グレースケールモード) シングルチャンネルのみ|None|
|パレット|LZW/非圧縮|8 (パレット、カラーモード) シングルチャンネルのみ|Horizontal (LZW同じパターンに対するより高い圧縮が達成されます)|
|MinIsWhite/MinIsBlack|LZW/非圧縮|8 (グレースケールモード) シングルチャンネルのみ|Horizontal (LZW同じパターンに対するより高い圧縮が達成されます)|
|RGB|LZW/非圧縮|[8,8,8] (3つのRGBチャンネル)|None/Horizontal|
|RGB|LZW/非圧縮|[8,8,8,8] (3つのRGBチャンネルおよび追加のアルファチャンネルはTiffOptions.AlphaStorageを介して設定可能) 実際には、追加チャンネルの数をサポートしていますが、各チャンネルは[8,8,8,8,8,8]のように8ビットサイズでなければいけません|None/Horizontal|
すべての4つのプロパティは、画像形式をTiff形式に保存するためにTiffOptionsを介して設定する必要があります。異なる組み合わせを使用する場合、一部のビューアー（Windows Photo Viewerを含む）は、彼らが提供するサポートの制限により、結果の画像をレンダリングできない場合があります。そのような場合は、テストに異なるビューアーを選択してください。
### **TiffOptionsクラス用の事前設定**
利用者の利便性を高め、TiffOptionsインスタンスの誤構成を避けるために、Aspose.PSD for .NET APIは、[TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat)タイプのパラメータを受け入れる別のコンストラクタを公開しています。TiffExpectedFormat列挙から選択した値に基づいて、APIはTiffOptionsインスタンスのすべての必須プロパティを自動的に構成して、所望の結果を生成します。サンプルコードに進む前に、TiffExpectedFormatのフィールドと使用法の詳細を理解するために、以下にTiffExpectedFormatフィールドとその詳細のリストを示します。


- TiffExpectedFormat.Default: Defaultをフィールドに設定すると、TiffOptionsクラスのデフォルトコンストラクタと同様に動作し、圧縮が設定されず、BitsPerPixelが1に設定されて、黒と白の結果が生成されます。他の形式固有のプロパティを所望に従って手動で設定する場合は、このフィールドを使用することが推奨されます。
- TiffExpectedFormat.TiffCcitRle: RLEエンコーディングに特化し、1 BitsPerPixel（白黒）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffCcittFax3: CCITT Fax3エンコーディングに特化し、1 BitsPerPixel（白黒）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffCcittFax4: CCITT Fax4エンコーディングに特化し、1 BitsPerPixel（白黒）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffDeflateBW: Deflate圧縮に特化し、1 BitsPerPixel（白黒）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffDeflateRGB: Deflate圧縮に特化し、RGB（カラー）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffJpegRGB: Jpeg圧縮に特化し、RGB（カラー）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffJpegYCBCR: Deflate圧縮に特化し、YCBCR（カラー）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffLzwBW: LZW圧縮に特化し、1 BitsPerPixel（白黒）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffLzwRGB: LZW圧縮に特化し、RGB（カラー）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffLzwRGBA: LZW圧縮に特化し、RGBA（透過付きカラー）TIFF形式で結果を保存します。
- TiffExpectedFormat.TiffNoCompressionBW: 圧縮されていないTIFF形式に特化し、1 BitsPerPixel（白黒）で結果を保存します。
- TiffExpectedFormat.TiffNoCompressionRGB: 圧縮されていないTIFF形式に特化し、RGB（カラー）で結果を保存します。
- TiffExpectedFormat.TiffNoCompressionRGBA: 圧縮されていないTIFF形式に特化し、RGBA（透過付きカラー）で結果を保存します。


以下のコードスニペットは、TiffOptionsクラスのインスタンスを作成する際のTiffExpectedFormatフィールドの使用法を説明しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **DeflateおよびAdobe Deflate圧縮のサポート**
TIFF（Tagged Image File Format）ファイル形式はさまざまな種類の圧縮をサポートしており、圧縮タイプはファイル内のタグ（整数値）として保存されます。そのような圧縮方法の1つがAdobe Deflate（以前のDeflate）です。Aspose.PSD for .NET APIは、TIFFイメージのエクスポートと作成にこの圧縮方法をサポートしています。
### **Deflate圧縮でTIFFに画像を保存**
ロードされた画像をDeflate/Adobe Deflate圧縮付きのTIFFに変換するのは簡単です。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Adobe Deflate圧縮を使用してTiffImageを作成**
以下のサンプルは、Aspose.PSD for .NET APIを使用して、Adobe Deflate圧縮メソッドを使用してゼロからイメージを作成する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **TIFF画像の圧縮**
Aspose.PSD for .NET APIを使用すると、PSD画像をTIFF画像形式に変換し、結果のTIFF画像の圧縮を変更することができます。APIはまた、画像をTIFF画像内のフレームとしてアーカイブするために異なる画像を保存しながら、画像を最小データサイズに圧縮することもできます。画像の圧縮は、使用される圧縮アルゴリズムに関係なく、ソースデータサイズを減らすことで行うべきです。最良の圧縮比率を達成するために、インデックスカラースペースを使用することができます。以下のコードスニペットは、最高の圧縮を行い、16のインデックスカラーのみを使用し、LZW圧縮アルゴリズムを使用するが、ソースカラーがわずかにディザリングされている場合の最良の圧縮を実行します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}
