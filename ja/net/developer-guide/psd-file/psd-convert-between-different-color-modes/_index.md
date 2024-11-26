---
title: PSDさまざまなカラーモードの変換
type: docs
weight: 50
url: /ja/net/psd-convert-between-different-color-modes/
---

Aspose.PSDのサポートされているカラーモードについて、この記事で学ぶことができます。

Aspose.PSDは、例えば、8ビットから16ビットへの変換やその逆をサポートしています。CMYK ICCプロファイル変換や他のビット深度から別のタイプへの変換も可能です。ここでは、PSDファイル内でグレースケールへの変換方法の例を見ることができます。

## **CMYK、RGB、グレースケールからグレースケールカラーモードへの変換**
以下のサンプルコードは、Photoshopを使用せずに、CMYK、RGB、またはグレースケールを変換する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}

## **16ビットPhotoshop画像を8ビットグレースケールモードに変換**
しかし、16ビットのグレースケールPhotoshop画像を8ビットグレースケールモードに変換する必要がある場合はどうすればよいのでしょうか？ 以下のコードスニペットを使用する必要があります。 8ビットはPSDファイルで一般的なビット深度です。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}

## **グレースケールをRGBに変換**
もう1つの複雑なケースは、グレースケールPSD画像をRGB画像に変換する必要がある場合です。

グレースケール画像にはチャンネルが1つしかないのに対して、RGB画像には3つのチャンネルがあります：R - 赤、G - 緑、B - 青。 Aspose.PSDは、グレースケールをRGBに変換することができます。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
