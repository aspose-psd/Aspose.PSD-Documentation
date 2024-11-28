---
title: 画像を描画するためにGraphicsを使用する
type: docs
weight: 20
url: /ja/net/drawing-images-using-graphics/
---

## **画像を描画するためにGraphicsを使用する**
Aspose.PSDライブラリを使用すると、線、四角形、円などの単純な形状だけでなく、多角形、曲線、円弧、ベジエ形状などの複雑な形状も描画できます。Aspose.PSDライブラリは、Aspose.PSDネームスペースに存在する[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)クラスを使用してこれらの形状を作成します。Graphicsオブジェクトは、異なる描画操作を行い、画像の表面を変更する責任があります。[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)クラスは、次のようなヘルパーオブジェクトの種類を使用して形状を向上させます:

·         ペンは、線を描画したり、形状の輪郭を描いたり、他の幾何学的表現をレンダリングするために使用されます。

·         ブラシは、領域をどのように塗りつぶすかを定義します。

·         フォントは、テキストの文字の形状を定義します。
### **Graphicsクラスを使用して描画する**
以下は[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)クラスの使用を示すコード例です。例のソースコードは、シンプルで理解しやすいように複数の部分に分割されています。ステップバイステップで、例を使用して次のことができます:

1. 画像を作成する。
1. Graphicsオブジェクトを作成して初期化する。
1. 表面を消去する。
1. 楕円を描画する。
1. 塗りつぶされた多角形を描画して画像を保存する。
### **プログラミングサンプル**
#### **画像の作成**
作成方法に関する説明のいずれかを使用して画像を作成してください。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Graphicsオブジェクトの作成と初期化**
次に、画像オブジェクトをGraphicsオブジェクトのコンストラクタに渡してGraphicsオブジェクトを作成および初期化します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **表面を消去する**
[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)クラスのClearメソッドを呼び出してグラフィックス表面を消去し、パラメーターとして色を渡します。このメソッドは、引数として渡された色でGraphics表面を塗りつぶします。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **楕円を描画する**
[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)クラスには、形状を描画および塗りつぶすための多くのメソッドが公開されていることに気付くでしょう。Aspose.PSD for .NET APIリファレンスでメソッドの完全なリストを見つけることができます。Graphicsクラスによって公開されているDrawEllipseメソッドのいくつかのオーバーロードされたバージョンがあります。これらのメソッドはすべて、第1引数としてPenオブジェクトを受け取ります。後のパラメーターは、楕円の周りの境界矩形を定義するために渡されます。この例のために、第2パラメーターとしてRectangleオブジェクトを受け入れるバージョンを使用して、指定した色のPenオブジェクトを使用して楕円を描画してください。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **塗りつぶされた多角形を描画する**
次に、LinearGradientBrushおよびポイントの配列を使用して多角形を描画します。Graphicsクラスには、FillPolygon()メソッドの多くのオーバーロードされたバージョンが公開されています。これらすべては、塗りつぶしの特性を定義するBrushオブジェクトを最初の引数として受け入れます。第2パラメーターは、ポイントの配列です。配列の連続する2つのポイントが多角形の1辺を指定することに注意してください。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Graphicsを使用して画像を描画する: 完全なソース**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

全てのアンマネージドリソースにアクセスするIDisposableを実装するすべてのクラスは、正しく破棄されるようにUsingステートメントでインスタンス化されます。
