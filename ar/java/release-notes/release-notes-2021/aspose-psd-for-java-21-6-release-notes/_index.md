---
title: أسبوز.PSD لجافا 21.6 - ملاحظات الإصدار
type: docs
weight: 40
url: /ar/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} تحتوي هذه الصفحة على ملاحظات الإصدار لـ [أسبوز.PSD لجافا 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

| **المفتاح** | **الملخص** | **الفئة** |
| :- | :- | :- |
|PSDJAVA-351| لا يتم عرض تقنية القصاصة لمجموعة بشكل صحيح | خلل |
|PSDJAVA-352| تتم تجاهل القناع العادي أو الناقل لمجموعة الطبقة عند العرض | خلل |
|PSDJAVA-353| PSD الصورة مع تعطيل قناع طبقات الناقل عند الحفظ يمكن أن يتيح القناع الناقل | خلل |
|PSDJAVA-354| استثناء عند إنشاء طبقة نص بنص أطول من 255 حرفًا | خلل |

# **تغييرات واجهة برمجة التطبيقات العامة**
# **الواجهات البرمجية المضافة:**
- لا شيء

# **الواجهات البرمجية المحذوفة:**
- لا شيء

# **أمثلة الاستخدام:**

**PSDJAVA-351. لا يتم عرض تقنية القصاصة لمجموعة بشكل صحيح**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. تتم تجاهل القناع العادي أو الناقل لمجموعة الطبقة عند العرض**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. PSD الصورة مع تعطيل قناع طبقات الناقل عند الحفظ يمكن أن يتيح القناع الناقل**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. استثناء عند إنشاء طبقة نص بنص أطول من 255 حرفًا**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}