---
title: 回転テキストレイヤーのレンダリング
type: docs
weight: 40
url: /ja/net/rendering-of-rotated-text-layers/
---

## **回転テキストレイヤーのレンダリング**
Aspose.PSD は、回転したテキストレイヤーをレンダリングする機能を提供します。以下の例では、既存の PSD ファイルを Image クラスの static Load メソッドにファイルパスを渡してロードします。続けて、[PsdImage](https://reference.aspose.com/psd/net/aspose.psd/fileformats.psd/psdimage) インスタンスの [Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) メソッドを呼び出します。

以下のコードスニペットでは、回転した[Text layer](https://reference.aspose.com/psd/net/aspose.psd/fileformats.psd/layers/textlayer)をレンダリングする方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfRotatedTextLayer-RenderingOfRotatedTextLayer.cs" >}}
## **ベクトルマスクとテキストレイヤーの回転**
Aspose.PSD は、ベクトルマスクとテキストレイヤーを回転する機能を提供します。Aspose.PSD は、ベクトルマスクとテキストレイヤーを回転するための RotateFlip メソッドを公開しています。レイヤーを回転する手順は以下の通りです：

- Image クラスによって公開された factory メソッド Load を使用して画像として PSD ファイルをロードします。
- 必要な [RotateFlipType](https://reference.aspose.com/psd/net/aspose.psd/rotatefliptype) を設定します。
- [RotateFlip](https://reference.aspose.com/psd/net/aspose.psd/image/methods/rotateflip) メソッドを呼び出します。
- 結果を保存します。

以下のコードスニペットでは、ベクトルマスクとテキストレイヤーを回転する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfRotateLayer-SupportOfRotateLayer.cs" >}}
