```md
---
title: ملاحظات الإصدار لـ Aspose.PSD لـ .NET 22.2
type: docs
weight: 110
url: /ar/net/aspose-psd-for-net-22-2-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 22.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-1032|إضافة دعم لـ .Net 6|تحسين|
|PSDNET-142|دعم طبقات تعديل النغمة (Vibrance)|ميزة|
|PSDNET-396|دعم مورد vibAResource|ميزة|
|PSDNET-1057|إنشاء مثال على إضافة عوامل تصفية ذكية مخصصة لا تتمتع بالدعم في Aspose.PSD|ميزة|
|PSDNET-642|قناع الطبقة النقطية المعطلة لا يقوم بالعرض بشكل صحيح|خلل|
|PSDNET-644|استثناء عند تغيير حجم ملفات PSD بعمق 16 بت لكل قناة مع قناع نقطي|خلل|


## **تغييرات الواجهة البرمجية العامة**
### الواجهات الجديدة:
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddVibranceAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.VibranceLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.VibranceLayer.Vibrance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.VibranceLayer.Saturation
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Vibrance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Saturation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.Distribution
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.AmountNoise
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.IsMonochromatic
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.Radius
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.NoiseDistribution.Uniform
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.NoiseDistribution.Gaussian
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.SourceDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.Name
- P:Aspose.P