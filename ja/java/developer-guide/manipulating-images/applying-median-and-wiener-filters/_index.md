---
title: メディアンフィルターとWienerフィルターの適用
type: ドキュメント
weight: 10
url: /ja/java/applying-median-and-wiener-filters/
---

## **メディアンフィルターとWienerフィルターの適用**
メディアンフィルターは非線形デジタルフィルタリング技術であり、ノイズを除去するためにしばしば使用されます。このようなノイズ低減は、後続の処理の結果を改善する典型的な前処理ステップです。Wienerフィルターは、加法ノイズとぼかしが加わった画像に対してMSE（平均二乗誤差）最適な静止線形フィルターです。Aspose.PSD for Java APIを使用すると、開発者は画像にメディアンフィルターを適用したり、画像にガウス・ウィーナーフィルターを適用したりできます。この記事では、画像にメディアンフィルターとガウス・ウィーナーフィルターを適用する方法を示します。

### **メディアンフィルターの適用**
Aspose.PSDでは、MedianFilterOptionsクラスを提供して、RasterImageにフィルターを適用できます。以下に示すコードスニペットは、ラスター画像にメディアンフィルターを適用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **ガウス・ウィーナーフィルターの適用**
Aspose.PSDでは、GaussWienerFilterOptionsクラスを提供して、RasterImageにフィルターを適用できます。以下に示すコードスニペットは、ラスター画像にガウス・ウィーナーフィルターを適用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **カラー画像にガウス・ウィーナーフィルターの適用**
Aspose.PSDでは、カラー画像にもGaussWienerFilterOptionsを提供しています。以下に示すコードスニペットは、カラー画像にガウス・ウィーナーフィルターを適用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **モーション・ウィーナーフィルターの適用**
Aspose.PSDでは、MotionWienerFilterOptionsクラスを提供して、RasterImageにフィルターを適用できます。以下に示すコードスニペットは、ラスター画像にモーション・ウィーナーフィルターを適用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **画像に補正フィルターを適用**
この記事では、Aspose.PSD for Javaを使用して画像に補正フィルターを適用する方法を示します。Aspose.PSD APIでは、この目標を達成するために効率的で使いやすいメソッドが公開されています。Aspose.PSD for Javaでは、BilateralSmoothingFilterOptionsおよびSharpenFilterOptionsクラスがフィルトレーションのために公開されています。BilateralSmoothingFilterOptionsクラスはサイズを整数として必要とします。リサイズを実行する手順は以下のとおりです。

1. Imageクラスが公開するLoadファクトリーメソッドを使用して画像を読み込みます。
1. 画像をRasterImageに変換します。
1. BilateralSmoothingFilterOptionsおよびSharpenFilterOptionsクラスのインスタンスを作成します。
1. RasterImage.Filterメソッドを呼び出し、イメージ境界を指定し、BilateralSmoothingFilterOptionsクラスのインスタンスを指定します。
1. RasterImage.Filterメソッドを呼び出し、イメージ境界を指定し、SharpenFilterOptionsクラスのインスタンスを指定します。
1. コントラストを調整します。
1. 明るさを設定します。
1. 結果を保存します。

以下のコードスニペットは、補正フィルターを適用する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **Bradley閾値アルゴリズムを使用**
画像の閾値処理は、グラフィックアプリケーションで使用されます。画像の閾値処理の目的は、ピクセルを「暗い」と「明るい」のどちらかに分類することです。Aspose.PSD APIを使用すると、画像を変換する際にBradleyの閾値処理を使用することができます。以下のコードスニペットは、閾値値を定義し、Bradleyの閾値アルゴリズムを呼び出す方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
