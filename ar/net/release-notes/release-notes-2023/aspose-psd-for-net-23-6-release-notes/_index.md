---
title: تحديث Aspose.PSD لـ .NET 23.6 - ملاحظات الإصدار
type: docs
weight: 70
url: /ar/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD for .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **المفتاح** | **الملخص** | **الفئة** |
|:------------|:------------|:-----------|
| PSDNET-1401 | إعادة هيكلة واجهة برمجة التطبيقات للسجل الزمني | تحسين |
| PSDNET-1517 | إزالة الفنون عند تقديم التشويه | تحسين |
| PSDNET-1528 | تحسين أداء التقديم للتشويه | تحسين |
| PSDNET-147  | دعم طبقة التعديل التكيفية لعتبة الشفافية | ميزة |
| PSDNET-149  | دعم طبقة التعديل اللونية الانتقائية | ميزة |
| PSDNET-801  | القدرة على تصدير السجل الزمني لبرنامج Photoshop لملف Animated Gif | ميزة |
| PSDNET-1555 | إضافة دعم لطبقة النص بدون حدود مستطيلة | ميزة |
| PSDNET-1582 | دعم طبقة الشكل | ميزة |
| PSDNET-864  | إعادة تحميل الصورة في الكائن الذكي لا تحدث التحديث | خطأ |
| PSDNET-1404 | لا يمكن حفظ ملف PSD كملف PSD بالاستثناء التالي: لا يمكن أن يحتوي أوضاع RGB و Lab على أقل من 3 قنوات وأكثر من 4 قنوات | خطأ |
| PSDNET-1546 | الضبط التحقيقي للنص يفقد إذا تم فتح طبقة النص عن طريق وضع التحرير في Photoshop | خطأ |
| PSDNET-1548 | استثناء الإشارة الفارغة عند حفظ ملف PSD | خطأ |
| PSDNET-1578 | استثناء عند تحميل طبقة الشكل: نقاط النشأة الناقصة للنقاط غير مدعومة بعد | خطأ |
| PSDNET-1579 | استثناء عند تحميل VogkResource: يتم حفظ النقاط كـ DoubleStructures ، ونقرأ بوحدات البناء | خطأ |
| PSDNET-1581 | نوع طبقة ShapeLayer فارغ | خطأ |

## **تغييرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة APIs:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopsCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **تمت إزالة APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **أمثلة الاستخدام:**

**PSDNET-147. دعم طبقة التعديل التكيفية لعتبة الشفافية**

{{< highlight csharp >}}
// Your translation here
{{< /highlight >}}

**PSDNET-149. دعم طبقة التعديل اللونية الانتقائية**

{{< highlight csharp >}}
// Your translation here
{{< /highlight >}}

**PSDNET-801. القدرة على تصدير السجل الزمني لبرنامج Photoshop لملف Animated Gif**

{{< highlight csharp >}}
// Your translation here
{{< /highlight >}}

(وَهَلْ لِلْإِنسَانِ إِلَّا مَا سَعَىٰ)
