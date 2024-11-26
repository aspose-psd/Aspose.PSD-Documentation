---
title: 生データ処理
type: docs
weight: 50
url: /ja/net/raw-data-processing/
---

## **生データ処理**
Aspose.PSD APIのパフォーマンスを向上させるために、バージョン2.4.0で生データ処理用のメソッドが導入されました。現在、生データ処理は内部で使用されており、外部APIを持っているため、ライブラリの外部から全体的なパフォーマンスを向上させるために使用できます。処理が複雑になり、説明が必要な場合があります。現在、生データ処理はBMP形式のみで利用可能です。

開発者が最高のパフォーマンスを得るために、Aspose.PSD APIは生データ処理システムを提供しており、外部APIを使用して生データ処理が可能です。開発者は、生データ処理を行うために [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) と [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) メソッドファミリーを呼び出します。これらのメソッドでは、望ましい生データ形式を [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings) クラスを使用して設定する必要があります。RawDataSettingsクラスを使用することで、開発者は任意の生データ形式を指定できます。ただし、最高のパフォーマンスを得るためには、データが格納されている生データ形式を使用する必要があります。 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) クラスに定義された RawDataSettings は、画像の生の [データ形式](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat) を決定するのに役立ちます。RawDataSettingsインスタンスを LoadRawData メソッドに渡すと、データは変換を適用せずにそのまま返され、パフォーマンスが向上する可能性があります。一方で、時には、多少複雑な生データ形式のレイアウトに注意を払う必要があります。

処理を簡略化するために、パフォーマンスに多少のペナルティを支払うことで、望ましい RawDataSettings を指定することが可能です。バージョン2.4.0では、CMYKカラースペースからRGBに変換することはできない場合など、指定された形式で生データを返すことができない場合があります。さらに、画像形式に対して生データ処理が全く利用できない場合もあります。 [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable) プロパティをクエリして、LoadRawData および SaveRawData メソッドファミリーを使用できるかどうかを確認する必要があります。
### **インサイト**
RGBの [ピクセルデータ形式](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) には、インデックス（パレットベース）およびRGBベースの生データ形式があります。インデックス生データ形式には、0..(2^ビット数 - 1) の範囲にパレットエントリインデックスが含まれます。インデックス生データ形式には1、2、4、8ビットのピクセル形式が含まれます。残りは RGB ベースの生データ形式です。生データの読み込み時に、データを読み込むために十分なバイトがあることに注意してください。それ以外の場合、適切な例外が発生します。行あたりのバイト配列サイズを行数で乗算することで、単純にバイト配列のサイズを見積もることができます。行のサイズは変動する可能性があり、生データの保存形式に依存します。

最高のパフォーマンスを得るためには常に、[RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize) プロパティ値と同じ生データ行サイズを使用してください。ただし、場合によっては、生データ行に追加のパディングを追加したり、削除したりする必要があるため、異なる行サイズを使用する場合があります。画像のバウンディング矩形のサブセットが必要な場合は、インデックスRGBピクセル形式でビットシフトが発生することに注意してください。例えば、次のような状況を考えてみましょう：100x100ピクセルの画像があり、1ピクセルあたり1ビットの生データ形式で生データ矩形をロードしようとしています。このような場合、右のビットを計算するために簡単な式が使用できます：(rect.Left * bitsCount) % 8。
### **インデックスRGB色変換**
可能な限り最高のパフォーマンスを得るためには、常に同じソースと宛先の生データ設定、ピクセル形式、および行サイズを使用してください。ただし、場合によってはデータの変換が必要になることがあります。たとえば、1ビットのピクセルごとのRGB画像をロードして、2ビットのピクセルごとに保存したり、4ビットのRGB画像を取得してカラー範囲を2ビットのピクセルごとにダウングレードしたりすることがあります。どちらの場合も、カラー変換が必要です。インデックスRGB画像の変換は、ときには少し複雑になり、いくつかの設定を適用しないと実行できないことがあります。ソースのカラー範囲がどのように目的のカラースペースとマッピングされるかを判断する必要があります。このタスクを達成するために、異なる [モード](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods) があります：

- パレットマッピング (DitheringMethods.PaletteConversion)
- 生データマッピング (DitheringMethods.PaletteIgnore)
- カスタム変換 (DitheringMethods.CustomConverter)

