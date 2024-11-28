---
title: PSDファイルを使用してAPI経由でラスターレイヤーマスクを編集する
type: docs
weight: 20
url: /ja/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **概要**
**Adobe® Photoshop®を使用せずにPSD形式の編集とPSDファイルの変更を自動化するには、以下で提供されるAspose.PSD APIを使用できます。PSDファイルを変更するのに役立つC#および.NETコードスニペットがあります。**

Aspose.PSDでは、PSDのレイヤーマスクとベクトルマスクを使用して、レイヤーピクセルを永久的に削除することなく非表示および表示することができます。ラスターマスクはレイヤーマスクまたはユーザーマスクとも呼ばれます。Aspose.PSDでのラスターマスクとベクトルマスクの両方へのアクセスは、[LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata)レイヤープロパティを介して提供され、これは'LayerMaskData'クラスの抽象クラスの子クラスである'[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)'および'[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)'クラスのインスタンスである可能性があります。レイヤーにラスターマスクとベクトルマスクの両方がある場合、[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)インスタンスが提供されます。レイヤーにラスターマスクまたはベクトルマスクのみが含まれる場合、[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)インスタンスが提供されます。LayerMaskDataプロパティがnullの場合、レイヤーにマスクがないか、無効になっているベクトルマスクのみがあります。


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>ラスターマスクおよび無効なベクトルマスク LayerMaskDataShort</p><p>無効なラスターマスク LayerMaskDataShort</p><p>ラスターマスクおよびベクトルマスク LayerMaskDataFull</p><p>ラスターマスク LayerMaskDataShort</p><p>ベクトルマスク LayerMaskDataShort</p><p>無効なベクトルマスク（ただし、ベクトルリソースが存在する）</p>|
| :- | :- |
## **PSDファイル内のレイヤーラスターマスクを取得する方法**
まず、レイヤーがベクトルマスクとレイヤーマスクの両方を持っているかどうかを調べる必要があります。

以下に示すサンプルコードは、レイヤーラスターマスクを取得する方法を示しています。

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs">}}

それ以外の場合、LayerMaskDataレイヤープロパティのタイプはLayerMaskDataShortです。この場合、Flagsプロパティをチェックしてレイヤーにラスターマスクのみがあるかどうかを確認します。Flagsプロパティは[LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags)を含んでいてはならず、そうでない場合はマスクがベクトルマスクキャッシュである可能性があります。

マスクコードスニペットの取得:

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs">}}

両方のマスクが存在する場合でも、LayerMaskDataFullを抽出し、LayerMaskDataShortに変換してラスターマスクを抽出する必要があります。次のコードはどちらの場合にも使用できます。

PSDからラスターマスクを抽出する

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs">}}
## **PSDファイル内のレイヤーにラスターマスクがあるかどうかを確認する方法**
次のC#コードは、レイヤーにラスターマスクがあるかどうかを確認するのに役立つかもしれません:

ラスターマスクが適用されているかどうかを知る方法 [PSDレイヤー](/psd/ja/net/psd-layer/) 

{{<gist "aspose-com-gists" "8a4d34ce175c4c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs">}}
## **PSDファイル内のレイヤーラスターマスクを削除/追加/更新する方法**
正しく保存するには、単にLayerMaskDataを削除/追加/更新しても十分ではありません。チャネルが更新されないため，正しいレンダリングは可能かもしれませんが，これによりマスクチャネルは変更されません。

削除/追加/更新するために、レイヤーにAddLayerMaskメソッドを使用する必要があります。

これにより、マスクとチャネルの両方が追加/更新されます。

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs">}}

これにより、マスクとチャネルの両方が削除されます。

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs">}}

これにより、マスクとチャネルの両方が削除されます。

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs">}}
## **PSDイメージ内のレイヤーラスターマスクを削除する**
まず、マスクが短いフォーマットにあるかどうかをチェックし、ベクトルではない場合は、ラスターマスクを削除するためにnullを渡してAddLayerMaskメソッドを呼び出すことができます。ただし、フルフォーマットの場合は、フルフォーマットに変換してベクトルマスクのみを残す必要があります。このため、次のC# .NETコードスニペットを使用してレイヤーマスクを削除する方法を示します:

PSDファイルからレイヤーマスクを削除するコードスニペット。

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs">}}
## **PSDイメージ内のレイヤーラスターマスクを更新する**
これは直接的です：マスクが短いフォーマットにある場合は、ImageDataとMaskRectangleを必要に応じて変更する必要があります。それ以外の場合は、[UserMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)および[UserMaskRectangle](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)を変更する必要があります。次のC# .NETコードスニペットは、レイヤーマスクを更新するために使用できます:

C#でPSDレイヤーマスクを更新する

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs">}}

以下は、ラスターマスクを変更する可能性のある例です。これは、レイヤーユーザーマスクを反転させます。

C#でPSDレイヤーマスクを更新する

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs">}}
## **PSDファイル内のレイヤーラスターマスクが存在する場合のベクトルマスクの更新方法**
ユーザーが既にベクトルパスリソースを変更していると想定されます。その後、[AddLayerMask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask)レイヤーメソッドを呼び出すだけで、ベクトルマスクを更新することができます。

C#で[PSDレイヤーのベクトルマスクを更新](/psd/ja/net/layer-vector-mask/)する

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs">}}
## **PSDファイルにレイヤーラスターマスクを追加する**
マスクがない場合は、AddLayerMaskレイヤーメソッドを単純に呼び出すことで、指定されたラスターマスクを追加できます。

マスクに[UserMaskFromRenderingOtherData**](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)フラグがない場合、既にラスターマスクが含まれているため、上記のように更新する必要があります。そうでない場合は、短いフォーマットからフルフォーマットに変換します。そうでない場合はそのまま使用します。次のC# .NETコードスニペットは、レイヤーマスクを追加（更新）するために使用できます:

PSDに新しいレイヤーマスクを追加する

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs">}}

## **レイヤーマスクが有効かどうかを確認する方法**
レイヤーラスターマスクの有効状態を見つけるには、LayerMaskDataShortのFlagsプロパティまたはLayerMaskDataFullのRealFlagsで[LayerMaskFlags.Disabled](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags)フラグの状態をチェックすることができます。レイヤーマスクの有効状態を取得するために使用できる次のC# .NETコードスニペットは次のとおりです:

マスクが有効かどうかを確認する:

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs">}}
## **ラスターレイヤーマスクを有効または無効にする方法**
レイヤーラスターマスクを有効または無効にするには、LayerMaskDataShortのFlagsプロパティまたはLayerMaskDataFullのRealFlagsでLayerMaskFlags.Disabledフラグの状態を変更することができます。次のC# .NETコードスニペットは、レイヤーマスクの有効状態を変更するために使用できます:

ラスターレイヤーマスクの有効または無効化:

{{<gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs">}}
