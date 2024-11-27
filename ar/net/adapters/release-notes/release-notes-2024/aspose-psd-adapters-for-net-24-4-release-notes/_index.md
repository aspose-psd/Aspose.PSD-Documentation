---
title: محولات Aspose.PSD لـ .NET 24.4 - ملاحظات الإصدار
type: docs
weight: 100
url: /ar/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

يحتوي هذا الصفحة على ملاحظات الإصدار لـ [محولات Aspose.PSD لـ .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **المفتاح** | **الملخص**                                                          | **الفئة** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | نشر مبدئي لـ Aspose.PSD.Adapters.Imaging إلى Nuget                  | تحسين |


## **تغييرات واجهة برمجة التطبيقات العامة**
# **الـ APIs المضافة:**
- لا شيء

# **الـ APIs المحذوفة:**
- لا شيء

## **أمثلة الاستخدام:**

يرجى التحقق من [صفحة وثائق محولات Aspose.PSD.Adapters](/psd/ar/net/adapters)

**PSDNET-1985. أكثر مثال كامل على استخدام محولات Aspose.PSD**

{{< highlight csharp >}}
// أضف تمكين المحولات في تكوين بدء التشغيل الخاص بك
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// قم بتمكين مصدرين بالإضافة
Aspose.PSD.Adapters.Imaging.EnableExporters();

// للعمل مع المحولات ، تحتاج إلى تراخيص Aspose.PSD والمحول
// ها هي كيفية تطبيق ترخيص Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// هنا مثال على كيفية تطبيق ترخيص المحول لـ Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// بعد ذلك يمكنك تشغيل أي كود للمحولات أو مكتبة PSD أو Imaging

// بعد ذلك ، يمكن فتح كل هذه الملفات بواسطة Aspose.PSD دون أي كود إضافي فقط استخدم
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // بعد تنفيذ هذا الكود ، ستحصل على ملف PSD تم إنشاؤه من WEBP ويمكن تطبيق أي تصفيات Aspose.PSD وطبقات وتعديلات بما في ذلك تحول التشوه.
}

// يمكنك إنشاء تكملة إضافية لصور مصدرة إلى تنسيق PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // استخدم واجهة Aspose.Imaging لتحرير ملف WEBP بميزات معينة للصور
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // ثم استخدم فقط طريقة ToPsdImage() وعدل الملف مثل PSD بميزات تشبه Photoshop بما في ذلك الطبقات ومرشحات ذكية وكائنات ذكية.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("بعض النص", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // احفظ الملف النهائي بتنسيق PSD باستخدام Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// إذا لم تكن بحاجة إلى استخدام المحملات أو المصدرين المقدمة بواسطة المحولات ، فقم بتعطيلها
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}