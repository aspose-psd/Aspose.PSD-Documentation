---
title: لایه تنظیم منحنی‌ها
type: docs
weight: 30
url: /fa/java/layer-types/adjustment-layer/curves/
---

# کار با لایه تنظیم منحنی ها در فتوشاپ با جاوا

هدف این مقاله نشان دادن قابلیت های کتابخانه Aspose.PSD برای جاوا در **کار با لایه های تنظیم منحنی ها** در اسناد Adobe® Photoshop® است. این کتابخانه کاملاً مستقل است. بنابراین، بدون نیاز به نصب ویرایشگر عکس فتوشاپ کار می کند. [لیست کامل ویژگی ها](https://docs.aspose.com/psd/java/features/) را می توانید در پایگاه داده ما پیدا کنید. حالا بیایید به منحنی ها برگردیم.

## مرور API

ابزار منحنی‌ها می تواند به عنوان یک خط مورب (منحنی) در یک نمودار با نقاط روشن در گوشه بالا و سایه در گوشه پایین راست نشان داده شود.

این کتابخانه API ارائه می دهد برای کار با منحنی، به عبارتی کلاس [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). با این حال، این کلاس دو **راهکار کاملاً متفاوت** برای کار با منحنی دارد. بنابراین، می توان در هر زمان در یکی از دو حالت زیر آن را ویرایش کرد:

- پیوسته (منحنی به عنوان یک مسیر با نقاط در مکان های خم شده نشان داده می شود)
- گسسته (منحنی به عنوان یک خط خط دوتایی نشان داده می شود)

بنابراین، کتابخانه دو روش برای اصلاح منحنی با استفاده از [مدیریت پیوسته](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) و [مدیریت گسسته](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) به ترتیب دارد. در ادامه نحوه استفاده از هرکدام را در یک مثال خاص توضیح خواهیم داد.

## تنظیم رنگ و تون به کمک مدیریت پیوسته منحنی

[مدیریت پیوسته منحنی](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **نقاط خم منحنی پیوسته** برای کانال ترکیبی (RGB) و همچنین برای هر یک از کانال های رنگی خاص ارائه می دهد. به منظور نمایش، مقداری تنظیمات منحنی (a) برای تصویر تیره شده ارکستر (b) به صورت آزمایشی اعمال می شود تا تصویر روشن شده با رنگ های گرمتر (c) به دست آید.

![شکل ۱ لایه تنظیم منحنی‌ها فتوشاپ](curves-psd-adjustment-layer-figure-1.png)

زیرا دو مدیر وجود دارد، قبل از گرفتن آن، لازم است یکی را به صورت صریح انتخاب کنیم (مدیر پیوسته در این مورد) و سپس می توانیم برای کانال های رنگ مورد نظر (RGB ترکیبی، قرمز و آبی به ترتیب) نقاط منحنی را به مختصات خاص اضافه کنیم تا شکل منحنی را ایجاد کنیم:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

مبدأ مختصات در گوشه پایین چپ است. حداکثر مقدار مختصات یک نقطه محدود به نوع داده (بایت) است و برابر با ۲۵۵ (۱۲۷ برای نوع امضا شده) است.

همچنین چندین [متد دیگر](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) وجود دارد که می توانید استفاده کنید.

## تنظیم تون با استفاده از مدیریت گسسته منحنی

همچنین مدیریت گسسته منحنی امکان قرار دادن نقاط منحنی (تغییر رنگ و تون در واقع) را فراهم می کند، اما تفاوت این است که آنها این کار را به شیوه ای دیگر انجام می دهند. ابتدا، **منحنی از نقاط** یا نقطه ها (نه یک خط محکم) تشکیل شده است. دوم، این مدیر **نقطه ای را که خود به خود جایی در نمودار نمی گذارد**. به جای آن، **نقطه را به بالا یا پایین حرکت می دهد** با محدوده مقادیر بین ۲۵۵ و ۰ به ترتیب. به طور پیش فرض، مقادیر نقاط منحنی به صورت افزایشی تا شکل یک منحنی که در زاویه ۴۵ درجه است به شکلی که به یاد داریم ایجاد می شود.

بنابراین، با توجه به این موضوع، به راحتی می توان تنظیمات &#8220;منفی (RBG)&#8221; preset فتوشاپ (a) را احیا کرد و آن را بر روی یک تصویر خاکستری دره (b) اعمال کرد تا در نهایت نمایش منفی دره (c) به دست آید.

![شکل ۲ لایه تنظیم منحنی‌ها فتوشاپ](curves-psd-adjustment-layer-figure-2.png) ابتدا، فراموش نکنید که مدیر مربوطه را انتخاب کنید تا بتوانید از آن استفاده کنید و سپس مقادیر نقطه منحنی را به ترتیب کاهشی از ۲۵۵ به ۰ برای هر نقطه منحنی تنظیم کنید (۲۵۵ در کل):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

مدیر همچنین چندین [متد دیگر](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) برای مدیریت منحنی ارائه می دهد.

## نتیجه

در این مقاله یاد گرفتیم که چگونه با استفاده از Aspose.PSD برای جاوا با دو روش کاملاً متفاوت (مدیران پیوسته و گسسته) در اسناد فتوشاپ کار کنیم.
