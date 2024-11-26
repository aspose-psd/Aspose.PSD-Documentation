---
title: GraphicsPathを使用した画像の描画
type: ドキュメント
weight: 30
url: /ja/java/drawing-images-using-graphicspath/
---

## **GraphicsPathを使用した画像の描画**
GraphicsPathクラスは、グラフィックスパスの作成とメンテナンスを担当しています。GraphicsPathには画像への参照がなく、画像自体は変更しません。代わりに、Graphicsクラスが描画できるパスを記述するメタデータを含むオブジェクトと考えることができます。GraphicsPathクラスはフィギュアを使用します。各フィギュアは、連結された線や曲線のシーケンス、または幾何学的形状プリミティブで構成されています。各形状は形状セグメントに分割できます。GraphicsPathオブジェクトに異なるフィギュアや形状を追加、削除、変更することができます。GraphicsPathを完全に記述した後は、対応するGraphicsクラスのメソッド（DrawPathおよびFill Paths）を使用して、パスを描画または塗りつぶすことができます。Graphicsクラスは各形状セグメントを取り、最終的な画像を生成します。

### **GraphicsPathクラスを使用した描画**
以下は、GraphicsPathクラスの使用を示す例です。例のソースコードはいくつかの部分に分割されており、シンプルで追いやすくなるようにしています。段階的に、例では以下の方法を示しています：

- 画像を作成する。
- Graphicsオブジェクトを初期化する。
- 表面をクリアする。
- GraphicsPathのインスタンスを作成する。
- フィギュアを作成する。
- フィギュアに形状を追加する。
- フィギュアの配列を作成する。
- パスを描画する。
- パスを塗りつぶす。


### **GraphicsPathを使用した画像の描画：プログラミングサンプル**
#### **GraphicsPath：画像を作成する**
画像を作成するには、Creating Filesで説明される方法のいずれかを使用して開始します。
#### **GraphicsPath：Graphicsオブジェクトを初期化する**
Imageオブジェクトをそのコンストラクタに渡すことで、Graphicsオブジェクトを作成および初期化します。
#### **GraphicsPath：表面をクリアする**
GraphicsクラスのClearメソッドを呼び出して、グラフィックス表面をクリアします。このメソッドは、引数として渡された色でグラフィックス表面を塗りつぶします。
#### **GraphicsPath：GraphicsPathのインスタンスを作成する**
GraphicsPathのインスタンスを作成し、デフォルトでGraphicsPathがAlternateに設定されているようにします。このモードは、閉じた図形の内部をどのように塗りつぶすかを決定します。他の可能なGraphicsPath値はWindingです。
#### **GraphicsPath：フィギュアを作成する**
Figureクラスのインスタンスを作成します。前述のように、FigureにはShapesを含めることができ、shapesはAspose.PSD.Shapes名前空間に存在します。
#### **GraphicsPath：フィギュアに形状を追加する**
Figureクラスが公開するAdd Shapesメソッドを使用すると、フィギュアに形状を追加できます。以下のコード例では、複数の形状がFigureオブジェクトに追加されています。
#### **GraphicsPath：配列にフィギュアを追加する**
複数のフィギュアをパラメータとして受け入れるAddFiguresメソッドを使用して、GraphicsPathオブジェクトにフィギュアを追加できます。
#### **GraphicsPath：パスを描画する**
Graphicsクラスが公開するDrawPathメソッドを使用して、GraphicsPathを描画します。このメソッドは2つのパラメータを受け入れます。最初のパラメータはPenクラスのオブジェクトであり、パスの色、幅、スタイルを決定します。2番目のパラメータは、パス自体を表すGraphicsPathクラスのオブジェクトです。
#### **GraphicsPath：パスを塗りつぶす**


GraphicsPathオブジェクトをFill Pathsメソッドに渡すことで、パスを塗りつぶすことができます。Fill Pathsメソッドは、現在パスに設定されている塗りつぶしモード（alternateまたはwinding）に従ってパスを塗りつぶします。パスに開いたフィギュアがある場合は、それらのフィギュアが閉じられているかのようにパスが塗りつぶされます。

Fill Pathsメソッドは2つのパラメータを受け入れます。最初のパラメータは、Aspose.PSD.Brushes名前空間からの任意のブラシクラスのオブジェクトです。2番目のパラメータはパス自体です。この例では、前提として、HatchBrushを使用します。HatchBrushは、斜線スタイル、前景色、背景色を持つ矩形状のブラシです。HatchBrushオブジェクトをFill Pathsメソッドに渡す前に、プロパティを設定してください。
### **GraphicsPath：完全なソース**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}

IDisposableを実装しているすべてのクラスは、正しく破棄されるように、Usingステートメント内でインスタンス化されます。
