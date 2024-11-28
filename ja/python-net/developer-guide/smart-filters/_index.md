---
title: Aspose.PSD for PythonでのSmart Filter操作
weight: 100
type: docs
description: PSDファイル内でSmart Filtersを使用する例
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, python, code sample]
url: ja/python-net/smart-filters/
---

## **概要**

Aspose.PSD for PythonでSmart Filtersを適用する3つの方法があります。

## **直接フィルタの適用**

このコードサンプルでは、Aspose.PSD for Pythonでスマートフィルタを直接適用する例が示されています。

まず、コードは元の画像、元画像の出力ファイル、更新された画像の出力ファイルを指定します。

次に、コードはImage.load()メソッドを使用してPSD画像をロードし、PsdImageオブジェクトにキャストします。

元の画像は、出力ファイル名が指定されたsave()メソッドを使用して保存されます。

適用するスマートフィルタを表すSharpenSmartFilterオブジェクトが作成されます。

コードは次に、im.layers[1]を使用してPSD画像から通常のレイヤーを取得します。

ループを使用して、sharpenFilterを通常のレイヤーに3回適用します。

最後に、更新された画像は、save()メソッドを使用して出力ファイル名が指定されたsave()メソッドを使用して保存されます。

このコードは、Aspose.PSD for Pythonでスマートフィルタを直接適用する方法を示しています。適切なフィルタオブジェクトを使用し、それらを必要なレイヤーに適用することで、画像に希望する効果を実現できます。

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **スマートオブジェクト内のSmart Filters操作**

最初に、コードは元の画像、元画像の出力ファイル、更新された画像の出力ファイルを指定します。

PSD画像はImage.load()メソッドを使用してロードされ、その後PsdImageオブジェクトにキャストされます。

元の画像は、出力ファイル名が指定されたsave()メソッドを使用して保存されます。

次に、コードはPSD画像の2番目のレイヤーをSmartObjectLayerオブジェクトにキャストし、スマートオブジェクトレイヤーを表します。

コードは次に、スマートフィルタを編集します。この例では、GaussianBlurSmartFilterとAddNoiseSmartFilterの2種類のスマートフィルタの使用方法が示されています。

GaussianBlurSmartFilterでは、半径、ブレンドモード、不透明度、および有効/無効の値など、フィルタの値が更新されます。

AddNoiseSmartFilterでは、ノイズ分布がNoiseDistribution.UNIFORMに設定されます。

次に、コードはスマートオブジェクトレイヤーに別のGaussianBlurSmartFilterとAddNoiseSmartFilterの2つの新しいフィルタアイテムを追加します。

新しいフィルタを追加した後、update_resource_values()メソッドを使用して変更を適用します。

最後に、コードは、apply()メソッドとapply_to_mask()メソッドを使用してレイヤーとそのマスクにフィルタを直接適用する方法を示します。

更新された画像は、save()メソッドを使用して出力ファイル名が指定されたsave()メソッドを使用して保存されます。

このコードサンプルに従うことで、Aspose.PSD for Pythonでスマートフィルタを使用する方法を学ぶことができます。ライブラリは多くのスマートフィルタを提供しており、それぞれが独自のプロパティとカスタマイズ可能なメソッドを持っており、画像に希望する効果を実現するためにカスタマイズできます。

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **レイヤーマスクにSmart Filtersを適用する**

マスクにSmart Filtersを適用する: 強力な画像編集テクニック

スマートフィルタは、画像編集ソフトウェアの一般的な機能であり、ユーザーが画像にさまざまなフィルタやエフェクトを適用できるようにします。スマートフィルタを使用して達成できる面白いテクニックの1つは、マスクにそれらを適用することです。この記事では、スマートフィルタをマスクに適用する方法を探り、画像編集の世界での使用について説明します。

マスクとは何か？スマートフィルタをマスクに適用する前に、まずマスクが何かを理解しましょう。画像編集では、マスクは特定の部分の画像の透明度を決定するグレースケール画像です。マスクは、画像の特定の部分にフィルタ、調整、または効果を選択的に適用し、他の領域を変更せずに残すために使用できます。

マスクにSmart Filtersを適用する：マスクにSmart Filtersを適用すると、フィルタがマスクで指定された領域にのみ適用されます。これにより、フィルタが画像のどの部分に影響を与えるかを細かく制御できます。マスクを操作することで、フィルタの効果の強度や範囲を決定できます。

前の例と次のメソッドを確認してください：[API Reference Applying Smart Filter To Mask](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
