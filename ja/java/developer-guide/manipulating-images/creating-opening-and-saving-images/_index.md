---
title: 画像の作成、オープン、保存
type: ドキュメント
weight: 30
url: /ja/creating-opening-and-saving-images/
---

## **画像ファイルの作成**
Aspose.PSD for Java を使用すると、開発者は独自の画像を作成できます。Image クラスが公開する static Create メソッドを使用して新しい画像を作成します。必要なのは、出力画像形式のための ImageOptions ネームスペースのクラスのオブジェクトを供給するだけです。画像ファイルを作成するには、まず ImageOptions ネームスペースのクラスのインスタンスを作成します。これらのクラスは出力画像形式を決定します。以下に、ImageOptions ネームスペースからのいくつかのクラスが示されています（現在、PSD ファイル形式ファミリのみが作成にサポートされています）:

PsdOptions は PSD ファイルを作成するためのオプションを設定します。出力パスを設定するか、ストリームを設定することで画像ファイルを作成できます。
### **パスを設定して作成**
ImageOptions ネームスペースから PsdOptions を作成し、さまざまなプロパティを設定します。設定する最も重要なプロパティは、Source プロパティです。このプロパティは、画像データがどこにあるかを指定します（ファイルまたはストリーム）。以下の例では、ソースはファイルです。プロパティを設定した後、オブジェクトと幅と高さパラメータを1つの static Create メソッドに渡します。幅と高さはピクセル単位で定義されます。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **ストリームを使用して作成**
ストリームを使用して画像を作成するプロセスは、パスを使用する場合と同じです。唯一の違いは、Stream オブジェクトをそのコンストラクタに渡して StreamSource のインスタンスを作成し、Source プロパティに割り当てる必要があることです。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **画像ファイルのオープン**
開発者は、異なる目的で既存の PSD 画像ファイルを開くために Aspose.PSD for Java API を使用できます。例えば、イメージに効果を追加したり、既存のファイルを別の形式に変換したりすることができます。目的に関係なく、Aspose.PSD は既存のファイルを開くための 2 つの標準的な方法を提供します: ファイルからまたはストリームから。
### **ディスクからオープン**
Image クラスが公開する static Load メソッドに、パスとファイル名をパラメータとして渡すことで、画像ファイルを開きます。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **ストリームを使用して開く**
開く必要がある画像がストリームとして保存されている場合は、Load メソッドのオーバーロードバージョンを使用します。これにより、ストリームを引数として受け入れ、画像を開くことができます。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **レイヤーとして画像を読み込む**
この記事では、Aspose.PSD を使用して画像をレイヤーとして読み込む方法を示しています。Aspose.PSD API は、この目標を達成するための効率的で使いやすいメソッドを公開しています。Aspose.PSD は、PsdImage クラスの AddLayer メソッドを公開しており、PSD ファイルに画像をレイヤーとして追加することができます。

PSD に画像をレイヤーとして読み込む手順は以下の通りです:

- 指定された幅と高さで PsdImage クラスのインスタンスを作成します。
- Image クラスが公開するファクトリーメソッド Load を使用して画像を PSD ファイルとして読み込みます。
- Layer クラスのインスタンスを作成し、PSD 画像のレイヤーを割り当てます。
- AddLayer メソッドを使用して作成したレイヤーを PsdImage クラスが公開しているメソッドに追加します。
- 結果を保存します。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **画像ファイルの保存**
Aspose.PSD を使用すると、画像ファイルをゼロから作成できます。また、既存の画像ファイルを編集する手段も提供します。画像が作成または変更されたら、通常はファイルがディスクに保存されます。Aspose.PSD は、画像をディスクに保存するためのメソッドを、パスを指定するかストリーム オブジェクトを使用する方法で提供します。
### **ディスクへの保存**
Image クラスは画像オブジェクトを表し、このクラスは画像を作成、ロード、保存するために必要なすべてのツールを提供します。Save メソッドを使用して画像を保存します。Save メソッドのオーバーロードバージョンの 1 つは、ファイルの場所を文字列として受け入れます。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **ストリームへの保存**
Save メソッドの別のオーバーロードバージョンは、Stream オブジェクトを引数として受け入れ、画像ファイルをストリームに保存します。

画像が Image クラスの初期化時に提供されたパスまたはストリームで自動的に保存される場合、画像が Image クラスの初期化中に指定された CreateOptions のいずれかを指定して作成された場合は、Save メソッドを呼び出すことでパスまたはストリームに自動的に保存されます。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **欠落フォントの置換設定**
開発者は、Aspose.PSD for Java API を使用して既存の PSD 画像ファイルをロードし、PSD ドキュメントをラスター画像（PNG、JPG、BMP 形式のいずれかに）として保存する場合、PSD ドキュメントを保存するときに現在のオペレーティングシステム内で見つからない欠落しているフォントすべてにデフォルトフォント名を設定するなど、さまざまな目的で使用できます。画像が変更された後、ファイルはディスクに保存されます。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}


