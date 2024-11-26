---
title: Aspose.PSD for .NET 20.7 - リリースノート
type: docs
weight: 60
url: /ja/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-673|LnkE リソースのサポート|機能|
|PSDNET-392|britResource のサポート (明るさ/コントラスト調整レイヤーのリソース)|機能|
|PSDNET-629|非サポートの形式を画像として開こうとした際の例外メッセージの変更|改良|
|PSDNET-594|LayerMask の保存に失敗|バグ|
|PSDNET-597|新しいレイヤーグループを作成してから PSD ファイルを保存すると Photoshop 警告が表示される|バグ|
|PSDNET-618|フォルダにクリッピングマスクが適用されない|バグ|
|PSDNET-625|Aspose.PSD for .NET でファイルを開けない|バグ|
|PSDNET-650|PSD を PDF に変換する際に画像保存に失敗する例外|バグ|
|PSDNET-655|Clipping パスが PSD 画像で無効になるrop 操作|バグ|
|PSDNET-662|Shadow Effect 付きの特定の PSD ファイルを保存しようとした際の NullReference 例外|バグ|
|PSDNET-666|Image.CanLoad(pdfStream) で Aspose.PSD が true を返す|バグ|
|PSDNET-676|生成された PNG でレイヤーがレンダリングされない|バグ|
|PSDNET-677|TextData へのアクセス時の例外|バグ|
|PSDNET-679|PSD を保存する際の ImageSaveException|バグ|

## **パブリック API 変更**
# **追加された API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **削除された API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **使用例:**
**PSDNET-606. LnkE リソースのサポート**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-201. ドキュメント変換進行状況のサポート**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-386. britResource (明るさ/コントラスト調整レイヤーのリソース) のサポート**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-596. パススルーブレンディングモードを持つレイヤーグループがレンダリングされない**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-610. 特定の Psd ファイルを画像に変換しようとした際の NullReference 例外**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-636. マスクに空の境界がある調整レイヤーが含まれる場合、PSD ファイルのリサイズが正しく機能しない**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-611. 特定の Psd ファイルを開こうとした際の OverflowException**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-565. RGB モードの 16 ビット/チャンネルを持つ Psd 画像がプレビューのみでレイヤーを更新**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-652. 複合 LnkE リソースと adobeStockLicenseState プロパティを持つ特定の PSD ファイルをロードした際の例外**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDNET-638. 空のレイヤーグループにレイヤーグループを追加した後の不正なレイヤー順**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}

**PSDBET-219. DefaultReplacementFont 設定を ImageOptionsBase クラスに移動**

{{< highlight csharp >}}
// コードの挿入
{{< /highlight >}}