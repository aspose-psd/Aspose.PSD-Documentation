---
title: Aspose.PSD için .NET 20.8 - Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-20-8-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa [Aspose.PSD için .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-390|PlLdResource'un (Akıllı Nesne Katmanı için yerleştirilmiş katman kaynağı) desteklenmesi|Özellik|
|PSDNET-400|SoLdResource'un (Akıllı Nesne Katmanı Veri kaynağı) desteklenmesi|Özellik|
|PSDNET-693|ObAr / UnFl imzaları için Nesne Dizisi ve Birim Dizisi yapılarının desteği eklendi|Özellik|
|PSDNET-600|CMYK Renk Modu 16 bit kanalı olan değiştirilmiş PSD görüntüsünün kaydedilme hatası düzeltildi|Hata|
|PSDNET-664|Aspose.PSD ile kaydedilen dosyada metne odaklandıktan sonra alt çizgi ve üst çizgi kaybı yaşanması sorunu düzeltildi|Hata|
|PSDNET-710|Regresyon: Aspose.PSD 20.7.0 eski dosyalarda font boyutlarını bozuyor|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Structures
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitTypes,System.Double[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.UnitType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Values
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.ValueCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures```csharp
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TypeToolKey

# **Kaldırılan API'lar:**
- Yok

## **Kullanım örnekleri:**
**PSDNET-390. PlLdResource'un (Akıllı Nesne Katmanı için yerleştirilmiş katman kaynağı) desteklenmesi**
{{< highlight csharp >}}        
        void AssertAreEqual(object actual, object expected)
        {
            var areEqual = object.Equals(actual, expected);
            if (!areEqual && actual is Array && expected is Array)
            {
                var actualArray = (Array)actual;
                var expectedArray = (Array)actual;
                if (actualArray.Length == expectedArray.Length)
                {
                    for (int i = 0; i < actualArray.Length; i++)
                    {
                        if (!object.Equals(actualArray.GetValue(i), expectedArray.GetValue(i)))
                        {
                            break;
                        }
                    }

                    areEqual = true;
                }
            }

            if (!areEqual)
            {
                throw new FormatException(
                    string.Format("Gerçek değer {0}, beklenen {1} ile eşit değil.", actual, expected));
            }
        }

        string dataDir = "PSDNET390_1\\";
        var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";
        var outputFilePath = dataDir + "LayeredSmartObjects8bit2_output.psd";
        var expectedValues = new object[]
        {
            new object[]
            {
                true,
                "76f05a3b-7523-5e42-a1bb-27f4735bffa0",
                1,
                1,
                0x10,
                PlacedLayerType.Raster,
                new double[8]
                {
                    29.937922786050663,
                    95.419959734187131,
                    126.85445817782261,
                    1.0540625423957124,
                    172.20861031651307,
                    47.634102808208553,
                    75.292074924741144,
                    142
                },
                0d,
                0d,
                0d,
                0d,
                0d,
                149d,
                310d,
                4,
                4,
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d
                },
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0d, 0.0d, 0.0d, 0.0d,
                    49.666666666666664d, 49.666666666666664d, 49.666666666666664d, 49.666666666666664d,
                    99.333333333333329d, 99.333333333333329d, 99.333333333333329d, 99.333333333333329d,
                    149, 149, 149, 149,
                },
            },
            new object[]
            {
                true,
                "cf0477a8-8f92-ac4f-9462-f78e26234851",
                1,
                1,
                0x10,
``` 