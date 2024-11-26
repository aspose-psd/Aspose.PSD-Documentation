---
title: Aspose.PSD for .NET 23.4 - リリースノート
type: docs
weight: 90
url: /ja/net/aspose-psd-for-net-23-4-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)のリリースノートが含まれています。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-1409|公開APIで使用するためにRawColorクラスをデザインする（陳腐なColor構造体の代わりにPSD APIで）|強化|
|PSDNET-1332|Probationからmain Aspose.PSDコードにGradient Map Adjustment Layerを統合する|機能|
|PSDNET-1448|Text Portionsを使用したテキストの編集が正しい結果を保存しない|バグ|
|PSDNET-1449|ITextPortionによるテキストレイヤーの編集時にスタイルや段落の開始と終了位置が正しくない|バグ|
|PSDNET-1509|Photoshopで編集時のフォーマットの移動|バグ|

## **公開APIの変更**
# **追加されたAPI:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- 他省略

# **削除されたAPI:**
- なし

## **使用例:**

**PSDNET-1332。Gradient Map Adjustment LayerをProbationからmain Aspose.PSDコードに統合**

{{< highlight csharp >}}
// 例のコード
{{< /highlight >}}

**PSDNET-1409。公開APIが陳腐なColor構造体の代わりにPSD APIで使用するRawColorクラスをデザイン**

{{< highlight csharp >}}
// 例のコード
{{< /highlight >}}

**PSDNET-1448。Text Portionsを使用したテキストの編集が正しい結果を保存しない**

{{< highlight csharp >}}
// 例のコード
{{< /highlight >}}

**PSDNET-1449。ITextPortionによるテキストレイヤーの編集時にスタイルや段落の開始と終了位置が正しくない**

{{< highlight csharp >}}
// 例のコード
{{< /highlight >}}

**PSDNET-1509。Photoshopで編集時のフォーマットの移動**

{{< highlight csharp >}}
// 例のコード
{{< /highlight >}}