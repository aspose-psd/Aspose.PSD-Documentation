---
title: 画像の描画
type: ドキュメント
weight: 10
url: /ja/net/drawing-images/
---

## **直線の描画**
この例では、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスを使用して、イメージの表面に直線形状を描画します。操作をデモンストレーションするために、例では新しいイメージを作成し、Graphics クラスによって公開された [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) メソッドを使用して、イメージの表面に直線を描画します。まず、高さと幅を指定して PsdImage を作成します。

イメージが作成されたら、Graphics クラスによって公開された Clear メソッドを使用して背景色を設定します。[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスの [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) メソッドは、2つのポイント構造を結ぶイメージに直線を描画するために使用されます。このメソッドには、Pen クラスのインスタンスおよびポイントまたは構造体の座標ペアを引数として受け入れるいくつかのオーバーロードがあります。Pen クラスは、線、曲線、図形を描画するためのオブジェクトを定義します。Pen クラスには、指定された色、幅、およびブラシで線を描画するためのいくつかのオーバーロードされたコンストラクタがあります。SolidBrush クラスは、特定の色で連続して描画するために使用されます。最後に、イメージは bmp ファイル形式にエクスポートされます。以下のコードスニペットは、イメージの表面に直線形状を描画する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}


## **楕円の描画**
楕円の描画例は、描画された形状シリーズの2番目の記事です。[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスを使用して、イメージの表面に楕円形状を描画します。操作をデモンストレーションするために、例では新しいイメージを作成し、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスによって公開された DrawEllipse メソッドを使用して、イメージの表面に楕円形状を描画します。まず、高さと幅を指定して PsdImage を作成します。

イメージを作成した後、Graphics クラスオブジェクトを作成して初期化し、Clear メソッドを使用してイメージの背景色を設定します。[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスの DrawEllipse メソッドは、矩形構造によって指定されたイメージ表面に楕円形状を描画するために使用されます。このメソッドには、Pen インスタンスと Rectangle/RectangleF クラスまたは座標ペア、高さ、幅を引数として受け入れるいくつかのオーバーロードがあります。Pen クラスは、線、曲線、図形を描画するために使用されるオブジェクトを定義します。Pen クラスには、指定された色、幅、ブラシで線を描画するためのいくつかのオーバーロードされたコンストラクタがあります。Rectangle クラスは、矩形の位置とサイズを表す4つの整数のセットを格納します。Rectangle クラスには、指定されたサイズと位置で矩形構造を描画するためのいくつかのオーバーロードされたコンストラクタがあります。SolidBrush クラスは、特定の色で連続して描画するために使用されます。最後に、イメージは bmp ファイル形式にエクスポートされます。以下のコードスニペットは、イメージの表面に楕円形状を描画する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}


## **四角形の描画**
この例では、イメージの表面に四角形形状を描画します。操作をデモンストレーションするために、例では新しいイメージを作成し、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスによって公開された DrawRectangle メソッドを使用して、イメージの表面に四角形形状を描画します。まず、高さと幅を指定して PsdImage を作成します。その後、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスの Clear メソッドを使用して、イメージの背景色を設定します。

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスの DrawRectangle メソッドは、矩形構造によって指定されたイメージ表面に四角形形状を描画するために使用されます。このメソッドには、Pen および Rectangle/RectangleF クラスのインスタンス、または座標ペア、幅、高さを引数として受け入れるいくつかのオーバーロードがあります。Rectangle クラスには、矩形の位置とサイズを表す4つの整数のセットを格納します。Rectangle クラスには、指定されたサイズと位置で矩形構造を描画するためのいくつかのオーバーロードされたコンストラクタがあります。最後に、イメージは bmp ファイル形式にエクスポートされます。以下のコードスニペットは、イメージの表面に四角形形状を描画する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}


## **円弧の描画**
この図形シリーズのセッションでは、イメージの表面に円弧形状を描画します。[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) の DrawArc メソッドを使用して、BMP イメージ上で操作をデモンストレーションします。まず、高さと幅を指定して PsdImage を作成します。イメージが作成されたら、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスによって公開された Clear メソッドを使用して背景色を設定します。

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスの DrawArc メソッドは、イメージ表面に円弧形状を描画するために使用されます。DrawArc は、矩形構造または座標ペアで指定された楕円の一部を表します。このメソッドには、Pen クラスと Rectangle/RectangleF 構造体または座標ペア、幅、高さを引数として受け入れるいくつかのオーバーロードがあります。最後に、イメージは bmp ファイル形式にエクスポートされます。以下のコードスニペットは、イメージの表面に円弧形状を描画する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}


## **ベジエ曲線の描画**
この例では、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスを使用して、イメージの表面にベジエ曲線形状を描画します。操作をデモンストレーションするために、例では新しいイメージを作成し、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスによって公開された DrawBezier メソッドを使用して、イメージの表面にベジエ曲線形状を描画します。まず、高さと幅を指定して PsdImage を作成します。イメージが作成されたら、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスによって公開された Clear メソッドを使用して背景色を設定します。

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスの DrawBezier メソッドは、4つのポイント構造で定義されたイメージ表面にベジエスプライン形状を描画するために使用されます。このメソッドには、Pen クラスのインスタンスと4つの順序付けられた座標ペア、4つの Point/PointF 構造体、または Point/PointF 構造体の配列を引数として受け入れるいくつかのオーバーロードがあります。Pen クラスは、線、曲線、図形を描画するためのオブジェクトを定義します。Pen クラスには、指定された色、幅、ブラシで線を描画するためのいくつかのオーバーロードされたコンストラクタがあります。最後に、イメージは bmp ファイル形式にエクスポートされます。以下のコードスニペットは、イメージの表面にベジエ形状を描画する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}


## **コア機能を使用したイメージの描画**
Aspose.PSD は、画像をゼロから作成するを含む多くの有用な機能を提供するライブラリです。画像のビットマップ情報を操作するなど、コア機能を使用した描画や、[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) および [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) のような高度な機能を使用して異なるブラシとペンを使用してイメージ表面に形状を描画します。Aspose.PSD の RasterImage クラスを使用すると、画像領域のピクセル情報を取得し、操作できます。RasterImage クラスには、ピクセルの取得と設定などの画像操作のためのメソッドが含まれています。Creating Files で説明されている方法のいずれかを使用して新しい画像を作成し、RasterImage クラスのインスタンスに割り当てます。RasterImage クラスの LoadPixels メソッドを使用して、画像の一部のピクセル情報を取得します。ピクセルの配列を取得したら、例えば各ピクセルの色を変更するなどの操作を行うことができます。ピクセル情報を操作した後は、RasterImage クラスの SavePixels メソッドを使用して、画像の所定の領域に設定します。以下のコードスニペットは、コア機能を使用してイメージを描画する方法を示しています。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