パレット変換が使用されると、ソースのカラースペースは可能な限り目標のカラースペースに一致しようとします。たとえば、次のカラーを持つ4ビット画像があるとします：
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
...
[15] RGB=255, 255, 255

ソース画像は次のような形になります：



変換後、以下のパレット色が定義された1ビット画像に4ビット画像を変換するとします。

[0] RGB=0, 0, 0
[1] RGB=255, 255, 255

パレット変換モードでは、コンバータはソースカラーを読み取り、ターゲットパレットの [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) メソッドを使用してターゲットインデックスを決定します。パレットの GetNearestColorIndex メソッドが範囲外のインデックスを返す場合は、 [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) プロパティ値が使用されます。これにより、ソースカラーが強度値の観点で最も近いターゲットカラーに変換されます。ターゲット画像は、可能な限りソース画像に一致します。次のような結果が得られます：


生データマッピングモードでは、異なるシナリオが使用されます。ソースとターゲットのカラーパレットは単純に無視され、ソースインデックスが対応するターゲットインデックスにマップされます。値がターゲット範囲にマップできない場合（ビット数を下げるとき）、RasterImage.RawFallbackIndex プロパティ値が使用されます。このプロパティ値はデフォルトで0であり、ターゲットパレット内の最初の色にマップされます。このプロパティ値がターゲット範囲外にある場合は、適切な例外がスローされます。これは、予測可能でない結果につながります。次の画像で示すことができるでしょう：


パレット変換モードは、カラーマッピングの問題に対するより正しい解決策ですが、正しいパレットのマッピングを推定するために計算が実行されるため、少し時間がかかることがあります。（通常、両方の方法の間に非常に小さなパフォーマンスの違いがあります。）一方、生データマッピングモードは、速度がやや速く、正確なカラーマッピングがそれほど重要でない場合に使用できます。たとえば、ソースカラーパレットがトリムされ、追加のビットが使用されていない場合には、安全にビット数を減らして変換できる場合があります。

これらのアプローチのいずれかを使用するには、RasterImage クラスの RawDitheringMethod プロパティを使用します。デフォルトでは、最高の見た目の結果を得るために、パレット変換メソッドに設定されています。このプロパティを変更してから変換を行う前に（たとえば、画像をストリームに保存する場合など）、このプロパティを変更できます。注意すべきことは、生データをロードし、元のピクセルデータを一部上書きした場合、新しいデータがキャッシュに入り、キャッシュはデータを最大可用フォーマットである32ARGBで保存するため、パレット無視とパレット変換のディザリング方法が適用されないことです（2.4.0の状態によって変更される可能性があります）。この形式は、読み込んだ画像と保存された画像の可能な異なる色範囲に関連する問題を克服するために使用されます。さらに、RGBモードで画像をロードしてインデックスモードに変換する場合やその逆も同様に、パレット無視とパレット変換のディザリング方法は無視されます。
### **カスタムカラーコンバータ**
カラー変換のための標準的なアプローチで十分とは限りません。カラー変換ルーチンを使用する際に完全な自由度を得るためには、カスタムアルゴリズムを使用したいことがあるかもしれません。ソースとターゲット画像のピクセル形式が両方とも指標RGB形式である場合、より単純なインターフェース [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter) を使用できます。 IIndexedColorConverter インターフェイスのインスタンスを [RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter) プロパティに設定し、RawDitheringMethod プロパティ値に [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter を使用してください。この組み合わせが暗示されると、任意の指数色変換が指定された IIndexedColorConverter インスタンスを介して実行されます。カスタム指数色変換には、次のメソッドが定義されます：



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



FillIndexedtoIndexedMap メソッドは、インデックスRGB画像からインデックスRGB画像形式に変換が必要な場合に呼び出されます（1、2、4、8ビットのいずれかが相互に変換される場合）。マップ配列には、すべての可能なソース形式エントリカウントの長さがあります。その配列をソースカラーパレットエントリから宛先パレットエントリへのマッピングに入れる必要があります。宛先インデックス値は、0..(ビット数 - 1) の範囲内である必要があることに注意してください。それ以外の場合、適切な例外がスローされます。

よりカスタムなカラー変換シナリオを実行する必要がある場合は、 [RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter) プロパティを [IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter) インターフェースのインスタンスに設定する必要があります。 RawCustomColorConverter プロパティは、どちらも設定され