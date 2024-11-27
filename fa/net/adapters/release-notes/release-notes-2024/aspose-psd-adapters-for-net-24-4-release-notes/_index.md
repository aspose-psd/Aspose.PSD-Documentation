---
title: یادداشت‌های نسخه 24.4 Aspose.PSD Adapters برای .NET
type: docs
weight: 100
url: /fa/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD Adapters برای .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **کلید**    | **خلاصه**                                                          | **دسته‌بندی** |
|:------------|:-------------------------------------------------------------------|:--------------|
| PSDNET-1985 | انتشار اولیه Aspose.PSD.Adapters.Imaging به Nuget               | بهبود       |


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- هیچ‌کدام

# **API‌های حذف شده:**
- هیچ‌کدام

## **نمونه‌های استفاده:**

لطفا صفحه مستندات [Aspose.PSD.Adapters ](psd/fa/net/adapters) را بررسی کنید.

**PSDNET-1985. کامل‌ترین نمونه استفاده از Aspose.PSD.Adapters**

{{< highlight csharp >}}
// اضافه کردن فعال‌سازی آداپتورها در پیکان تنظیم
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// فعال‌سازی‌ کننده‌های اضافی را نیز فعال کنید
Aspose.PSD.Adapters.Imaging.EnableExporters();

// برای کار کردن با آداپتورها ، شما نیازمند لایسنس های هر دو Aspose.PSD و adaptee هستید
// اینجا نحوه اعمال لایسنس Aspose.PSD را مشاهده کنید
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// اینجا نمونه‌ای از نحوه اعمال Adaptee License برای Aspose.Imaging است
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// سپس می‌توانید هر کدی از آداپتورها یا کتابخانه PSD یا Imaging اجرا کنید

// بعد از این ، تمامی این فایل‌ها می‌توانند توسط Aspose.PSD بدون هیچ کد اضافی دیگری باز شوند ، فقط از آن استفاده کنید
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // پس از اجرای این کد ، فایل PSD ایجاد شده از WEBP را دریافت می کنید و می توانید هر گونه فیلتر Aspose.PSD ، لایه ها و تنظیمات شامل تبدیل وارپ را اعمال کنید
}

// شما می‌توانید علاوه برای ایجاد Adaptees عکس‌هایی را به فرمت PSD انتقال دهید
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // از رابط کاربری Aspose.Imaging برای ویرایش فایل WEBP با ویژگی‌های خاص تصویربرداری استفاده کنید
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // سپس فقط از متد ToPsdImage() استفاده کنید و فایل را مانند PSD با ویژگی‌های شبیه فتوشاپ از جمله لایه ها ، فیلترهای هوشمند و اشیاء هوشمند ویرایش کنید
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // ذخیره نهایی فایل PSD با استفاده از Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// اگر نیازی به استفاده از بارگذارها یا صادر کننده‌های ارائه شده توسط آداپتورها نیست ، این‌ها را غیرفعال کنید
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		

{{< /highlight >}}
