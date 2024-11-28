---
title: ストローク効果とカラーフィルで
type: ドキュメント
weight: 60
url: /ja/net/stroke-effect-with-color-fill/
---

## **ストローク効果とカラーフィル**
この記事では、ストローク効果をカラーフィルでレンダリングする方法について説明します。 ストローク効果は、レイヤーとシェイプにストロークとボーダーを追加するために使用されます。 これを使用して、単色の線、カラフルなグラデーション、およびパターン化されたボーダーを作成できます。

ストローク効果をカラーフィルでレンダリングする手順は以下の通りです:

- [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource)プロパティを設定します。
- [**Image**クラスによって公開されたLoadファクトリーメソッドを使用して、PSDファイルを画像としてロードし、[**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions)を定義します。
- [**ColorFillSetting**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)の設定プロパティを設定します。
- 結果を保存します。

次のコードスニペットは、ストローク効果をカラーフィルでレンダリングする方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
