---
title: أصدر Aspose.PSD للجافا 20.7 - ملاحظات الإصدار
type: docs
weight: 50
url: /ar/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}}
هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD للجافا 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) 
{{% /alert %}}

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDJAVA-231|دعم إضافة تأثير الحدود أثناء التشغيل|ميزة|
|PSDJAVA-249|دعم موارد lnk2 / lnk3 (موارد طبقة الكائن الذكي)|ميزة|
|PSDJAVA-247|تغيير رسالة الاستثناء عند محاولة فتح تنسيقات غير مدعومة كصورة|تحسين|
|PSDJAVA-235|إذا قمنا بحفظ ملف PSD بعد إنشاء مجموعة طبقات جديدة نحصل على تحذير من فوتوشوب عند فتح الملف.|خلل|
|PSDJAVA-236|فشل حفظ قناع الطبقة|خلل|
|PSDJAVA-237|قناع المقص غير ينطبق على المجلد|خلل|
|PSDJAVA-238|لا يمكن فتح الملف باستخدام Aspose.PSD للجافا|خلل|
|PSDJAVA-239|استثناء فشل حفظ الصورة عند تحويل PSD إلى PDF|خلل|
|PSDJAVA-240|عملية القص تُجعل مسار المقص غير صالح في صورة PSD|خلل|
|PSDJAVA-241|استثناء NullReference عند محاولة حفظ ملف PSD مع تأثير الظل معين|خلل|
|PSDJAVA-243|Aspose.PSD يقوم بإرجاع قيمة صحيحة في Image.CanLoad(pdfStream)|خلل|
|PSDJAVA-244|فشل الطبقات في التقديم في PNG المُنشَّأ|خلل|
|PSDJAVA-245|استثناء عند الوصول إلى بيانات النص|خلل|
|PSDJAVA-246|استثناء ImageSaveException عند حفظ ملف PSD|خلل|

# **تغييرات واجهة برمجة التطبيقات العامة**
# **الواجهات البرمجية المضافة:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T:com.aspose.psd.fileformats.psd.resources.WorkingPathResource
## **الواجهات البرمجية التي تمت إزالتها:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])

# **أمثلة الاستخدام:**

**PSDJAVA-231. دعم إضافة تأثير الحدود أثناء التشغيل**
{{< highlight java >}}
// توضح هذه الأمثلة كيفية إضافة تأثير حدود إلى الطبقات الحالية في ملف PSD في لغة الجافا.
// هنالك ثلاثة أنواع من التأثير: لون وتدرج ونمط. كل نوع له ثلاث طرق (مواقع) تُرسم فيها الحدود: داخل، وسط، وخارج.
// توضح هذه الأمثلة استخدام جميع هذه الحالات.

String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;

    // 1. يضيف تعبئة لونية، في الموضع الداخلي
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 2. يضيف تعبئة لونية، في الموضع الخارجي
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 3. يضيف تعبئة لونية، في الموضع الوسط
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // تدعيم بحد أعلى بوزن 700 للنص
    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

...

**PSDJAVA-246. استثناء ImageSaveException عند حفظ الملف PSD**
{{< highlight java >}}
// تحقق هذا المثال من عدم حدوث استثناء عند حفظ ملف PSD معين.

String srcPsdPath = "snowflake-ui-kit.psd";
String dstPsdPath = "snowflake-ui-kit-output.psd";

PsdImage image = (PsdImage)Image.load(srcPsdPath);
try
{
    image.save(dstPsdPath, new PsdOptions(image));
}
finally
{
    image.dispose();
}
{{< /highlight >}}