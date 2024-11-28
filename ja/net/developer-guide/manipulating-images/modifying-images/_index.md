---
title: 画像の修正
type: ドキュメント
weight: 50
url: /ja/net/modifying-images/
---

## **ラスター画像のディザリング**
ディザリングは、実際に画像を作成するドットのパターンを変化させることによって、新しい色や濃淡の錯覚を作り出す技術です。これは、画像のカラー範囲を256色（またはそれ以下）に減らすための最も一般的な手段です。Aspose.PSDは、[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) クラス向けのディザリングサポートを提供し、Ditherメソッドを導入しています。このメソッドは、適用するディザリング手法を指定するDitheringMethod型の最初のパラメータと、ディザリング結果のサンプリングサイズを定義する整数であるビット数の2つのパラメータを受け入れます。デフォルト値は黒と白を示す1であり、許可される値はそれぞれ、2、4、256色を生成するパレットを生成します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}

## **明るさ、コントラスト、ガンマの調整**
デジタル画像のカラー調整は、画像処理ライブラリの主要機能の1つです。カラー調整は以下のようにカテゴリ分けされます。

1. 明るさは色の明るさまたは暗さを指します。画像の明るさを増やすと全ての色が明るくなり、明るさを減らすと全ての色が暗くなります。
1. コントラストは、画像内のオブジェクトやディテールをより明瞭にすることを指します。画像のコントラストを増やすと、明暗の差が増え、明るい部分がより明るく、暗い部分がより暗くなります。一方、コントラストを減らすと、明るい部分と暗い部分はほぼ同じままですが、画像全体が均質化されます。
1. ガンマは、画像内の物体を照らしている間接光のコントラストと明るさを最適化します。
### **明るさの調整**
Aspose.PSD for .NET APIは、[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) クラス向けの[AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) メソッドを提供しており、画像の明るさを整数値としてパラメータとして渡すことで調整できます。パラメータの値が最も高いほど、より明るい画像になります。以下に、オリジナル画像と結果画像の比較が表示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}

### **コントラストの調整**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) クラスが公開する[AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) メソッドは、画像のコントラストを調整するために浮動小数点値をパラメータとして渡すことができます。パラメータの値が最も高いほど、与えられた画像のコントラストが高くなります。以下に、オリジナル画像と結果画像の比較が表示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}

### **ガンマの調整**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) クラスが公開する[AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) メソッドには2つのオーバーロードがあります。1つのオーバーロードは1つの浮動小数点値を受け入れ、赤、青、緑の各色係数に対してガンマ補正を行います。一方、他のオーバーロードはそれぞれの色係数を表す3つの浮動小数点パラメータを受け入れます。次のコード例は、画像にガンマ補正を適用する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}

## **画像のぼかし**
この記事では、Aspose.PSD for .NETを使用して画像にぼかし効果を適用する方法を示しています。Aspose.PSD APIは、この目標を達成するための効率的で使いやすいメソッドを公開しています。Aspose.PSD for .NETは、画像にぼかし効果を作成するための[GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) クラスを公開しています。ぼかし効果を作成するためには、[GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) クラスに半径とシグマ値を指定する必要があります。リサイズを実行する手順は以下の通りです。

1. Imageクラスによって公開されているLoadファクトリメソッドを使用して画像を読み込みます。
1. 画像を[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)に変換します。
1. デフォルトコンストラクタを使用した[GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) クラスのインスタンスを作成するか、コンストラクタで半径とシグマ値を指定します。
1. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filterメソッドを呼び出して、画像の境界と[GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) クラスのインスタンスを指定します。
1. 結果を保存します。

次のコード例は、画像でぼかし効果を作成する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}

## **画像の透過性を確認**
この記事では、Aspose.PSD for .NETを使用して画像の透明性を確認する方法を示しています。画像の透明性を確認する手順は以下の通りです。

1. Imageクラスが公開する[Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) ファクトリメソッドを使用して画像を読み込みます。
1. 画像の不透明度をチェックし、不透明度がゼロであれば画像は透明です。
1. 次のコード例は、画像が透明かどうかを確認する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}

## **損失率のGIF圧縮を実装**
Aspose.PSD for .NETを使用すると、開発者はピクセルの差異を設定できます。GIFの圧縮は、見られるピクセルの「辞書」に基づいています。通常のエンコーダーは、画像内のピクセルと完全に一致する最も長いピクセル文字列を辞書で検索します。一方、損失エンコーダーは、画像内のピクセルに「十分に似ている」最長のピクセル文字列を選択します。以下に、この機能のコードデモンストレーションが示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}

## **バイキュービックリサンプリングの実装**
リサンプリングとは、画像のピクセル寸法を変更することです。ダウンサンプリングすると、ピクセルが削除され、したがって画像から情報と詳細が削除されます。アップサンプリングすると、ピクセルが追加されます。Photoshopはこのようなピクセルを補間して追加します。この記事では、Aspose.PSD for .NETを使用してバイキュービックリサンプリングを実行する方法を示しています。

以下に、この機能のコードデモンストレーションが示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}

## **カラーバランス調整レイヤー**
この記事では、Aspose.PSD for .NETを使用して画像に**カラーバランス調整レイヤー**を適用する方法を示しています。カラーバランス調整レイヤーを使用すると、画像の色調を調整する能力が得られます。これにより、三つのカラーチャンネルとその補色が表示され、これらのペアのバランスを調整して写真の外観を変更できます。

以下に、この機能のコードデモンストレーションが示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}

## **反転調整レイヤー**
この記事では、Aspose.PSD for .NETを使用して**反転調整レイヤー**を実行する方法を示しています。調整レイヤーは、主にカラー補正のために使用される特別な種類のレイヤーです。独自のコンテンツを持つのではなく、それらの下のレイヤーの情報を調整します。反転調整レイヤーは、画像の色を反転してネガティブ効果を与えます。

以下に、この機能のコードデモンストレーションが示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}

