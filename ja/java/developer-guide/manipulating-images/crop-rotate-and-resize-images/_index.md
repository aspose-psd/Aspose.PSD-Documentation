---
title: 画像の切り取り、回転、リサイズ
type: ドキュメント
weight: 40
url: /ja/java/crop-rotate-and-resize-images/
---

## **画像の切り取り**
画像の切り取りとは、通常、画像の外側の部分を削除してフレームを改善することを指します。切り取りは、画像の特定の領域に焦点を当てるために画像の一部を切り取るためにも使用される場合があります。Aspose.PSD APIでは、画像の切り取りを行うための2つの異なる方法、シフトによる切り取りと矩形による切り取りがサポートされています。
### **シフトによる切り取り**
RasterImageクラスは、左、右、上、下を示す4つの整数値を受け入れるCropメソッドのオーバーロードバージョンを提供しています。これらの4つの値に基づいて、Cropメソッドは画像の境界を画像の中心に向かって移動させながら外部の部分を破棄します。以下のコードスニペットは、シフトによる画像の切り取り方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **矩形による切り取り**
RasterImageクラスは、矩形クラスのインスタンスを受け入れるCropメソッドの別のオーバーロードバージョンを提供しています。Rectangleオブジェクトに所望の境界を指定することで、画像の任意の部分を切り取ることができます。以下のコードスニペットは、矩形によって画像を切り取る方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **画像の回転と反転**
JavaのAspose.PSDは、複雑な操作を実行するためのシンプルなメソッドを提供するため使いやすいライブラリです。例えば、回転したい場合は、Aspose.PSD for Javaでは、基本クラスImageにRotateFlipメソッドが用意されています。画像の形式に関係なく、ライブラリは特定の回転＆反転手順を実行できます。
### **画像の回転**
Image.RotateFlipメソッドは、画像を90°/180°/270°回転させ、画像を水平または垂直に反転させるために使用できます。Image.RotateFlipメソッドは、画像に適用する回転と反転の種類を指定するRotateFlipTypeパラメータを受け入れます。回転と反転を実行する手順は以下のように簡単です。

1. Imageクラスが公開するファクトリーメソッドLoadを使用して画像を読み込む。
1. 適切なRotateFlipTypeを指定しながらImage.RotateFlipメソッドを呼び出す。
1. 結果を保存する。

以下のコード例は、ImageのRotateFlipプロパティとRotateFlipType列挙体を設定する方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **特定の角度で画像を回転**
Aspose.PSD for Java APIには、特定の角度で画像を回転させたいユーザーをサポートするために、RasterImage.Rotateメソッドが公開されています。RasterImage.RotateFlipメソッドと異なり、RasterImage.Rotateメソッドは以下の3つのパラメータを受け入れます。

1. 回転角度：画像を回転させる角度を指定するfloat型のパラメータ。正の値は画像を時計回りに回転させ、負の値は反時計回りに回転します。
1. 均等にリサイズ：Boolean型のパラメータは、画像のサイズを回転した矩形（角のポイント）の投影に従って変更するかどうかを指定します。falseに設定されている場合、画像の寸法は変更されず、内部画像コンテンツのみが回転されます。
1. 背景色：Color型のパラメータは、回転された画像の背景に塗られる色を指定します。

以下のコードスニペットは、RasterImage.Rotateメソッドの使用法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **画像のリサイズ**
この記事では、Aspose.PSD for Javaを使用して画像のリサイズ操作を行う方法を示しています。Aspose.PSD APIには、この目標を達成するための効率的で使いやすいメソッドが公開されています。Aspose.PSD for Javaは、既存の画像をリサイズするために使用できるImageクラスのResizeメソッドを公開しています。アプリケーションのニーズに合わせて、Resizeメソッドの2つのオーバーロードが用意されています。
### **単純なリサイズ**
リサイズを行う手順は以下のとおりです：

1. Imageクラスが公開するファクトリーメソッドLoadを使用して画像を読み込む。
1. 新しい高さと幅を指定しながらImage.Resizeメソッドを呼び出す。
1. 結果を保存する。

以下のコード例は、画像をリサイズする方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **ResizeType列挙体を使用したリサイズ**
Aspose.PSD APIは、Image.Resizeで使用するResizeType列挙体を公開しています。以下のコードスニペットは、ResizeType列挙型の使用法を示しています。ResizeType列挙型のメンバーの詳細は、このページの最下部に記載されています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}


リサイズ後に品質の高い結果を得たい場合は、常にResizeType.LanczosResampleを使用することをお勧めします。これにより、高品質な結果が出力されますが、ResizeType.NearestNeighbourResampleよりも処理が遅くなる可能性があります。一方、ResizeType.NearestNeighbourResampleアルゴリズムは、画質を犠牲にして高速なリサイズを行うために特に使用されます。このメソッドは、サムネイルのリアルタイム生成など、パフォーマンスが必要なプロセスに役立ちます。
## **画像を比例してリサイズ**
新しい高さと幅の値をImage.Resizeメソッドにパラメータとして渡すことで画像をリサイズすることができますが、その場合、アスペクト比を自分で計算する必要があります。これは、画像の幅または高さが変更されると、画像が新しいサイズに合わせてスケーリングまたは縮小されるためです。画像の幅と高さの変更が比例していないと、伸びたり歪んだ結果につながる可能性があるためです。この記事では、Aspose.PSD for Java APIを使用して、新しい高さまたは幅を渡すことで画像を自動的に比例させる方法を示しています。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **ResizeType列挙体**
ResizeTypeは、選択したフィルタに基づいて画像上で実行するリサイズのタイプを決定します。

ResizeType列挙体メンバー

|**メンバー名**|**値**|**説明**|
| :- | :- | :- |
|LeftTopToLeftTop|0|新しい画像の左上点が元の画像の左上点と一致します。必要に応じてクロップが行われます。|
|RightTopToRightTop|1|新しい画像の右上点が元の画像の右上点と一致します。必要に応じてクロップが行われます。|
|RightBottomToRightBottom|2|新しい画像の右下点が元の画像の右下点と一致します。必要に応じてクロップが行われます。|
|LeftBottomToLeftBottom|3|新しい画像の左下点が元の画像の左下点と一致します。必要に応じてクロップが行われます。|
|CenterToCenter|4|新しい画像の中心が元の画像の中心と一致します。必要に応じてクロップが行われます。|
|LanczosResample|5|7x7マスクを使用したLanczosアルゴリズムを使用してリサンプリングします。|
|NearestNeighbourResample|6|最近傍補間アルゴリズムを使用してリサンプリングします。|
