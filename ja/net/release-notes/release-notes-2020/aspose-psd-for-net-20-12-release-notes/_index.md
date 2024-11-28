---
title: Aspose.PSD for .NET 20.12 - リリースノート
type: docs
weight: 10
url: /ja/net/aspose-psd-for-net-20-12-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 20.12](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-757|レイヤーをスマートオブジェクトレイヤーに変換するサポート|機能|
|PSDNET-764|PSBファイルを追加しようとすると、SmartObjectLayer.ReplaceContentsメソッドがNullReferenceExceptionをスローする|バグ|
|PSDNET-773|レイヤーがキャンバスよりも大きい場合にCMYK 8ビットおよびCMYK 16ビット画像の描画が不正確|バグ|
|PSDNET-782|保存されたPSBファイルはAPIで開くことができますが、Photoshopでは開くことができません|バグ|
|PSDNET-783|特定のPSDで共有データソースを使用すると、共有データソースを変更しようとすると例外が発生する|バグ|
|PSDNET-172|混乱を避けるためにFileFormatVersionをPsdVersionに改名|強化|
|PSDNET-620|Aspose.PSD .NETからCompactフレームワーク構成を削除|強化|
|PSDNET-765|SmartObjectLayersを含むPSBファイルを開こうとするとPsdImageException: 未知のリソースヘッダー|強化|
|PSDNET-798|Aspose.PSDおよびAspose.Imaging製品の一貫性を保証するために、Vector MaskクラスのヒエラルキーをCore Namespaceに移動|強化|

## **パブリックAPIの変更**
# **追加されたAPI:**
- T:Aspose.PSD.FileFormats.Psd.PsdVersion
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.PsdVersion
- T:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord
...

## **使用例:**
**PSDNET-757. レイヤーをスマートオブジェクトレイヤーに変換するサポート**
{{< highlight csharp >}}
            // 以下の例は、PSDファイル内のレイヤーをスマートオブジェクトレイヤーに変換する方法を示しています
            // ...
{{< /highlight >}}

**PSDNET-764. SmartObjectLayer.ReplaceContentsメソッドがPSBファイルを追加しようとするとNullReferenceExceptionをスローする**
{{< highlight csharp >}}
            // ...
{{< /highlight >}}

**PSDNET-765. SmartObjectLayersを含むPSBファイルを開こうとするとPsdImageException: 未知のリソースヘッダー**
{{< highlight csharp >}}
            // ...
{{< /highlight >}}

**PSDNET-773. レイヤーがキャンバスよりも大きい場合にCMYK 8ビットおよびCMYK 16ビット画像の描画が不正確**
{{< highlight csharp >}}
            // ...
{{< /highlight >}}

**PSDNET-782. 保存されたPSBファイルはAPIで開くことができますが、Photoshopでは開くことができません**
{{< highlight csharp >}}
            // ...
{{< /highlight >}}

**PSDNET-783. 特定のPSDで共有データソースを使用すると、共有データソースを変更しようとすると例外が発生する**
{{< highlight csharp >}}
            // ...
{{< /highlight >}}