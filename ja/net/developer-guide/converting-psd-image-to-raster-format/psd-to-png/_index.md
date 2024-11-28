---
title: C#を使用してPSDファイルをPNGファイルに変換
linktitle: PSDからPNGへ
type: docs
weight: 30
url: /ja/net/psd-to-png/
description: C# .NET Photoshop Manipulation APIは、この記事で提供されるコードを使用して、PSD形式からPNG形式に変換できます。
---

Aspose.PSDは、PSD形式のSDKおよびC# .NET Photoshop操作APIであり、PSD形式からPNG形式に変換できます。

このPSD変換には、次のC#コードを使用する必要があります:

以下に示すサンプルコードは、PSDをPngに変換する方法を示しています:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ConvertPsdToPng-ConvertPsdToPng.cs" >}}

Png形式の圧縮レベルを0から9の間で指定できます。9が最も高い圧縮率です。Pngプログレッシブ圧縮を使用したり、Pngファイルの色の種類を変更したりできます。[Png Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)はPSDエクスポートのあらゆるケースに対して異なるプロパティを持っています。

セミトランスペアレントなAlphaチャンネルを持つPngをサイトや作業で使用するのは良い解決策です。Adobe Photoshopファイルは[Read-Only Mode](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/readonlymode)でピクセルパーフェクトにエクスポートできます。

ここには、[Applied Mask](https://docs.aspose.com/display/psdjava/Apply+Masking)、[Layer with Text](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)、およびTransparent [Fill Color Layer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.filllayers/filllayer)（Aspose.PSDはすべての[Adobe Photoshop Fill Layer](https://docs.aspose.com/display/psdjava/Support+of+Fill+Layers)の種類をサポートしています）を含むエクスポートされたPSDファイルの例があります。また、PSD Shape Layer上での[影響のエフェクト](/ja/net/shadow-effects-in-psd-file/)も確認できます。

![todo:image_alt_text](psd-to-png_1.png)
