---
title: تحديثات إطلاق Aspose.PSD لـ Java 23.4
type: docs
weight: 40
url: /ar/java/aspose-psd-for-java-23-4-release-notes/
---

{{% alert color="primary" %}} تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD لـ Java 23.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.4/) {{% /alert %}}

|**الرقم**|**الملخص**|**التصنيف**|
| :- | :- | :- |
|PSDJAVA-446|نقل وظائف مفقودة من Aspose.PSD لـ .Net إلى Aspose.PSD لـ Java|تعزيز|
|PSDJAVA-441|تصميم فئة RawColor لاستخدامها في واجهة برمجة التطبيقات العامة في API PSD بدلاً من هيكل اللون القديم|تعزيز|
|PSDJAVA-418|دمج ترخيص Aspose الحديث لـ Aspose.PSD|تعزيز|
|PSDJAVA-445|التنسيق يتحرك عند التحرير في برنامج فوتوشوب|خلل|
|PSDJAVA-443|تحرير النص باستخدام أقسام النص لا يحفظ النتيجة الصحيحة|خلل|
|PSDJAVA-444|ظهور بداية ونهاية الأنماط أو الفقرات في المكان غير الصحيح عند تحرير طبقة النص بواسطة ITextPortion|خلل|

# **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المضافة:**
- M:com.aspose.psd.FontSettings.getFontReplacements(java.lang.String)
- M:com.aspose.psd.FontSettings.getReplacementFont(java.lang.String)
- M:com.aspose.psd.FontSettings.setAllowedFonts(java.lang.String[])
- M:com.aspose.psd.FontSettings.setFontReplacements(java.lang.String,java.lang.String[])
- M:com.aspose.psd.FontSettings.isFontAllowed(java.lang.String)
- M:com.aspose.psd.License.setLicense(java.io.File)
- M:com.aspose.psd.License.getRenewSubscriptionStartMessage
- M:com.aspose.psd.License.getErrorCodeMessages
- M:com.aspose.psd.License.removeLicense
- T:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.#ctor(int,int,com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getPsdVersion
- ...

# **API المحذوفة:**
- M:com.aspose.psd.FontSettings.addFontsFolder(java.lang.String)
- M:com.aspose.psd.FontSettings.removeFontsFolder(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.saveData(java.io.OutputStream)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lfx2Resource.getBlendMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lfx2Resource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lfx2Resource.getEffectColor
- ...

# **أمثلة الاستخدام:**

**PSDJAVA-446. نقل وظائف مفقودة من Aspose.PSD لـ .Net إلى Aspose.PSD لـ Java**

الرجاء التحقق من <a href="https://reference.aspose.com/psd/java/">مرجع API لـ Aspose.PSD لـ Java</a>. لم يتم نسخ جميع أمثلة استخدام API الجديدة واختبارها بعد.

{{< highlight java >}}        
        // سيتم توفير الأمثلة لاحقًا.
{{< /highlight >}}

**PSDJAVA-441. تصميم فئة RawColor لاستخدامها في واجهة برمجة التطبيقات العامة لاستخدامها في واجهة برمجة التطبيقات PSD بدلاً من هيكل اللون القديم**

{{< highlight java >}}
    PixelDataFormat rgb32Bpp = PixelDataFormat.getRgb32Bpp();
    RawColor color = new RawColor(rgb32Bpp);
    Color oldColor = Color.fromArgb(5, 1, 2, 3);

    int argbValue = oldColor.toArgb();
    color.setAsInt(argbValue);

    Assertions.assertEquals("ARGB", color.getColorModeName());
    Assertions.assertEquals(32, color.getBitDepth());
    Assertions.assertEquals("A Alpha", color.getComponents()[0].getFullName());
    Assertions.assertEquals(5, (int)color.getComponents()[0].getValue());
    Assertions.assertEquals("R Red", color.getComponents()[1].getFullName());
    Assertions.assertEquals(1, (int)color.getComponents()[1].getValue());
    Assertions.assertEquals("G Green", color.getComponents()[2].getFullName());
    Assertions.assertEquals(2, (int)color.getComponents()[2].getValue());
    Assertions.assertEquals("B Blue", color.getComponents()[3].getFullName());
    Assertions.assertEquals(3, (int)color.getComponents()[3].getValue());

    Assertions.assertEquals(argbValue, color.getAsInt());
{{< /highlight >}}

**PSDJAVA-445. التنسيق يتحرك عند التحرير في برنامج فوتوشوب**

{{< highlight java >}}
    // الكود المقصود يتم توفيره في وقت لاحق.
{{< /highlight >}}

**PSDJAVA-443. تحرير النص باستخدام أقسام النص لا يحفظ النتيجة الصحيحة**

{{< highlight java >}}
    // الكود المقصود يتم توفيره في وقت لاحق.
{{< /highlight >}}

**PSDJAVA-444. ظهور بداية ونهاية الأنماط أو الفقرات في المكان غير الصحيح عند تحرير طبقة النص بواسطة ITextPortion**

{{< highlight java >}}
    // الكود المقصود يتم توفيره في وقت لاحق.
{{< /highlight >}}