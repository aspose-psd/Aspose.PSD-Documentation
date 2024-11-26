---
title: フィルレイヤーのサポート
type: ドキュメント
weight: 90
url: /ja/net/support-of-fill-layers/
---

## **パターンフィルでのフィルレイヤー**
この記事では、[PSD](https://wiki.fileformat.com/image/psd/) レイヤーをパターンフィルで塗りつぶす方法を示しています。パターン* * は、画像や色、影、または線などが画像の領域を塗りつぶすために使用されます。Aspose.PSD.FileFormats.Psd.Layers.FillLayer を使用して、PSD レイヤーにパターンを追加します。以下のコードスニペットでは、PSD ファイルをロードし、[FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) クラスにアクセスし、[PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) プロパティを使用してパターンを設定します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}

以下は、[Aspose.PSD](https://products.aspose.com/psd/net) が [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) と [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings) を使用してパターンをレンダリングする別の例です。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}

## **グラデーションフィルでのフィルレイヤー**
この記事では、グラデーションフィルを使用してPSD レイヤーを塗りつぶす方法を示しています。Aspose.PSD API には、この目的を達成するための効率的で使いやすい方法が公開されています。Aspose.PSD では、[GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) および [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) クラスがレイヤーにグラデーション効果を追加するために公開されています。

グラデーションで PSD レイヤーを塗りつぶす手順は以下のように簡単です：

- [Image](https://reference.aspose.com/net/psd/aspose.psd/image) クラスで公開されたファクトリーメソッド [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) を使用して PSD ファイルを画像として読み込む。
- [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) オブジェクトの設定プロパティを設定する。
- 必要な色と色の位置を持つ [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) のリストを作成する。
- 必要な不透明度と透明度点の位置を持つ透明度ポイントのリストを作成する。
- [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) メソッドを呼び出す。
- 結果を保存する。

以下のコードスニペットは、グラデーションフィルを PSD レイヤーに追加する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}

**さらに、この例では、[GradientFillSettings.GradientType](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** プロパティを使用して PSD レイヤーにグラデーションフィルを入れる方法を示しています。Aspose.PSD は GradientType 列挙型を通じて以下のグラデーションタイプをサポートしています：

- **GradientType.Linear:** 線形グラデーションでは、色が直線に始まりから終わりまで遷移します。
- **GradientType.Radial:** 放射状グラデーションでは、色は始点から円形に広がります。
- **GradientType.Angle:** 角度グラデーションは、始点を中心に反時計回りに広がります。
- **GradientType.Reflected:** 反射グラデーションでは、色が始点の両側に対称に反映されます。
- **GradientType.Diamond:** ダイヤモンドグラデーションは、始点からダイヤモンド形状を作り出します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

## **グラデーションフィルレイヤーのスケールプロパティのサポート**
この記事では、Aspose.PSD for .NET を使用してグラデーションフィルで FillLayer をスケーリングする方法を示しています。このために、**IGradientFillSettings** に [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) プロパティが追加されました。

以下は、**Scale** プロパティを使用する方法を示すコードのデモンストレーションです。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}

## **カラーフィルでのフィルレイヤー**
この記事では、PSD レイヤーをカラーで塗りつぶす方法を示しています。[Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) クラスを使用して、PSD レイヤーにカラーを追加してください。以下のコードスニペットは、PSD ファイルを読み込み、Fill レイヤークラスにアクセスし、[FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings) プロパティを使用して色を設定します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}

