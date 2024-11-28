---
title: 画像の作成、開封、保存
type: ドキュメント
weight: 30
url: /ja/net/creating-opening-and-saving-images/
---

## **画像ファイルの作成**
Aspose.PSD for .NETを使用すると、開発者は独自の画像を作成できます。 Imageクラスによって公開された静的Createメソッドを使用して新しい画像を作成します。必要なのは、出力画像形式のためのImageOptions名前空間のクラスのいずれかの適切なオブジェクトを提供するだけです。 画像ファイルを作成するには、まずImageOptions名前空間のクラスのインスタンスを作成します。これらのクラスは出力画像形式を決定します。 以下はImageOptions名前空間からのいくつかのクラスです（現在はPSDファイル形式ファミリーだけが作成されてサポートされています）：

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) は PSDファイルを作成するためのオプションを設定します。出力パスを設定するか、ストリームを設定することで画像ファイルを作成できます。
### **パスを設定して作成**
[ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 名前空間からPsdOptionsを作成し、さまざまなプロパティを設定します。 設定する最も重要なプロパティはSourceプロパティです。 このプロパティは画像データがどこにあるかを指定します（ファイル内またはストリーム内）。 下の例では、ソースはファイルです。 プロパティを設定した後、Imageクラスのstatic [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) メソッドの1つにオブジェクトを渡します。 オブジェクトには幅と高さのパラメータも必要です。 幅と高さはピクセル単位で定義されています。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **ストリームを使用して作成**
ストリームを使用してイメージを作成するプロセスは、パスを使用する場合と同じです。 違いは、Streamオブジェクトをそのコンストラクタに渡し、Sourceプロパティに割り当てる[StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource)のインスタンスを作成する必要がある点です。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **画像ファイルの開封**
開発者は、様々な目的で既存のPSD画像ファイルを開くためにAspose.PSD for .NET APIを使用できます。画像に効果を追加したり、既存のファイルを別の形式に変換するなどの目的に使えます。 Aspose.PSDは既存のファイルを開くための2つの標準方法を提供します：ファイルから、またはストリームから。
### **ディスクから開く**
ファイルのパスとファイル名をImageクラスの staticメソッドLoadにパラメータとして渡すことで、イメージファイルを開きます。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **ストリームを使用して開く**
開く必要があるイメージがストリームとして保存されている場合は、Loadメソッドのオーバーロードバージョンを使用します。 このオーバーロードバージョンは、イメージを開くためにStreamオブジェクトを引数として受け入れます。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **レイヤーとしてイメージをロード**
本記事では、Aspose.PSDを使用して画像をレイヤーとしてロードする方法を示します。 Aspose.PSD APIは、この目標を達成するための効率的で使いやすいメソッドを公開しています。 Aspose.PSDは、PsdImageクラスのAddLayerメソッドを使って画像をPSDファイルにレイヤーとして追加します。

PSDに画像をレイヤーとしてロードする手順は以下の通りです：

- 指定された幅と高さでPsdImageクラスを使用してイメージのインスタンスを作成します。
- Imageクラスが公開するfactoryメソッドLoadを使用してPSDファイルをイメージとしてロードします。
- Layerクラスのインスタンスを作成し、PSDイメージレイヤーをそれに割り当てます。
- 作成したレイヤーをPsdImageクラスが公開するAddLayerメソッドを使って追加します
- 結果を保存します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **ストリームからのレイヤーとしてイメージをロード**
本記事では、ストリームからイメージをレイヤーとしてロードする方法を示します。 イメージをストリームからロードするには、単純にイメージを含むストリームオブジェクトをLayerクラスのコンストラクタに渡します。 作成したレイヤーをPsdImageクラスが公開するAddLayerメソッドを使って追加し、結果を保存します。


サンプルコードは以下の通りです。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **画像ファイルの保存**
Aspose.PSDを使用すると、画像ファイルをゼロから作成することができます。既存の画像ファイルを編集する手段も提供します。 画像が作成されたり変更されたりすると、通常はファイルがディスクに保存されます。 Aspose.PSDには、パスを指定して画像をディスクに保存するためのメソッドやストリームオブジェクトを使用するメソッドが用意されています。
### **ディスクに保存**
Imageクラスは画像オブジェクトを表すため、このクラスは画像を作成、ロード、保存するために必要なすべてのツールを提供します。 画像を保存するには、ImageクラスのSaveメソッドを使用します。 Saveメソッドの1つのオーバーロードバージョンはファイルの場所を文字列として受け取ります。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **ストリームに保存**
Saveメソッドの別のオーバーロードバージョンはStreamオブジェクトを引数として受け入れ、画像ファイルをストリームに保存します。

ImageクラスのコンストラクタでCreateOptionsのいずれかを指定して画像が作成された場合、Imageクラスの初期化時に指定したパスまたはストリームに画像は自動的に保存されます。 保存メソッドを呼び出すときは、パラメータを受け取らないSaveメソッドを使用します。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **欠落フォントの置き換え設定**
開発者は、PSD文書をラスターイメージ（PNG、JPG、BMP形式に）変換して保存する際に、欠落フォントの代替としてデフォルトフォント名を設定するなど、さまざまな目的で既存のPSD画像ファイルをAspose.PSD for .NET APIを使用してロードできます。 画像が変更されたら、ファイルはディスクに保存されます。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}
