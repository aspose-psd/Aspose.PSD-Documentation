---
title: تحديثات Aspose.PSD لـ .NET 20.2
type: docs
weight: 110
url: /ar/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 


|الرقم|الملخص|الفئة|
| :- | :- | :- |
|PSDNET-206|تحسين القدرة على عرض نصوص مختلفة الألوان في طبقة النص|ميزة|
|PSDNET-369|دعم مورد ال layer clbl (الطبقة تحتوي على معلومات حول عناصر القص) |ميزة|
|PSDNET-274|دعم مورد ال blwh (المورد يحتوي على بيانات طبقة التعديل الأبيض والأسود)|ميزة|
|PSDNET-230|القدرة على تصدير مجموعة الطبقات إلى Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|ميزة|
|PSDNET-372|دعم مورد lspf (يحتوي على إعدادات حول ضبط الطبقة المحمية)|ميزة|
|PSDNET-370|دعم مورد infx (يحتوي على بيانات حول خلط العناصر الداخلية)|ميزة|
|PSDNET-251|إعادة هيكلة PsdImage و Layer لتغيير سلوك التحويل (تغيير تغييرات الحجم/الدوران/القص الصحيحة لأقنعة الطبقة إذا قمنا بتحويل طبقة واحدة بشكل منفصل)|تحسين|
|PSDNET-276|في بعض إعدادات عالمنة، لا يمكن فتح صورة النقطية المتجاورة لصورة الذكاء الاصطناعي|خلل|
|PSDNET-194|بعد أداء عملية FlipRotate على الطبقة، تصبح صورة PSD غير قابلة للقراءة|خلل|
|PSDNET-177.|System.ArgumentException أثناء تحميل ملف PSD|خلل|
|PSDNET-249|بعد استخدام طريقة تحويل لطبقة فقط، تحتوي الطبقة المحفوظة على حدود غير صحيحة أو قناع|خلل|

## الواجهة البرمجية العامة

### الواجهات الجديدة:
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- .. (تم حذف الأسطر للتقليل من الطول)

### الواجهات المحذوفة:
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- .. (تم حذف الأسطر للتقليل من الطول)

## أمثلة الاستخدام

### PSDNET-206. تحسين القدرة على عرض نصوص مختلفة الألوان في طبقة النص

{{< highlight java >}}

    استخدم (var psdImage = (PsdImage)Image.Load("text_ethalon_different_colors.psd"))

{

    var txtLayer = (TextLayer)psdImage.Layers[1];

    txtLayer.TextData.UpdateLayerData();

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}