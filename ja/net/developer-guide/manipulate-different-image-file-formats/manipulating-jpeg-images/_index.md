---
title: JPEG 画像の操作
type: docs
weight: 30
url: /ja/net/manipulating-jpeg-images/
---

## **ExifData クラスを使用して Jpeg EXIF タグを読み取り、変更する**
ほとんどのデジタルカメラ（スマートフォンを含む）、スキャナーや他の画像を処理するシステムは、画像を EXIF（Exchangeable Image File）情報とともに保存します。 カメラの設定やシーン情報は、カメラによって画像ファイルに記録されます。 EXIF データには、シャッタースピード、写真が撮影された日時、焦点距離、露出補正、測光パターン、フラッシュの使用の有無などが含まれます。 Aspose.Imaging API は、与えられた画像から EXIF 情報を非常に簡単かつ簡単な方法で抽出することを可能にしました。 開発者は、ExifData クラスを使用して画像に EXIF データを書き込んだり、既存の情報を必要に応じて変更することもできます。 Aspose.PSD は、EXIF データの読み取り、書き込み、および変更のための[ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata)クラスを提供しており、[Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums)名前空間にはプロセスで使用される関連する列挙型が含まれています。
### **EXIF データの読み取り**
Aspose.PSD API は、与えられた画像から EXIF データを読み取る手段を提供します。 以下に示されている手順は、ExifData クラスを使用して画像から EXIF 情報を読み取る方法を説明しています。

- ファクトリーメソッド Load を使用して PSD 画像をロードします。
- PSD リソースの中から Jpeg サムネイルを見つけます。
- ExifData クラスのインスタンスを抽出します。

必要な情報を取得し、コンソールに書き込みます。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


また、開発者は、以下のコードスニペットを使用して特定の情報を取得することも可能です。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **EXIF データの書き込みおよび変更**
Aspose.PSD API を使用すると、開発者は画像の新しい EXIF 情報を書き込み、画像の既存の EXIF データを変更できます。 これらのプロセス（書き込みおよび変更）は、画像を読み込んで ExifData クラスのインスタンスに EXIF データを取得することを必要とします。 次に、ExifData クラスによって公開されるプロパティにアクセスしてそれらを適切に設定できます。 操作対象の画像は、通常 PSD サムネイルである Jpeg または Tiff 画像である必要があります。 使用法を示すサンプルコードは以下の通りです:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **PSD リソースからサムネイルを抽出**
サムネイルは写真の縮小版であり、フルフレームの代わりに画像の重要な部分を表示するために使用されます。 一部の画像ファイル（特にデジタルカメラで撮影されたもの）には、ファイルに埋め込まれたサムネイル画像が含まれています。 Aspose.PSD API を使用すると、PSD リソース内のサムネイルを抽出してディスクに別々に保存することができます。 サムネイルリソースには、サムネイルデータを取得できる[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail)プロパティを含む ExifData があります。 以下のコードスニペットは、その使用方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


上記の手法を使用して、他のサポートされているファイル形式にサムネイルを保存します。 BMP や PNG など、他の画像エクスポートオプションを使用してサムネイルデータを他の画像形式にエクスポートしたい場合は、同様の手法を使用してください。


### **JFIF セグメントからのサムネイルの抽出**
PSD サムネイルリソースの ExifData または JFIF セグメントからサムネイルを抽出することも可能です。 以下のコードは、JFIF データまたは ExifData セグメントからのサムネイルデータの抽出方法を示しています:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


上記の手法を使用して、サムネイルを他のサポートされているファイル形式に保存します。 BMP や PNG など、他の画像エクスポートオプションを使用してサムネイルデータを他の画像形式にエクスポートしたい場合は、同様の手法を使用してください。
### **JFIF セグメントにサムネイルを追加**
以下のコードスニペットは、ロードされた PSD 画像の JFIF セグメントにサムネイル画像を追加する JFIF. Thumbnail プロパティの使用方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

JPEG 形式仕様のため、他のセグメントデータを持つサムネイル画像は 65545 バイトを超えることはできません。 大きな画像をサムネイルとして設定する場合、例外が発生する可能性があります。


### **EXIF セグメントにサムネイルを追加**
以下のコードスニペットは、ロードされた PSD 画像の EXIF セグメントにサムネイ ル画像を追加する場合の ExifData.Thumbnail プロパティの使用方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


この場合、Aspose.PSD API はサムネイル画像のサイズを見積もることはできませんが、全体の EXIF データセグメントのサイズを確認することができます。 これは 65535 バイトを超えることはできません。
## **Jpeg EXIF タグの読み取りおよび変更に JpegExifData クラスを使用**
Aspose.PSD API は、Jpeg 画像形式に固有の[JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata)クラスを提供し、EXIF 情報を取得および更新するための手段となっています。 この記事では、JpegExifData クラスの使用方法を示しています。 Aspose.PSD.Exif.JpegExifData クラスは、Jpeg 画像用の EXIF データコンテナとして機能し、次のように標準的な Jpeg EXIF タグを取得する手段を提供します:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **完全な EXIF タグリスト**
上記のコードスニペットは、Aspose.PSD.Exif.JpegExifData クラスが提供するプロパティを使用していくつかの EXIF タグを読み取ります。 これらのプロパティの完全なリストはこちらでご確認いただけます。 以下のコードでは、[System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) クラスを使用してすべての EXIF タグを読み取ります。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **JPEG 画像の自動方向補正**


写真は、カメラを 90°、180°、270°、またはなし（通常の方向）に回転して撮影することがあります。 ほとんどのデジタルカメラは、JPEG 画像の EXIF タグとして画像データとともに方向情報を保存します。 この情報を使用して、画像の方向を正しく補正するために画像を自動的に回転させることができます。 Aspose.PSD API では、JpegImage クラスの AutoRotate メソッドが JPEG 画像の方向を自動的に補正するための手段を提供しています。 以下に、Aspose.PSD for .NET API を使用して AutoRotate メソッドを使用する方法を示します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **JPEG-LS および CMYK, YCCK のサポート**


Aspose.PSD for .NET API は、JPEG-LS で CMYK および YCCK カラーモデルをサポートしています。 以下のコードスニペットは、JPEG-LS のサポートを使用する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **JPEG-LS 画像で 2-7 ビット/サンプルのサポート**


Aspose.PSD for .NET API は、2-7 ビット/サンプル JPEG-LS 画像のサポートを提供しています。 以下のコードスニペットは、JPEG-LS のサポートを使用する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **JPEG 画像の ColorType および CompressionType の設定**




Aspose.PSD for .NET API は、JPEG 画像の Color Type および Compression Type をサポートし、これをグレースケールとプログレッシブ形式に設定します。 以下のコードスニペットは、そのサポートを使用する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





以下のコードスニペットでは、ロードされた PSD 画像の EXIF セグメントにサムネイル画像を追加する ExifData.Thumbnail プロパティの使用方法が示されています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

この場合、Aspose.PSD API はサムネイル画像のサイズを推定できませんが、すべての EXIF データセグメントのサイズをチェックすることができます。 これは 65535 バイトを超えることはできません。

