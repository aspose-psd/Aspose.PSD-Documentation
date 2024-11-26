---
title: 画像にウォーターマークを追加する
type: ドキュメント
weight: 30
url: /ja/net/adding-a-watermark-to-an-image/
---

## **画像にウォーターマークを追加する**
この文書では、Aspose.PSDを使用して画像にウォーターマークを追加する方法について説明します。画像処理アプリケーションで画像にウォーターマークを追加することは一般的な要件です。この例では、Graphicsクラスを使用して画像の表面に文字列を描画します。

### **ウォーターマークの追加**
操作を示すために、ディスクからBMP画像を読み込み、GraphicsクラスのDrawStringメソッドを使用して画像の表面にウォーターマークとして文字列を描画します。PngOptionsクラスを使用して画像をPNG形式で保存します。以下に、画像にウォーターマークを追加する方法を示すコード例があります。この例のソースコードは、追いやすいように複数の部分に分割されています。ステップバイステップで、例は以下のようにどのようにするかを示します。

1. [画像を読み込む](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2)。
1. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)オブジェクトを作成および初期化する。
1. Fontおよび[SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush)オブジェクトを作成および初期化する。
1. Graphicsクラスの[DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring)メソッドを使用して、ウォーターマークとして文字列を描画する。
1. 画像をPNG形式で保存する。

以下のコードスニペットは、画像にウォーターマークを追加する方法を示します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **対角線のウォーターマークの追加**
画像に対角線のウォーターマークを追加することは、上記で説明した水平のウォーターマークを追加することと類似していますが、いくつかの違いがあります。操作を示すために、ディスクからJPG画像を読み込み、Matrixクラスのオブジェクトを使用して変換を追加し、GraphicsクラスのDrawStringメソッドを使用して画像の表面にウォーターマークとして文字列を描画します。以下に、画像に対角線のウォーターマークを追加する方法を示すコード例があります。この例のソースコードは、追いやすいように複数の部分に分割されています。ステップバイステップで、例は以下のようにどのようにするかを示します。

1. 画像を読み込む。
1. Graphicsオブジェクトを作成および初期化する。
1. [Font](https://reference.aspose.com/psd/net/aspose.psd/font)およびSolidBrushオブジェクトを作成および初期化する。
1. [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef)オブジェクト内の画像サイズを取得する。
1. Matrixクラスのインスタンスを作成し、複合変換を行う。
1. 変換をGraphicsオブジェクトに割り当てる。
1. [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat)オブジェクトを作成および初期化する。
1. GraphicsクラスのDrawStringメソッドを使用して、ウォーターマークとして文字列を描画する。
1. 結果画像を保存する。

以下のコードスニペットは、対角線のウォーターマークを追加する方法を示します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
