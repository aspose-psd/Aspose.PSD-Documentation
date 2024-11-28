---
title: PNG画像の操作
type: docs
weight: 40
url: /ja/net/manipulating-png-images/
---

## **PNG画像の透明度の指定**
PNG形式で画像を保存する利点の1つは、PNGに透明な背景を持たせることができる点です。Aspose.PSD for .NETは、以下のセクションで示されているように、PNG画像およびラスター画像の透明度を指定する機能を提供しています。Aspose.PSD for .NET APIは、新しいPNG画像を作成する際や既存の画像をPNG形式に変換する際に、透明色を指定するために使用できます。そのために、Aspose.PSD for .NET APIは、[TransparentColorプロパティ](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor)と[PngColorType列挙型](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype)を公開しており、PNG画像内で透明にする任意の色を指定するために設定できます。以下の提供されたコードスニペットは、指定された色を透明にして既存のPSD画像をPNG画像に変換する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **PNG画像の解像度の設定**
Aspose.PSD for .NETは、すべての画像形式（PNGを含む）の解像度を設定するために使用できるResolutionSettingクラスを公開しています。この記事では、Aspose.PSD for .NET APIを使用してPNG画像形式の水平および垂直解像度パラメータを設定する方法を示しています。以下のコードスニペットでは、既存のPSD画像を読み込んでPNG形式に変換し、また解像度を変更します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}

## **PNGファイルの圧縮**
Portable Network Graphic（PNG）は、ネットワークを介してビットマップを転送するための無損失圧縮形式です。任意のプログラムで画像をPNGファイルとして保存するとき、0から最大レベルまでの範囲で圧縮レベルを選択するように求められることがあります。この値を設定することで、ファイルサイズが圧縮され、画質が低下することはありません。この記事では、Aspose.PSD APIがPNGファイルサイズを制御する方法について説明します。Aspose.PSD APIsを使用して、PngOptionsクラスを介してPNGファイル形式の圧縮レベルを設定できます。このクラスには、int型の[CompressionLevelプロパティ](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel)があり、このプロパティは0から9までの値を受け入れます（9が最大圧縮です）。以下の提供されたコードスニペットは、Aspose.PSD for .NET APIを使用して圧縮レベルを設定する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **PNG画像のビット深度の指定**
画像のビット深度とは、ビットマップ画像内の単一のピクセルの色を示すのに使用されるビット数です。他のすべてのビットマップ形式と同様に、PNGカラーの深度も1ビット（2色）、2ビット（4色）、4ビット（16色）、8ビット（256色）などのようにビットで表されます。Aspose.PSD for .NET APIは、PngOptionsクラスによって公開される[BitDepthプロパティ](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth)を使用してPNG画像のビット深度を設定することができます。現時点では、BitDepthプロパティは、グレースケールおよびインデックスカラータイプの場合に1、2、4、または8ビットに設定できます。ほかのすべてのカラータイプでは、8ビットのみがサポートされます。以下の提供されたコードスニペットは、PNG画像のビット深度を設定する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **PNG画像にフィルター効果を適用する**
画像のビット深度とは、ビットマップ画像内の単一のピクセルの色を示すのに使用されるビット数です。他のすべてのビットマップ形式と同様に、PNGカラーの深度も1ビット（2色）、2ビット（4色）、4ビット（16色）、8ビット（256色）などのようにビットで表されます。Aspose.PSD for .NET APIは、PngOptionsクラスによって公開されるBitDepthプロパティを使用してPNG画像のビット深度を設定することができます。現時点では、BitDepthプロパティはグレースケールおよびインデックスカラータイプの場合に1、2、4、または8ビットに設定できます。ほかのすべてのカラータイプでは、8ビットのみがサポートされます。以下の提供されたコードスニペットは、PNG画像のビット深度を設定する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **透明なPNG画像の背景色の変更**
PNG形式の画像は透明な背景を持つことができます。Aspose.PSD for .NETは、透明な背景を持つPNG画像の背景色を変更する機能を提供しています。Aspose.PSD for .NET APIは、透明なPNG画像の背景色を設定/変更するために使用できます。以下の提供されたコードスニペットは、透明なPNG画像の背景色を設定/変更する方法を示しています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
