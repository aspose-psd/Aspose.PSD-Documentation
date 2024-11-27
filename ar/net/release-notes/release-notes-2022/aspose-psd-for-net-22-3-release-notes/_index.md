---
title: أسبوز بي.اس.دي لـ 22.3 - ملاحظات الإصدار
type: docs
weight: 100
url: /ar/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [أسبوز بي.اس.دي لـ .نت 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-210|إضافة خاصية IsOpen لمجموعة الطبقات|ميزة|
|PSDNET-643| تجاهل قناع الطبقة النقطية في صورة PSD عند الحفظ في صورة PSD بعمق 16 بت|علة|
|PSDNET-899| لا تطبق وضع الدمج Dissolve على المجلد مع القناع|علة|
|PSDNET-1047| لا يمكن فتح الملف المعين بواسطة فوتوشوب بعد الحفظ في أسبوز بي.اس.دي 21.11|علة|
|PSDNET-1068| عرض غير صحيح للطبقة بوضع الدمج الخطي Dodge (Add)|علة|
|PSDNET-1069| تثير طبقة ملء النمط استثناءً عند التحديث بعد التحميل|علة|


## **تغييرات واجهة التطبيق العمومية**
# **APIs المضافة:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **APIs المحذوفة:**
- لا شيء


## **أمثلة الاستخدام:**

**PSDNET-210. إضافة خاصية IsOpen لمجموعة الطبقات**

{{< highlight csharp >}}
// مثال على قراءة وكتابة خاصية IsOpen أثناء التشغيل.
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. تجاهل قناع الطبقة النقطية في صورة PSD عند الحفظ في صورة PSD بعمق 16 بت**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. لا تطبق وضع الدمج Dissolve على المجلد مع القناع**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. لا يمكن فتح الملف المعين بواسطة فوتوشوب بعد الحفظ في أسبوز بي.اس.دي 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // تحتاج إلى فتح ملف PSD الناتج يدويًا باستخدام فوتوشوب.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // لا توجد استثناءات.
            }
{{< /highlight >}}

**PSDNET-1068. عرض غير صحيح للطبقة بوضع الدمج الخطي Dodge (Add)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. تثير طبقة ملء النمط استثناءً عند التحديث بعد التحميل**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}