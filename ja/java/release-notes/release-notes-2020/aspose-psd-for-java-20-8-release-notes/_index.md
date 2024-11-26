---
title: Aspose.PSD for Java 20.8 - リリースノート
type: docs
weight: 50
url: /ja/aspose-psd-for-java-20-8-release-notes/
---

{{% alert color="primary" %}} このページには、[Aspose.PSD for Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) のリリースノートが含まれています。{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDJAVA-264|SoLdResource（Smart Object Layer Dataリソース）のサポート|機能|
|PSDJAVA-263|PlLdResource（Smart Object Layer用の置かれたレイヤリソース）のサポート|機能|
|PSDJAVA-262|オブジェクト配列およびユニット配列構造のサポートを追加：ObAr / UnFlシグネチャ|機能|
|PSDJAVA-265|Asposeで保存されたファイルでテキストのフォーカスを当てると下線と取り消し線が失われる|バグ|
|PSDJAVA-257|CMYK ColorModeで保存した16ビット/チャンネルの変更されたPSD画像の保存を修正|バグ|
|PSDJAVA-268|リグレッション：Aspose.PSD 20.7.0は古いファイルのフォントサイズを壊す|バグ|

# **パブリックAPIの変更**
# **追加されたAPI:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.ImageStack
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Raster
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Unknown
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Vector
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.AntiAliasPolicyKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure.StructureKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure.StructureKey
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ClassID.#ctor(byte[],boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getAntiAliasPolicy
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.その他のメソッド
- T:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType

# **使用例:**

**PSDJAVA-264. SoLdResource（Smart Object Layer Dataリソース）のサポート**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}}

**PSDJAVA-263. PlLdResource（Smart Object Layer用の置かれたレイヤーリソース）のサポート**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}} 

**PSDJAVA-262. Object ArrayおよびUnit Array構造のサポート: ObAr / UnFlシグネチャ**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}}

**PSDJAVA-265. Aspose.PSDで保存したファイルでフォーカスを合わせた後に下線と取り消し線がなくなる問題**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}}

**PSDJAVA-257. CMYK ColorMode 16ビット/チャンネルの変更されたPSD画像の保存修正**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}}

**PSDJAVA-268. リグレッション：Aspose.PSD 20.7.0は古いファイルのフォントサイズを壊す**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}}**PSDJAVA-257. CMYK ColorMode 16ビット/チャンネルの変更されたPSD画像の保存修正**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}}

**PSDJAVA-268. リグレッション：Aspose.PSD 20.7.0は古いファイルのフォントサイズを壊す**
{{< highlight java >}}
*上記の使用例*
{{< /highlight >}}