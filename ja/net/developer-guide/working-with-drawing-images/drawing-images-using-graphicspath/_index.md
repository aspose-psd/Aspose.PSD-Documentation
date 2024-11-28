---
title: GraphicsPathを使用した画像の描画
type: ドキュメント
weight: 30
url: /ja/net/drawing-images-using-graphicspath/
---

## **GraphicsPathを使用した画像の描画**
[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) クラスは、グラフィックス パスの作成と維持を担当しています。GraphicsPath はイメージに対する参照を持っておらず、イメージ自体を変更することはせず、代わりに、Graphics クラスが描画できるパスを記述するメタデータを含むオブジェクトと見なすことができます。GraphicsPath クラスは、各図形が連結した線および曲線のシーケンスまたは幾何学的形状のプリミティブから構成される、図形を使用します。各形状は形状セグメントに分割できます。GraphicsPath オブジェクトに異なる図形や形状を追加、削除、変更できます。GraphicsPath が完全に記述されたら、対応する Graphics クラスのメソッド（DrawPath および Fill Paths）を使用して、パスを描画するか塗りつぶすことができます。Graphics クラスは、各形状セグメントを取り、最終的なイメージを生成するためにそれを描画します。

### **GraphicsPath クラスを使用した描画**
以下は、[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) クラスの使用を示す例です。例のソースコードは、単純で追いやすいように複数の部分に分割されています。ステップ バイ ステップで、例では以下の方法を示します:

- イメージを作成する。
- Graphics オブジェクトを初期化する。
- サーフェスをクリアする。
- [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) クラスのインスタンスを作成する。
- 図形を作成する。
- 図形に形状を追加する。
- 図形の配列を作成する。
- パスを描画する。
- パスを塗りつぶす。


### **GraphicsPath クラスを使用した画像の描画: プログラミング例**
#### **GraphicsPath: イメージの作成**
まず、ファイルの作成で説明されている方法を使用してイメージを作成します。
#### **GraphicsPath: Graphics オブジェクトの初期化**
Image オブジェクトをコンストラクタに渡すことで、Graphics オブジェクトを作成して初期化します。
#### **GraphicsPath: サーフェスのクリア**
Graphics サーフェスを Clear メソッドを呼び出してクリアし、Color をパラメータとして渡します。このメソッドは、引数として渡された色で Graphics サーフェスを塗りつぶします。
#### **GraphicsPath: GraphicsPath のインスタンスを作成**
GraphicsPath のインスタンスを作成し、GraphicsPath をデフォルトで Alternate に設定します。このモードは、閉じた図形の内部を塗りつぶす方法を決定します。他の可能な GraphicsPath の値は Winding です。
#### **GraphicsPath: 図形を作成**
Figure クラスのインスタンスを作成します。前述のように、Figure には Shapes が含まれ、shapes は Aspose.PSD.Shapes ネームスペースにあります。
#### **GraphicsPath: 図形に形状を追加**
Figure クラスが公開する Add Shapes メソッドを使用すると、図形に形状を追加できます。以下のコード例では、いくつかの形状を Figure オブジェクトに追加しています。
#### **GraphicsPath: 図形を配列に追加**
複数の図形を AddFigures メソッドを使用して GraphicsPath オブジェクトに追加できます。このメソッドは、図形の配列をパラメータとして受け入れます。
#### **GraphicsPath: パスを描画**
Graphics クラスが公開する DrawPath メソッドを使用して GraphicsPath を描画します。このメソッドは 2 つのパラメータを受け入れます。最初のパラメータは Path の色、幅、スタイルを決定する Pen クラスのオブジェクトであり、2 番目のパラメータはパス自体を表す GraphicsPath クラスのオブジェクトです。
#### **GraphicsPath: パスを塗りつぶす**


Graphics クラスが公開する Fill Paths メソッドに GraphicsPath オブジェクトを渡すことで、パスを塗りつぶすことができます。Fill Paths メソッドは、パスが現在パスに設定されている塗りつぶしモード（alternate または winding）に従ってパスを塗りつぶします。パスに開いている図形がある場合、その図形が閉じられたと仮定してパスが塗りつぶされます。

Fill Paths メソッドは 2 つのパラメータを受け入れます。最初のパラメータは、Aspose.PSD.Brushes ネームスペースからの任意のブラシクラスのオブジェクトです。2 番目のパラメータはパス自体です。この例では、HatchBrush を使用し、これはハッチスタイル、前景色、背景色を持つ四角形ブラシです。HatchBrush オブジェクトを Fill Paths メソッドに渡す前に、そのプロパティを設定してください。
### **GraphicsPath: 完全なソース**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}

全ての IDisposable を実装したクラスは正しく破棄されるよう、Using ステートメント内でインスタンス化されます。

