---
title: メディアンフィルタとワイナーフィルタの適用
type: docs
weight: 10
url: /ja/net/applying-median-and-wiener-filters/
---

## **メディアンフィルタとワイナーフィルタの適用**
メディアンフィルタは非線形のデジタルフィルタリング手法であり、しばしばノイズを除去するために使用されます。このようなノイズ低減は通常、後続処理の結果を改善するための典型的な前処理手法です。ワイナーフィルタは、付加的なノイズとぼかしによって劣化した画像に対して、MSE（平均二乗誤差）最適な定常線形フィルタです。Aspose.PSDフィルターは.NET API開発者が画像にメディアンフィルタを適用し、画像にガウス・ワイナーフィルタを適用できるようにします。この記事では、メディアンフィルタとガウス・ワイナーフィルタの画像への適用方法を説明します。

### **メディアンフィルタの適用**
Aspose.PSDは、[MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions)クラスを提供して、[RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)にフィルタを適用します。以下に示すコードスニペットでは、ラスター画像にメディアンフィルタを適用する方法が示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}

### **ガウス・ワイナーフィルタの適用**
Aspose.PSDは、[GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)クラスを提供して、[RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)にフィルタを適用します。以下に示すコードスニペットでは、ラスター画像にガウス・ワイナーフィルタを適用する方法が示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}

### **カラー画像にガウス・ワイナーフィルタを適用する**
Aspose.PSDは、カラー画像に対しても[GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)を提供しています。以下に示すコードスニペットでは、カラー画像にガウス・ワイナーフィルタを適用する方法が示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}

### **モーション・ワイナーフィルタの適用**
Aspose.PSDは、[MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions)クラスを提供して、[RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)にフィルタを適用します。以下に示すコードスニペットでは、ラスター画像にモーション・ワイナーフィルタを適用する方法が示されています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}

## **画像に補正フィルタを適用する**
この記事では、Aspose.PSD for .NETを使用して画像に補正フィルタを適用する方法を示しています。Aspose.PSD APIは、この目標を達成するための効率的で使いやすいメソッドを公開しています。Aspose.PSD for .NETは、[BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)および[SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions)クラスをフィルトレーション用に公開しています。 BilateralSmoothingFilterOptionsクラスにはサイズとして整数が必要です。リサイズを実行する手順は以下の通りです:

1. Imageクラスによって公開された工場メソッドLoadを使用して画像を読み込みます。
2. 画像をRasterImageに変換します。
3. BilateralSmoothingFilterOptionsクラスとSharpenFilterOptionsクラスのインスタンスを作成します。
4. RasterImage.Filterメソッドを呼び出し、画像の境界を指定してBilateralSmoothingFilterOptionsクラスのインスタンスを指定します。
5. RasterImage.Filterメソッドを呼び出し、画像の境界を指定してSharpenFilterOptionsクラスのインスタンスを指定します。
6. コントラストを調整します。
7. 明るさを設定します。
8. 結果を保存します。

## **Bradleyの閾値アルゴリズムを使用する**
画像の閾値処理は、グラフィックアプリケーションで使用されます。画像の閾値処理の目的は、ピクセルを「暗い」または「明るい」に分類することです。Aspose.PSD APIでは、画像を変換する際にBradleyの閾値処理を使用できます。次のコードスニペットは、閾値値を定義し、その後Bradleyの閾値アルゴリズムを呼び出す方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
