```markdown
---
title: ملاحظات الإصدار لـ Aspose.PSD for .NET 20.6
type: docs
weight: 70
url: /ar/net/aspose-psd-for-net-20-6-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

## تحسينات الإصدار

- **PSDNET-219**: نقل إعداد DefaultReplacementFont إلى فئة ImageOptionsBase.

## الأخطاء المعروفة

### الصلاحيات

- **PSDNET-606**: دعم LnkE للمورد.
- **PSDNET-386**: دعم britResource (مورد تعديل السطوع/التباين).

### العلل

- **PSDNET-596**: مجموعة طبقات بوضع الدمج غير المباشر لا تُعرض.
- **PSDNET-610**: استثناء الإشارة إلى NullReference عند محاولة تحويل ملف Psd معين إلى صورة.
- **PSDNET-636**: تغيير حجم ملفات PSD يعمل بشكل غير صحيح إذا كان هناك قناع في طبقة التعديل يحتوي على حدود فارغة.
- **PSDNET-611**: استثناء OverflowException عند محاولة فتح ملف Psd معين.
- **PSDNET-565**: صورة Psd بوضع RGB بـ 16 بت/قناة تُحدث الطبقات فقط على المعاينة.
- **PSDNET-652**: استثناء عند تحميل ملف PSD معين بمورد LnkE المُركّب وخصائص adobeStockLicenseState.
- **PSDNET-640**: تجاهل تغييرات قناع الطبقة PSD عند الحفظ.
- **PSDNET-593**: حفظ ملف AI إلى تنسيق Jpeg2000 لا يعمل.
- **PSDNET-638**: ترتيب الطبقات غير صحيح بعد إضافة مجموعة طبقات إلى مجموعة طبقات فارغة.

## التغييرات في واجهة برمجة التطبيقات

### الواجهات الجديدة

- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.MaskRectangle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.IsEmpty

### الواجهات المحذوفة

- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## الأمثلة

### كيفية الدعم لـ LnkE للمورد

```java
 string message = "مثال على دعم LnkE Resource يعمل بشكل غير صحيح.";

void AssertIsTrue(bool condition)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

void AssertAreEqual(object actual, object expected)

{

    if (!object.Equals(actual, expected))

    {

        throw new FormatException(message);

    }

}

// يُظهر هذا المثال كيفية الحصول وتعيين الخصائص لموارد Photoshop Psd LnkE التي تحتوي على معلومات عن ملف مرتبط خارجيًا.

void ExampleOfLnkEResourceSupport(

    string filePath,

    int length,

    int length2,

    int length3,

    int length4,

    string fullPath,

    string date,

    double assetModTime,

    string childDocId,

    bool locked,

    string uid,

    string name,

    string originalFileName,

    string fileType,

    long size)

{

    string fileName = Path.GetFileName(filePath);

    string outputPath = @"Output\" + fileName;

    using
```
