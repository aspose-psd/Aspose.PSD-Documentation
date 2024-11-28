---
title: Aspose.PSD for Java でのスマートフィルタ操作
weight: 100
type: docs
description: PSD ファイルでスマートフィルタを使用する例
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, java, code sample]
url: ja/java/smart-filters/
---

## **概要**

Aspose.PSD for Java でスマートフィルタを適用するための 3 つのメソッドがあります。

## **スマートフィルタの直接適用**

このコードサンプルは、Aspose.PSD for Java でスマートフィルタを直接適用する方法を示しています。

まず、コードはソース PSD ファイル、元の画像の出力ファイル、および更新された画像の出力ファイルを定義します。

次に、Image.load() メソッドを使用して PSD 画像を読み込み、それを PsdImage オブジェクトにキャストします。

元の画像は、出力ファイル名を指定して save() メソッドを使用して保存されます。

SharpenSmartFilter オブジェクトは、希望するスマートフィルタを表すためにインスタンス化されます。

その後、psdImage.getLayers()[1] を使用して PSD 画像から通常のレイヤーを取得します。

ループを使用して、sharpenFilter を通常のレイヤーに 3 回適用します。

最後に、更新された画像は、出力ファイル名を指定して save() メソッドを使用して保存されます。

このコードは、Aspose.PSD for Java でスマートフィルタを直接適用する方法を示しています。適切なフィルタオブジェクトを使用して、画像に望ましい効果を適用することができます。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## **スマートオブジェクト内のスマートフィルタの操作**

このコードスニペットは、Aspose.PSD for Java でスマートオブジェクト内のスマートフィルタを操作する方法を概説しています。

最初に、コードはソース PSD ファイル、元の画像の出力ファイル、および更新された画像の出力ファイルを定義します。

PSD 画像は、Image.load() メソッドを使用して読み込まれ、次に PsdImage オブジェクトにキャストされます。

元の画像は、出力ファイル名を指定して save() メソッドを使用して保存されます。

次に、コードは PSD 画像の 2 番目のレイヤーを SmartObjectLayer オブジェクトにキャストし、スマートオブジェクトレイヤーを表します。

その後、コードは GaussianBlurSmartFilter および AddNoiseSmartFilter の 2 つのタイプを示す、スマートフィルタの編集を示しています。

GaussianBlurSmartFilter の場合、コードは半径、ブレンドモード、不透明度、およびアクティベーションステータスなどのフィルタ値を更新します。

AddNoiseSmartFilter の場合、コードはノイズ分布を NoiseDistribution.Uniform に設定します。

その後、コードはスマートオブジェクトレイヤーに新しいフィルタアイテムを 2 つ追加します。これは、別の GaussianBlurSmartFilter と AddNoiseSmartFilter です。

新しいフィルタを追加した後、updateResourceValues() メソッドを使用して変更を適用します。

最後に、コードは、レイヤーとそのマスクにフィルタを直接適用し、それぞれ apply() メソッドと applyToMask() メソッドを使用します。

更新された画像は、出力ファイル名を指定して save() メソッドを使用して保存されます。

このコードサンプルに従うことで、Aspose.PSD for Java でスマートオブジェクト内のスマートフィルタを操作する方法が理解できます。ライブラリにはさまざまなスマートフィルタが用意されており、それぞれが独自のプロパティとカスタマイズ可能なメソッドセットを持っており、画像に望ましい効果を実現することができます。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## ** レイヤーマスクへのスマートフィルタの適用 **

マスクへのスマートフィルタの適用：効果的な画像編集テクニック

画像編集ソフトウェアで一般的なスマートフィルタを使用することで、ユーザーは画像にさまざまなフィルタや効果を適用することができます。スマートフィルタによって可能になる興味深いテクニックの1つは、それらをマスクに適用することです。この記事では、マスクにスマートフィルタを適用する方法を探り、画像編集の領域でのその有用性について論じます。

マスクの理解：マスクにスマートフィルタを適用する前に、マスクの概念を把握することが重要です。画像編集では、マスクは画像内の特定の領域の透明度を指定するグレースケール画像です。マスクを使用すると、画像の特定の部分にのみフィルタ、調整、または効果を選択的に適用できます。

マスクへのスマートフィルタの適用：マスクにスマートフィルタを適用すると、マスクで指定された領域のみに影響を与えます。これにより、フィルタの効果の強度や範囲を調整することができます。

前の例とメソッドを参照してください：[API リファレンス マスクにスマートフィルタを適用する](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

