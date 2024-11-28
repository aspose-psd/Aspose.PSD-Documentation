---
title: 画像の切り取り、回転、リサイズ
type: ドキュメント
weight: 40
url: /ja/net/crop-rotate-and-resize-images/
---

## **画像の切り取り**
通常、画像の切り取りとは、画像の外側部分を取り除いてフレーミングを改善することを指します。切り取りは、画像の特定の領域に焦点を当てたい場合に、画像の一部を切り抜くためにも使用されることがあります。Aspose.PSD APIは、画像の切り取りをするための2つの異なるアプローチをサポートしています: シフトによる切り取りと長方形による切り取り。

### **シフトによる切り取り**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) クラスは、左、右、上、下を示す4つの整数値を受け入れる Crop メソッドのオーバーロードバージョンを提供しています。これらの4つの値に基づいて、Crop メソッドは画像の境界を中心に向かって移動し、外側の部分を破棄します。以下のコードスニペットは、シフトによって画像を切り取る方法を示しています。

### **長方形による切り取り**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) クラスは、Rectangle クラスのインスタンスを受け入れる Crop メソッドの別のオーバーロードバージョンを提供しています。Rectangle オブジェクトに希望する境界を指定することで、画像の任意の部分を切り取ることができます。以下のコードスニペットは、長方形によって画像を切り取る方法を示しています。

## **画像の回転と反転**
Aspose.PSD for .NET は、複雑な操作を行うための簡単なメソッドを提供しているため、使いやすいライブラリです。たとえば、画像の回転を必要とするアプリケーション向けに、Aspose.PSD for .NET は、Image クラスの RotateFlip メソッドを提供しています。画像形式に関係なく、ライブラリは画像に特定の回転や反転手順を実行することができます。

### **画像の回転**
Image.RotateFlip メソッドを使用すると、画像を90/180/270度回転させたり、画像を水平または垂直に反転させたりすることができます。Image.RotateFlip メソッドは、画像に適用する回転および反転の種類を指定する RotateFlipType パラメータを受け入れます。回転および反転を行う手順は以下の通りです。
1. Image クラスによって公開された Load ファクトリメソッドを使用して画像を読み込みます。
1. 適切な RotateFlipType を指定しながら Image.RotateFlip メソッドを呼び出します。
1. 結果を保存します。

以下のコード例は、Image の RotateFlip プロパティと RotateFlipType 列挙型の設定方法を示しています。

## **特定角度で画像を回転**
Aspose.PSD for .NET API は、特定の角度で画像を回転させたいユーザーをサポートするために、[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate メソッドを公開しています。[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip メソッドとは異なり、[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate メソッドは次の3つのパラメータを受け入れます:

1. 回転角度: 画像を回転させる角度を指定する float 型のパラメータ。正の値は時計回りに画像を回転させ、負の値は反時計回りに回転させます。
1. 等しい比率でリサイズ: ブーリアン型のパラメータで、画像サイズを回転された長方形（ホットポイント）の射影に従って変更するかどうかを指定します。false に設定すると、画像の寸法は変更されず、内部の画像内容のみが回転されます。
1. 背景色: 回転された画像の背景に塗りつぶされる色を指定する Color 型のパラメータ。

以下のコードスニペットは、[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate メソッドの使用方法を示しています。

## **画像のリサイズ**
この記事では、Aspose.PSD for .NET を使用して画像のリサイズ操作を行う方法を示します。Aspose.PSD API は、この目的を達成するために効率的で使いやすいメソッドを公開しています。Aspose.PSD for .NET は、既存の画像をリサイズするために使用できる Image クラス向けの Resize メソッドを公開しています。アプリケーションのニーズに合わせて、2つのオーバーロードされた Resize メソッドがあります。

### **単純なリサイズ**
リサイズを行う手順は以下の通りです:
1. Image クラスによって公開された Load ファクトリメソッドを使用して画像を読み込みます。
1. 新しい高さと幅を指定しながら Image.Resize メソッドを呼び出します。
1. 結果を保存します。

以下のコード例は、画像をリサイズする方法を示しています。

### **ResizeType 列挙型を使用したリサイズ**
Aspose.PSD API には、Image.Resize で使用される ResizeType 列挙型が公開されており、望ましい結果を得るために使用できます。以下の提供されたコードスニペットは、ResizeType 列挙型の使用方法を示しています。ResizeType 列挙型のメンバの詳細はこのページの最下部で見つけることができます。

リサイズ後に品質の良い結果を得たい場合は、常に ResizeType.LanczosResample を使用することが推奨されます。これにより、高品質な結果が出力されますが、ResizeType.NearestNeighbourResample よりも処理速度が遅くなるかもしれません。一方、ResizeType.NearestNeighbourResample アルゴリズムは、画質に犠牲を払いながら高速にリサイズを行うため、サムネイルの生成などでパフォーマンスが必要なプロセスで有用です。

## **画像を比例的にリサイズ**
画像をリサイズするには、Image.Resize メソッドに新しい高さと幅の値をパラメータとして渡すことができますが、その場合はアスペクト比を自分で計算する必要があります。画像の幅または高さが変更されると、画像は新しいサイズに合わせて拡大または縮小されます。画像の幅と高さの変更が比例していない場合、伸縮や歪んだ結果になる可能性があります。この記事では、画像の片方の新しい高さまたは幅を渡すことで、他の比例的な値を自動的に計算させる Aspose.PSD for .NET API の使用方法を示しています。

### **ResizeType 列挙型**
ResizeType は、選択されたフィルタに基づいて画像に実行するリサイズのタイプを決定します。

[ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype) 列挙型のメンバ

|**Member Name**|**Value**|**Description**|
| :- | :- | :- |
|LeftTopToLeftTop|0|左上の点が新しい画像と元の画像の左上の点が重なります。必要に応じてクロップが発生します。|
|RightTopToRightTop|1|右上の点が新しい画像と元の画像の右上の点が重なります。必要に応じてクロップが発生します。|
|RightBottomToRightBottom|2|右下の点が新しい画像と元の画像の右下の点が重なります。必要に応じてクロップが発生します。|
|LeftBottomToLeftBottom|3|左下の点が新しい画像と元の画像の左下の点が重なります。必要に応じてクロップが発生します。|
|CenterToCenter|4|新しい画像の中心が元の画像の中心と一致します。必要に応じてクロップが発生します。|
|LanczosResample|5|7x7 マスクを使用した Lanczos アルゴリズムを使用して再サンプリングを行います。|
|NearestNeighbourResample|6|最近傍補間アルゴリズムを使用して再サンプリングを行います。|
