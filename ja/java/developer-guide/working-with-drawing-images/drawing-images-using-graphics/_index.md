---
title: グラフィックスを使用して画像を描画する
type: ドキュメント
weight: 20
url: /ja/java/drawing-images-using-graphics/
---

## **グラフィックスを使用して画像を描画する**

Aspose.PSDライブラリを使用すると、直線、四角形、円などの単純な形状だけでなく、多角形、曲線、円弧、ベジエ形状などの複雑な形状も描画できます。 Aspose.PSDライブラリは、Aspose.PSDネームスペースに存在するGraphicsクラスを使用してこれらの形状を作成します。 Graphicsオブジェクトは、画像にさまざまな描画操作を行い、画像の表面を変更する責任があります。 Graphicsクラスは、次のようないくつかのヘルパーオブジェクトを使用して形状を拡張します：

- ペン：直線を描画したり、形状の輪郭を描画したり、他の幾何学的表現をレンダリングしたりするためのもの。
- ブラシ：領域がどのように塗りつぶされるかを定義するもの。
- フォント：テキストの文字の形状を定義するもの。
### **Graphicsクラスを使用した描画**
以下は、Graphicsクラスの使用法を示すコード例です。コード例のソースコードはいくつかの部分に分割されており、簡単で追いやすいようにしています。ステップバイステップで、次のように行う方法を示します：

1. 画像を作成する。
1. Graphicsオブジェクトを作成および初期化する。
1. 表面をクリアする。
1. 楕円を描画する。
1. 塗りつぶされた多角形を描画して画像を保存する。
### **プログラミングサンプル**
#### **画像の作成**
画像を作成するには、Creating Filesで説明されている方法のいずれかを使用して画像を作成します。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Graphicsオブジェクトの作成および初期化**
次に、Imageオブジェクトをそのコンストラクタに渡すことで、Graphicsオブジェクトを作成および初期化します。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **表面のクリア**
Graphicsの表面をクリアするには、GraphicsクラスのClearメソッドを呼び出し、パラメータとして色を渡します。このメソッドは、引数として渡された色でGraphicsの表面を塗りつぶします。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **楕円を描画**
Graphicsクラスには、多くの形状を描画したり塗りつぶしたりするためのメソッドが公開されていることに気づくでしょう。Aspose.PSD for Java API Referenceでメソッドの完全なリストが見つかります。Graphicsクラスによって公開されているDrawEllipseメソッドのいくつかのオーバーロードされたバージョンがあります。これらのメソッドは、楕円の周りの境界矩形を定義するために後続のパラメータとして渡されるPenオブジェクトを最初の引数として受け入れます。この例では、望む色でPenオブジェクトを使用して楕円を描画するために、第2パラメータとしてRectangleオブジェクトを受け入れるバージョンを使用します。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **塗りつぶされた多角形を描画**
次に、LinearGradientBrushおよびポイントの配列を使用して多角形を描画します。Graphicsクラスは、FillPolygonメソッドのいくつかのオーバーロードされたバージョンを公開しています。これらすべては塗りつぶしの特性を定義するBrushオブジェクトを最初の引数として受け入れ、第2パラメータとしてポイントの配列を受け入れます。配列内の連続する2つのポイントは、多角形の辺を指定しますのでご注意ください。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **グラフィックスを使用して画像を描画する：完全なソース**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

全てのIDisposableを実装し、アンマネージリソースにアクセスするクラスはきちんと破棄されるように、Usingステートメントでインスタンス化されます。
