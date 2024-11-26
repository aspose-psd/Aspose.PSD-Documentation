---
title: 画像に署名を追加
type: ドキュメント
weight: 70
url: /ja/net/adding-a-signature-to-an-image/
---

## **署名の追加**

画像に署名を追加することは、画像を偽造から守るためにデジタル署名する必要があることがあります。別の考え方としては、画像をギャラリーに表示されているように扱うことができます。どちらの理由であっても、Aspose.PSD API は、簡単なメカニズムを使って画像に署名を追加する機能を提供しています。以下で説明するように、この例では [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) クラスを使用して、元の画像の表面に署名を追加する機能を提供しています。操作を示すために、ディスクから PSD 画像を読み込み、Graphics クラスの [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) メソッドを使用して元の画像の表面に署名として別の画像を描画します。作成されたイメージは、[PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions) クラスを使用して PNG 形式で保存します。以下は、画像に署名を追加する方法を示すコード例です。コード例は、分割されているため、操作を追うのが簡単です。ステップバイステップで、例は以下を示します:

- メインおよびセカンダリ (署名) 画像を読み込む。
- Graphics オブジェクトを作成して初期化する。
- Graphics クラスの DrawImage メソッドを使用してイメージを描画する。
- 結果を PNG 形式で保存する。
### **プログラムサンプル**
#### **画像の読み込み**
まず、イメージクラスのインスタンスを作成して、ディスクからサンプル画像を読み込みます。
#### **グラフィックオブジェクトの作成と初期化**
画像を読み込んだ後、プライマリイメージのオブジェクトを使用しながら、Graphics クラスオブジェクトを作成して初期化します。
#### **セカンダリイメージをプライマリイメージに描画**
次に、Graphics クラスの DrawImage メソッドを使用して、セカンダリイメージをプライマリイメージに追加します。DrawImage メソッドには、最初のパラメータとして Image オブジェクトを受け入れるオーバーロードバージョンが複数あり、他のすべてのパラメータはイメージを描画する場所に対応しています。デモのため、次のコードでは、DrawImage のオーバーロードバージョンを使用し、2 番目のパラメータとして Point オブジェクトを受け入れ、署名を元の画像の右下隅に描画しようとしています。
#### **イメージの保存**
最後に、PngOptions クラスを使用して、PNG ファイルとしてイメージをローカルディスクに保存します。
#### **コンプリートソース**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
