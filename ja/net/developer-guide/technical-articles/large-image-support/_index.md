---
title: 大きな画像のサポート
type: ドキュメント
weight: 40
url: /ja/net/large-image-support/
---

## **大きな画像のサポート**
標準の.NETライブラリには処理できる画像サイズに制限があるため、大きな画像のサポートのための新しいメカニズムを導入しました。この新しいアプローチは制限を克服していますが、データサイズの制限により、作成およびロードの最大サポート寸法は2,147,483,647 x 2,147,483,647ピクセルです。
### **大きな画像の操作**
Aspose.PSDでは大きな画像の性能とサポートが向上しています。数百メガバイトのサイズの画像でも問題なく作成、ロード、および描画が可能です。ただし、OutOfMemoryException例外の部分的な処理とハンドリングにより、非常に大きな画像では性能が非常に低くなる場合があります。これは、Aspose.PSDが処理のためにより小さいデータ量を再割り当てしようとするためであり、各再割り当てステップが非常にコストがかかるためです。新しいアーキテクチャの利点は明らかです：

- 画像サイズに制限がありません。
- PCで利用可能なメモリに制限されることはありません。

処理が遅い場合は、すべてのピクセルをメモリに収めるため、総RAM量を増やすことが推奨されます。そうしないと、処理は可能ですが遅くなります。アプローチは以下のとおりです：

- [ロードパーシャルピクセルズ](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels)メソッドを、指定した長方形とロードされたピクセルが指定されたデリゲートと共に呼び出します。

Aspose.PSDは長方形全体をロードしようとします。

- メモリにすべてのピクセルを収めるのに十分なスペースがある場合、すべてのピクセルが呼び出し元に返されます。
- メモリが不足している場合、呼び出し元は指定された長方形の内部からピクセルのサブセットを受け取ります。これらのピクセルが処理された後、呼び出し元は次の長方形を受け取ります。長方形全体が処理されると処理が終了します。

Aspose.PSDはできるだけ多くの行を抽出しようとします。1行のピクセルを収めるためのメモリが十分でない場合、1行が1の高さを持つ長方形に一様に分割されます。大きな画像に描画することもできます。描画プロセスは指定した長方形全体に影響を与えようとします。メモリが不足している場合、描画は完全な長方形が描画されるまで部分長方形で行われます。さらに、Aspose.PSDは大きな画像の保存とエクスポートをサポートしています。ソース画像をディスクに保存したり、他のファイル形式にエクスポートすることができます。必要に応じて、保存またはエクスポートプロセスは部分長方形を使用して実行されます。
### **サポートされている画像形式**
以下の形式は大きな画像の処理に対してサポートされています：

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

上記の形式は画像サイズに関係なく安全に処理され、作成、変更、描画操作の適用、ディスクへの保存またはエクスポートが可能です。

