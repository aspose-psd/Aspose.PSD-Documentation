---
title: Aspose.PSDでのスマートフィルタ操作
weight: 100
type: docs
description: PSDファイルでスマートフィルタを使用する例
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, C#, csharp, code sample]
url: ja/net/smart-filters/
---

## 概要

Aspose.PSD for C# でスマートフィルタを適用する方法は3つあります。

### 直接フィルタの適用

この例では、Aspose.PSD for C# でスマートフィルタを直接適用する方法を示します。

まず、元の画像のソースPSDファイル、元画像用の出力ファイル、更新された画像用の出力ファイルを指定します。

次に、`Image.Load` メソッドを使用してPSD画像をロードし、`PsdImage` オブジェクトにキャストします。

指定された出力ファイル名で `Save` メソッドを使用して元画像を保存します。

適用するスマートフィルタを表す `SharpenSmartFilter` オブジェクトを作成します。

`psdImage.Layers[1]` を使用してPSD画像から通常のレイヤーを取得します。

`sharpenFilter` をループ内で通常のレイヤーに3回適用します。

最後に、指定された出力ファイル名で `Save` メソッドを使用して更新された画像を保存します。

このコードは、Aspose.PSD for C# でスマートフィルタを直接適用する方法を示しています。適切なフィルタオブジェクトを使用して、必要なレイヤーに適用することで、画像に所望の効果を実現できます。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### スマートオブジェクト内のスマートフィルタの操作

この例では、スマートオブジェクト内のスマートフィルタを操作する方法を示しています。

まず、元の画像のソースPSDファイル、元画像用の出力ファイル、更新された画像用の出力ファイルを指定します。

`Image.Load` メソッドを使用してPSD画像をロードし、`PsdImage` オブジェクトにキャストします。

指定された出力ファイル名で `Save` メソッドを使用して元画像を保存します。

PSD画像の2番目のレイヤーを `SmartObjectLayer` オブジェクトにキャストします。

スマートフィルタの編集。この例では `GaussianBlurSmartFilter` と `AddNoiseSmartFilter` の操作方法を示しています。

`GaussianBlurSmartFilter` の場合は、半径、ブレンドモード、不透明度、有効状態などのフィルタ値を更新します。

`AddNoiseSmartFilter` の場合は、ノイズ分布を `NoiseDistribution.UNIFORM` に設定します。

スマートオブジェクトレイヤーに新しいフィルタアイテムを追加します。別の `GaussianBlurSmartFilter` と `AddNoiseSmartFilter` を追加します。

`UpdateResourceValues` メソッドを使用して変更を適用します。

`Apply` メソッドおよび `ApplyToMask` メソッドを使用して、フィルタをレイヤーに直接適用し、フィルタをマスクに適用します。

指定された出力ファイル名で `Save` メソッドを使用して更新された画像を保存します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### レイヤーマスクにスマートフィルタを適用

スマートフィルタは、さまざまなフィルタや効果を適用できる強力な画像編集ツールです。その中でも興味深いテクニックの1つは、フィルタをマスクに適用することです。これにより、フィルタが影響を受けるエリアを正確に制御できます。

マスクは、一部の画像領域の透明度を決定し、フィルタ、調整、または効果を選択的に適用するためのグレースケール画像です。

マスクにスマートフィルタを適用すると、フィルタはマスクで指定された領域にのみ適用されます。この正確な制御により、フィルタの強度や範囲を操作できます。

詳細な情報や例については、[Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/) を参照してください。
