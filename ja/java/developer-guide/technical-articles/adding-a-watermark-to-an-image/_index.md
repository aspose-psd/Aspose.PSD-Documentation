---
title: 画像に透かしを追加する
type: ドキュメント
weight: 20
url: /ja/adding-a-watermark-to-an-image/
---

## **画像に透かしを追加する**
このドキュメントでは、Aspose.PSDを使用して画像に透かしを追加する方法について説明します。画像処理アプリケーションにおいて、画像に透かしを追加することは一般的な要件です。この例では、Graphicsクラスを使用して画像表面に文字列を描画します。
### **透かしの追加**
操作を実証するために、ディスクからBMP画像を読み込み、GraphicsクラスのDrawStringメソッドを使用して透かしとして文字列を画像表面に描画します。また、PngOptionsクラスを使用して画像をPNG形式で保存します。以下は、画像に透かしを追加する方法を示すコード例です。コード例は工程ごとに分割されており、追いやすくなっています。

1. 画像を読み込む
1. Graphicsオブジェクトを作成し初期化する
1. フォントとSolidBrushオブジェクトを作成および初期化する
1. GraphicsクラスのDrawStringメソッドを使用して文字列を透かしとして描画する
1. 画像をPNG形式で保存する

以下のコードスニペットは、画像に透かしを追加する方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **対角線状の透かしの追加**
画像に対角線状の透かしを追加することは、上記で説明した水平方向の透かしを追加するのと似ており、いくつかの違いがあります。操作を実証するために、ディスクからJPG画像を読み込み、Matrixクラスのオブジェクトを使用して変換を追加し、GraphicsクラスのDrawStringメソッドを使用して、画像表面に文字列を透かしとして描画します。以下は、画像に対角線状の透かしを追加する方法を示すコード例です。コード例は工程ごとに分割されており、追いやすくなっています。

1. 画像を読み込む
1. Graphicsオブジェクトを作成し初期化する
1. フォントとSolidBrushオブジェクトを作成および初期化する
1. 画像のサイズをSizeFオブジェクトで取得する
1. Matrixクラスのインスタンスを作成し、複合変換を実行する
1. 変換をGraphicsオブジェクトに割り当てる
1. StringFormatオブジェクトを作成し初期化する
1. GraphicsクラスのDrawStringメソッドを使用して文字列を透かしとして描画する
1. 結果の画像を保存する

以下のコードスニペットは、対角線状の透かしを追加する方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
