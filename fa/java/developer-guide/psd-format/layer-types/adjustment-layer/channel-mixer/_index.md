---
title: لایه تنظیم کننده Mixer شیوه
type: docs
weight: 30
url: /fa/layer-types/adjustment-layer/channel-mixer/
---

# کار با لایه تنظیم کننده Channel Mixer در فتوشاپ به زبان جاوا

امروز قصد داریم بررسی کنیم که چگونه می‌توانیم با استفاده از برنامه‌نویسی به صورت پروگراماتیک در جاوا، رنگ‌های کانال‌ها را ترکیب کنیم در اسناد فتوشاپ. از آن‌جایی که ویرایشگر فتوشاپ اسکریپت Java را پشتیبانی نمی‌کند، ما از کتابخانه خاص تلاش‌ها در قالب فرمت PSD به نام Aspose.PSD برای جاوا استفاده خواهیم کرد.

این کتابخانه شامل **رابط برنامه نویسی برای کار با کانال‌های رنگ** است. چندین روش برای ترکیب رنگ‌ها وجود دارد، اما، در این مقاله، ما بر روی لایه تنظیم کننده Channel Mixer تمرکز خواهیم کرد.

رابط لایه تنظیم کننده Channel Mixer **امکان بازی با کانال‌های رنگ** را فراهم می‌کند برای ساخت تصاویر نظیر پنبه‌ریز یا ایجاد اثرات رنگی خلاق و حتی تبدیل تصویر به سیاه و سفید. بعد از آن، ما به بررسی چگونگی اعمال لایه تنظیم کننده Channel Mixer بر روی یک سند فتوشاپ موجود با استفاده از Aspose.PSD برای جاوا می‌پردازیم اما ابتدا باید در مورد ویژگی‌های کلی رابط برنامه نویسی صحبت کنیم.

## مروری بر رابط برنامه نویسی

در ایجاد لایه تنظیم کننده Channel Mixer چیز خاصی وجود ندارد. می‌توان از [روش کارخانه پیشفرض](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) برای اضافه‌کردن آن استفاده کرد که یک نمونه از کلاس ChannelMixerLayer را برمی‌گرداند. این کلاس حاوی **ویژگی‌های کلی** مانند گزینه Monochrome و یک متد برای دریافت یک کانال خروجی است. کانال خروجی خاص می‌تواند یکی از دو نوع [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) یا [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel) باشد. نوع [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) بستگی به [حالت رنگ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) تصویر دارد.

## تبدیل تصویر به سیاه و سفید

حالا، ما بیایید یک مثال از اعمال لایه تنظیم کننده Channel Mixer بر روی یک سند فتوشاپ موجود را بررسی کنیم. از آنجایی که این نوع لایه تنظیم کننده پشتیبانی از پیش‌تنظیم‌ها را هنوز انجام نمی‌دهد، ما **پیش‌تنظیم سیاه و سفید مادون قرمز (RGB) فتوشاپ** (a) را بازسازی خواهیم کرد. پیش‌تنظیم بر روی تصویر یک درخت با گل‌های رسیده (b) اعمال خواهد شد. به عنوان نتیجه، ما می‌خواهیم اثر عکاسی مادون قرمز را به دست آوریم (c).

![مثال لایه تنظیم کننده Channel Mixer](channel-mixer-adjustment-psd-layer-figure-1.png) اول، برای بازسازی پیش‌تنظیم سیاه و سفید مادون قرمز (RGB) فتوشاپ، لازم است که پرچم مادون قرمز را فعال کنیم و مقادیر مناسب واقعی برای هر رنگ (قرمز، سبز و آبی) برای کانال خروجی خاکستری را تنظیم کنیم:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome(**true**);
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed((**short**)-70);
    grayOutputChannel.setGreen((**short**)200);
    grayOutputChannel.setBlue((**short**)-30);

تصویر باید در حالت رنگ RGB باشد تا کد کار کند (به دلیل تبدیل به کلاس RgbMixerChannel). حالت رنگ CMYK نیز پشتیبانی می‌شود اما تنها برای تصاویر با حالت رنگ مربوطه.

در نظر داشته باشید که مقدار هر رنگ و همچنین خاصیت ثابت باید در بازه -200 تا 200 باشد.

## نتیجه‌گیری

در این مقاله، ما بررسی کردیم که چگونه با استفاده از API لایه تنظیم کننده Channel Mixer برای جاوا، رنگ‌ها در کانال‌های رنگ را تنظیم کرده و تصویر را به سیاه و سفید تبدیل کنیم.
