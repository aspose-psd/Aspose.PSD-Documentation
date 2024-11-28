---
title: JPEGを介したICCプロファイルを使用したカラースペース変換
type: docs
weight: 60
url: /ja/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **JPEGフォーマットのカラーマネージメント**


この記事では、Aspose.PSD APIを使用してJPEG形式を処理する際にICCプロファイルを使用してカラースペース管理を行う方法について説明します。JPEGの内部カラースペースはYCbCrですが、この[フォーマット](https://reference.aspose.com/psd/net/aspose.psd/pixelformat)はグレースケール、RGB、CMYK、およびYCCKカラースペースを画像のメタデータを格納するために使用することもできます。Aspose.PSD APIは主にRGBスペースで動作するため、APIはJPEGファイルを適切に処理するためにカラースペースの変換を行わなければなりません。グレースケールからRGBおよびYCbCrからRGBへの変換は数学的な変換で行うことができますが、CMYKおよびYCCKスペースは簡単にRGBスペースに変換することができません。

Aspose.PSD APIは、CMYKカラースペースを持つJPEG画像に対して直接RGBからCMYKに変換を行わなければならず、一方、YCCKカラースペースを持つ画像はRGBからCMYKからYCCKに変換する必要があります。CMYKからYCCKへの変換は、ITU-R BT.601変換が最初の3つのチャンネルに適用され、Kチャンネルは変更されないようにします。要するに、Aspose.PSD APIは、CMYKおよびYCCK画像の両方に対してRGBとCMYKカラースペースの相互変換を行わなければならず、そのような変換は基本的に色の特性を説明し、色の変換を助ける見出しテーブルであるICCプロフィールの助けを借りて行われます。


## **ICCプロファイル**
ICC変換メカニズムは、ソースのカラースペースをデバイス非依存のCIELABまたはCIEXYZカラースペースにマッピングする「プロファイル」を使用します。Aspose.PSDは、これらの2つのカラースペースを追加プロファイルと共に使用してデータを必要なカラースペースに変換できます。したがって、ICC変換のためには、ユーザーが2つのプロファイルを提供する必要があります。RGBプロファイルを使用して内部CIEカラースペースに到達し、CMYKプロファイルを使用してCMYKカラー特性を取得します。CMYKからRGBへの変換を実現するためには、プロファイルを交換する必要があります。つまり、ソースプロファイルとしてCMYKプロファイルを使用し、デスティネーションプロファイルとしてRGBプロファイルを使用します。
## **ICCプロファイルを使用したJPEGのためのカラー変換**
Aspose.PSD APIは詳細を隠蔽し、[JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)クラスを介してお使いのICCプロファイルを指定するための簡単なメカニズムを提供します。さらに、Aspose.PSDは、SWOP、CMYK、およびsRGBのサンプルプロファイルをコアに埋め込んでいるため、一般的な使用ケースではユーザーは特定のプロファイルを探す必要はありません。このような補正の欠点はありますが、RGBからCMYKからRGBへの変換後に同じ色を期待することはできないため、こうしたカラースペース変換は不可逆です。互換性のない色空間と異なるカラープロファイルのためです。以下のコードスニペットは、Aspose.PSDを.NET APIで使用してYCCK JPEG画像のためにRGBとCMYKカラープロファイルを指定する方法を示しています。以下の例では、RGBおよびCMYKのカラープロファイルが変更され、画像がYCCKカラースペースに保存されます。これらの[RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile)および[CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile)プロパティは、YCCKカラースペースのピクセルデータを変更するために機能します。他のすべてのカラースペースは、カラーデータを更新するためのカラープロファイルを取得しません。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


プロファイルが設定されていない場合は、Aspose.PSD for .NET APIがデフォルトのプロファイルを使用します。以下の例では、最もJPEGイメージに対してデフォルトのプロファイルプロパティが使用され、宛先カラースペースが変更されます。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
