---
title: أسبوسيبس دي ستوديو لجافا 20.6 - ملاحظات الإصدار
type: docs
weight: 50
url: /ar/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} تحتوي هذه الصفحة على ملاحظات الإصدار لـ [أسبوسيبس دي ستوديو لجافا 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDJAVA-216|دعم LnkEResource (مورد طبقة الكائن الذكي)|ميزة|
|PSDJAVA-219|دعم britResource (مورد تعديل السطوع/التباين)|ميزة|
|PSDJAVA-222|نقل إعداد DefaultReplacementFont إلى فئة ImageOptionsBase|تحسين|
|PSDJAVA-217|تغيير حجم ملفات PSD يعمل بشكل غير صحيح في حالة وجود قناع في طبقة التعديل يحتوي على حدود فارغة|خطأ|
|PSDJAVA-218|تحديث طبقة Psd بوضع RGB 16 بت/قناة فقط على المعاينة|خطأ|
|PSDJAVA-220|تجاهل تغييرات قناع طبقة PSD عند الحفظ|خطأ|
|PSDJAVA-221|ترتيب الطبقات غير الصحيح بعد إضافة مجموعة طبقات إلى مجموعة طبقات فارغة|خطأ|
|PSDJAVA-223|استثناء عند تحميل ملف PSD مع مورد LnkE المركب وخصائص adobeStockLicenseState|خطأ|
|PSDJAVA-224|فشل حفظ ملف AI إلى تنسيق Jpeg2000|خطأ|
|PSDJAVA-225|لم يتم عرض مجموعة الطبقات بوضع الدمج غير المباشر|خطأ|
|PSDJAVA-226|استثناء NullReference عند محاولة تحويل ملف Psd معين إلى صورة|خطأ|
|PSDJAVA-227|استثناء Overflow عند محاولة فتح ملف PSD معين|خطأ|

## تغييرات واجهة برمجة التطبيقات العامة
## تمت إضافة الواجهات البرمجية التالية:
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- ...
  
## الواجهات البرمجية التالية تمت إزالتها:
- M: com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M: com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont

# أمثلة الاستخدام:

**PSDJAVA-216: دعم LnkEResource (مورد طبقة الكائن الذكي)**

{{< highlight java >}}
// مثال على ربط أنواع مختلفة من الأصول (صور نقطية، مكتبات CC) بملف PSD.

// أيضًا Api من LnkeResource يعتبر.

...

{{< /highlight >}}

...
