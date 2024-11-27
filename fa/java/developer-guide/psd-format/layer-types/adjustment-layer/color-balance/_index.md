---
title: لایه تنظیم تعادل رنگ
type: docs
weight: 30
url: /fa/java/layer-types/adjustment-layer/color-balance/
---

# کار با لایه تنظیم تعادل رنگ فتوشاپ در جاوا

در این مقاله ما قصد داریم **تعادل رنگ تصویر** را در قالب فایل PSD در جاوا تنظیم کنیم. ما از یک کتابخانه ویژه به نام Aspose.PSD برای جاوا استفاده خواهیم کرد که یک جعبه ابزار برای مدیریت اسناد فتوشاپ است.

از آنجایی که این کتابخانه با فرمت فایل PSD کار می‌کند، تقریبا همه [ویژگی‌ها](https://docs.aspose.com/psd/java/features/) موجود در ویرایشگر فتوشاپ، از جمله **لایه تنظیم تعادل رنگ**، که کاملاً مناسب برای این کار است، هیچ استثناءی نیست.

لایه تنظیم تعادل رنگ امکان تغییر تعادل بین رنگ‌های اصلی (RGB) و از کم شونده (CMY) برای سایه‌ها، میان‌تون‌ها و نقاط روشن تصویر را به صورت ساده و سریع فراهم می‌کند.

## تنظیم تعادل رنگ

همانطور که گفته شد، لایه تنظیم تعادل رنگ در Aspose.PSD برای جاوا دقیقاً همان‌طور که است یعنی **تعادلی بین رنگ‌های اصلی و از کم شونده**. این به این معنی است که برای هر جفت رنگ (سیان/قرمز، مگنتا/سبز، زرد/آبی) سه مقیاس وجود دارد. شدت رنگ خاص در جفت‌های رنگی افزایش می‌یابد اگر مقدار به سمت آن حرکت کند و برعکس. علاوه بر این، این سه جفت ارثی برای هر منطقه از محدوده تونال (سایه‌ها، میان‌تون‌ها و نقاط روشن) که انعطاف‌پذیری این نوع تنظیم را افزایش می‌دهد.

پس، بیایید این دانش را به کار اندازیم. به عنوان مثال یک عکس قرمزی از صورت زن (ب) را انتخاب می‌کنیم. صورت به اندازه کافی قرمز است و می‌خواهیم آن را با **اضافه کردن لایه تنظیم تعادل رنگ** برای کاهش قرمزی و افزایش سیان به طور اصلی تغییر دهیم (الف) تا صورت بیشتر به صورتی طبیعی به نظر برسد (ج). دوباره، برای این تصویر زیادی کار برای انجام داریم اما در این مقاله همه‌ی آنچه را خواهیم کرد را بیان کرده‌ایم.

![مثال لایه تنظیم تعادل رنگ](color-balance-adjustment-layer-example-figure-1.png) API لایه تنظیم تعادل رنگ دارای طراحی صاف است. بنابراین، کلاس [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) که همه چیزی که نیاز دارید است. ابتدا، نور را حفظ کنید زیرا به طور پیش‌فرض غیرفعال است. سپس، کمی از سبز و بیشتر زرد برای سایه‌ها با استفاده از متدهای مربوطه (نام‌هایی که از نام ناحیه محدوده تونال خاص و نام‌های رنگی در جفت رنگی تشکیل شده‌اند) اضافه کنید، سپس بیشتر سیان و کمی از آبی برای میان‌تون‌ها، و در نهایت بیشتری از سیان به همراه کمی از مگنتا و آبی اضافه کنید:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

حالا، عکسی که می‌خواستیم را دریافت کردیم! آیا اینقدر ساده نیست؟

توجه کنید که _مقدار هر جفت رنگ باید در بازه‌ی -100 تا 100 باشد_ که ارزش‌های منفی برای رنگ‌های کم شونده و مثبت برای رنگ‌های اصلی است، دقیقاً مانند ویرایشگر فتوشاپ.

برای کسب اطلاعات فنی بیشتر در مورد [لایه تنظیم تعادل رنگ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) به مراجعه به مرجع API‌ما مراجعه کنید.

## نتیجه‌گیری

در این مقاله ما بررسی کردیم چگونه می‌توانیم به صورت برنامه‌ریزی شده تعادل رنگ تصویر را در جاوا با استفاده از کتابخانه Aspose.PSD برای جاوا تنظیم کنیم. این کتابخانه API کاملی برای کار با لایه‌های تنظیم تعادل رنگ در اسناد فتوشاپ دارد.
