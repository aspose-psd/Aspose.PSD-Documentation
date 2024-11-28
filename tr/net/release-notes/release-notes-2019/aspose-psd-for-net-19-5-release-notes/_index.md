---
title: Aspose.PSD for .NET 19.5 - Sürüm Notları
type: docs
weight: 80
url: /tr/net/aspose-psd-for-net-19-5-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, Aspose.PSD for .NET 19.5 için sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-133|Dolgu Katmanlarının Desteğini Ekle: Desen|Özellik|
|PSDNET-138|PtFlResource Desteğini Ekle|Özellik|
|PSDNET-129|PSD dosyaları için Doğru Kırpma yöntemini uygula|Özellik|
|PSDNET-140|VsmsResource Desteğini Ekle|Özellik|
|PSDNET-121|Görünmez Klasörde Görünmez Alt Klasördeki Görünür Katmanlar, render edilir ancak olmamalı.|Hata|
|PSDNET-119|PSD (Kanal başına 16 bitlik RGB modu) doğru şekilde JPEG'e dönüştürülmemiş|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternHeight
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternHeight
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.#ctor(System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Offset
- ...

## **Kullanım örnekleri:**
**PSDNET-133. Dolgu katmanlarının Desteğini Ekle: Desen**

{{< highlight java >}}

 // Dolgu katmanlarının Desteğini Ekle: Desen

    string sourceFileName = "PatternFillLayer.psd";

    string exportPath = "PatternFillLayer_Edited.psd";

    double tolerance = 0.0001;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

         foreach (var layer in im.Layers)

         {

             if (layer is FillLayer)

             {

                  FillLayer fillLayer = (FillLayer)layer;

                  PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                  if (fillSettings.HorizontalOffset != -46 || 

                      fillSettings.VerticalOffset != -45 || 

                      fillSettings.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      fillSettings.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      ...
{{< /highlight >}}