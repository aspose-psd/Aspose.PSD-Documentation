---
title: JPEG画像の操作
type: docs
weight: 20
url: /ja/java/manipulating-jpeg-images/
---

## **ExifDataクラスを使用してJPEG EXIFタグを読み取り、変更する**

ほとんどのデジタルカメラ（スマートフォンを含む）、スキャナー、および画像を扱う他のシステムは、EXIF（交換可能画像ファイル）情報を含む画像を保存します。カメラの設定やシーン情報は、撮影された画像ファイルにカメラによって記録されます。EXIFデータには、シャッタースピード、撮影日時、焦点距離、露出補正、測光パターン、フラッシュの使用の有無なども含まれます。Aspose.Imaging APIは、与えられた画像から簡単かつ簡単な方法でEXIF情報を抽出することを可能にしました。開発者は、ExifDataクラスを使用して画像にEXIFデータを書き込んだり、既存の情報を必要に応じて変更したりできます。Aspose.Imagingは、ExifDataクラスを提供しており、EXIFデータの読み取り、書き込み、および変更が行われるAspose.PSD.Exif.Enumsネームスペースには、それを処理するために使用される関連する列挙型が含まれています。
### **EXIFデータの読み取り**
Aspose.PSD APIは、指定された画像からEXIFデータを読み取る手段を提供しています。以下に示すステップでは、ExifDataクラスを使用して画像からEXIF情報を読み取る方法を説明しています。

- Loadメソッドを使用してPSDイメージをロードします。
- PSDリソースの中からJPEGサムネイルを見つけます。
- ExifDataクラスのインスタンスを取得します。

必要な情報を取得してそれをコンソールに書き込みます。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}

また、開発者は以下のコードスニペットを使用して特定の情報を取得することもできます。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **EXIFデータの書き込みと変更**
Aspose.PSD APIを使用すると、開発者は画像の新しいEXIF情報を書き込んだり、既存のEXIFデータを変更したりできます。書き込みと変更の両方のプロセスでは、画像のロードとExifDataクラスのインスタンスへのEXIFデータの取得が必要です。その後、ExifDataクラスが公開するプロパティにアクセスしてそれらを適切に設定します。なお、操作対象の画像は通常PSDサムネイルであるJPEGまたはTIFF形式の画像である必要があります。使用法をデモンストレーションするためのサンプルコードは以下の通りです。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **PSDリソースからサムネイルを抽出**
サムネイルは、フレーム全体ではなく写真の一部を表示するために使用される縮小サイズの画像です。一部の画像ファイル（特にデジタルカメラで撮影されたもの）には、ファイルに埋め込まれたサムネイル画像が含まれています。Aspose.PSD APIを使用して、PSDリソースからサムネイルを抽出してディスクに別途保存することができます。サムネイルリソースにはサムネイルデータを取得できるExifData.Thumbnailプロパティが含まれています。以下に提供されたコードスニペットは、その使用方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

上記の方法を使用して、サムネイルを他のサポートされているファイル形式に保存してください。サムネイルデータをBMPやPNGなどの他の画像形式にエクスポートしたい場合は、他の画像エクスポートオプションを使用してください。
### **JFIFセグメントからサムネイルを抽出**
PSDサムネイルリソースのExifDataまたはJFIFセグメントからサムネイルを抽出することも可能です。以下のコードは、JFIFまたはExifDataセグメントからサムネイルデータを抽出する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

上記の方法を使用して、サムネイルを他のサポートされているファイル形式に保存してください。サムネイルデータをBMPやPNGなどの他の画像形式にエクスポートしたい場合は、他の画像エクスポートオプションを使用してください。
### **JFIFセグメントへのサムネイルの追加**
以下のコードスニペットは、ロードされたPSDイメージのJFIFセグメントにサムネイル画像を追加する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

JPEG形式の仕様により、他のセグメントデータと併せてサムネイル画像は65,545バイトを超えることはできません。大きな画像をサムネイルとして設定する場合、例外が発生することがあります。
### **EXIFセグメントへのサムネイルの追加**
以下のコードスニペットは、ロードされたPSDイメージのEXIFセグメントにサムネイル画像を追加する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

この場合、Aspose.PSD APIはサムネイル画像のサイズを見積ることはできませんが、全体のEXIFデータセグメントのサイズを確認できます。これは65,535バイトを超えることはできません。
## **JpegExifDataクラスを使用してJPEG EXIFタグを読み取り、変更する**
Aspose.PSD APIは、JPEG画像形式専用のJpegExifDataクラスを提供しており、EXIF情報を取得および更新するために使用できます。この記事では、JpegExifDataクラスの使用方法を説明します。Aspose.PSD.Exif.JpegExifDataクラスはJPEGイメージ用のEXIFデータコンテナとして機能し、標準のJPEG EXIFタグを取得する手段を提供しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **全EXIFタグの完全なリスト**
上記のコードスニペットは、Aspose.PSD.Exif.JpegExifDataクラスが提供するプロパティを使用していくつかのEXIFタグを読み取ります。これらのプロパティの完全なリストはこちらで利用できます。以下のコードは、System.Reflection.PropertyInfoクラスを使用してすべてのEXIFタグを読み取ります。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **JPEG画像の自動方向補正**
写真はカメラが90°、180°、270°、またはなし（通常の方向）で回転して撮影されることがあります。ほとんどのデジタルカメラは、JPEG画像のEXIFタグとして方向情報を画像データと共に保存します。この情報を使用して、画像の方向を修正して自動回転を行うことができます。Aspose.PSD APIは、JPEG画像の自動方向補正のためのJpegImageクラスのAutoRotateメソッドを提供しています。以下に、Aspose.PSD for Java APIを使用してAutoRotateメソッドをどのように使用するかを示します。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **JPEG-LSのCMYKおよびYCCKサポート**
Aspose.PSD for Java APIは、JPEG-LSにおけるCMYKおよびYCCKカラーモデルのサポートを提供します。以下のコードスニペットは、JPEG-LSのサポートを使用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **JPEG-LS画像における2-7ビットのサンプルのサポート**
Aspose.PSD for Java APIは、2-7ビットのサンプルJPEG-LS画像のサポートを提供します。以下のコードスニペットは、JPEG-LSのサポートを使用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **JPEG画像のColorTypeとCompressionTypeの設定**

Aspose.PSD for Java APIは、JPEG画像のColor TypeとCompression Typeのサポートを提供し、これらをグレースケールとプログレッシブに設定できます。以下のコードスニペットは、そのサポートを使用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}

