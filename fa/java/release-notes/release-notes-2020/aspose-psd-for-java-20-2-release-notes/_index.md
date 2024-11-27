---
title: دفترچه‌ها ی انتشار Aspose.PSD برای جاوا 20.2
type: مستندات
weight: 20
url: /fa/java/aspose-psd-for-java-20-2-release-notes/
---

{{% alert color="primary" %}} این صفحه حاوی یادداشت‌های انتشار برای [Aspose.PSD برای جاوا 20.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) می‌باشد. {{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDJAVA-96|بهبود قابلیت رنگ‌های متفاوت متن در لایه متن|ویژگی|
|PSDJAVA-97|پشتیبانی از منابع clbl (منبع لایه اطلاعاتی در مورد عناصر برشی‌گذاری ادغام نور)|ویژگی|
|PSDJAVA-100|پشتیبانی از منابع blwh (منبع حاوی داده لایه تنظیم سیاه و سفید)|ویژگی|
|PSDJAVA-101|قابلیت صدور گروه لایه به Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|ویژگی|
|PSDJAVA-105|پشتیبانی از منبع lspf (شامل تنظیمات درباره تنظیم محافظت از لایه)|ویژگی|
|PSDJAVA-106|پشتیبانی از منبع infx (شامل داده‌های درباره ادغام عناصر داخلی)|ویژگی|
|PSDJAVA-99|تجدید نظر در PsdImage و Layer برای تغییر رفتار تبدیل (بازنویسی صحیح/چرخاندن/برش برای ماسک لایه اگر ما یک لایه را به طور جداگانه تبدیل کنیم)|بهبود|
|PSDJAVA-98|در برخی از تنظیمات جهانی سیستم تصویر نقاشی AI باز نمی‌شود|خطا|
|PSDJAVA-102|پس از انجام عملیات FlipRotate بر روی لایه، تصویر PSD غیرقابل خواندن می‌شود|خطا|
|PSDJAVA-103|System.ArgumentException در هنگام بارگذاری فایل PSD|خطا|
|PSDJAVA-104|پس از استفاده از یک متد تبدیل برای یک لایه تنها، لایه ذخیره شده مرزهای نادرست یا یک ماسک دارد|خطا|
# **تغییرات API عمومی**
# **این API موقت غیرفعال شده و در انتشار بعدی فعال خواهد شد:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)

` `**لطفا در این مدت از وابستگی مناسب، نسخه v19.4 را استفاده کنید.**
# **APIهای اضافه شده:**
- M:com.aspose.psd.Color.op_Equality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.Color.op_Inequality(com.aspose.psd.Color,com.aspose.psd.Color)
- ...

**مثال‌های استفاده:**
**PSDJAVA-96. بهبود قابلیت رنگ‌های متفاوت متن در لایه متن**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-97. پشتیبانی از منابع clbl (منبع لایه اطلاعاتی در مورد عناصر برشی‌گذاری ادغام نور)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-100. پشتیبانی از منابع blwh (منبع حاوی داده لایه تنظیم سیاه و سفید)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-101. قابلیت صدور گروه لایه به Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-105. پشتیبانی از منبع lspf (شامل تنظیمات درباره تنظیم محافظت از لایه)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-106. پشتیبانی از منبع infx (شامل داده‌های درباره ادغام عناصر داخلی)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-98. در برخی از تنظیمات جهانی سیستم تصویر نقاشی AI باز نمی‌شود**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-102. پس از انجام عملیات FlipRotate بر روی لایه، تصویر PSD غیرقابل خواندن می‌شود**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-103. System.ArgumentException در هنگام بارگذاری فایل PSD**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-104. پس از استفاده از یک متد تبدیل برای یک لایه تنها، لایه ذخیره شده مرزهای نادرست یا یک ماسک دارد**

{{< highlight java >}}
...
{{< /highlight >}}
**PSDJAVA-99. Refactoring of PsdImage and Layer to change Transformation behavior (Correct resize/rotate/crop for layer masks if we transform one layer separately)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-98. In some globalization settings AI Image raster image can not be opened**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-102. After performing the FlipRotate operation on Layer, PSD Image becomes unreadable**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-103. System.ArgumentException during the loading of PSD file**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-104. After using a transformation method for a layer only, the saved layer has incorrect bounds or a mask**

{{< highlight java >}}
...
{{< /highlight >}}

**اینجا پایان انتقال ترجمه فایل است.**