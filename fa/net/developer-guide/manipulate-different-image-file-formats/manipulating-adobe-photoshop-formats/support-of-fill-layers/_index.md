---
title: پشتیبانی از لایه‌های پر شده
type: docs
weight: 90
url: /fa/net/support-of-fill-layers/
---

## **لایه‌های پرشده با الگو**
این مقاله نحوه پر کردن لایه [PSD](https://wiki.fileformat.com/image/psd/) با پردازنده الگو را نشان می دهد. یک الگو* * تصویر، رنگ، سایه یا خط است که برای پر کردن یک ناحیه از یک تصویر استفاده می شود. لطفا از Aspose.PSD.FileFormats.Psd.Layers.FillLayer برای اضافه کردن یک الگو به لایه PSD استفاده کنید. کد‌های زیر یک پرونده PSD را بارگیری می‌کنند، به کلاس [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) دسترسی می‌یابند و الگو را با استفاده از خصوصیات [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) تنظیم می‌کنند.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}

در زیر مثالی دیگر آمده که نشان می دهد چگونه [Aspose.PSD](https://products.aspose.com/psd/net) الگو را با استفاده از [FillLayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) و [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings) اجرا می کند.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}

## **لایه‌های پر شده با پر کردن گرادیانت**
این مقاله نحوه استفاده از پر کردن گرادیانت برای پر کردن لایه PSD را نشان می‌دهد. API‌های Aspose.PSD متدهای کارآمد و آسان برای رسیدن به این هدف ارائه کرده‌اند. Aspose.PSD کلاس های [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) و [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) را برای اضافه کردن اثر گرادیانت به یک لایه ارائه داده است.

مراحل پر کردن لایه PSD با پر کردن گرادیانت به شرح زیر است:

-  با استفاده از متد کارخانه [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) ارائه شده توسط کلاس [Image](https://reference.aspose.com/net/psd/aspose.psd/image) یک پرونده PSD را به عنوان تصویر بارگیری کنید.
- خصوصیات تنظیمات شی [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) را تنظیم کنید.
- یک لیست از [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) با رنگ‌های مورد نیاز و موقعیت رنگ ایجاد کنید.
- یک لیست از نقاط شفافیت با شفافیت و موقعیت نقطه شفافیت مورد نیاز ایجاد کنید.
- متد [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) را فراخوانی کنید
- نتایج را ذخیره کنید.

کد زیر نشان می دهد چگونه گرادیانت گرادیانت به لایه PSD اضافه کنید.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

**مثال دیگری که از خصوصیت [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** برای پر کردن لایه PSD با پر کردن گرادیانت استفاده میکند، بیان می شود. Aspose.PSD از طریق شماره گرادیانت‌ها زیر را از طریق شماره گرادیانت ها پشتیبانی می کند:

- **GradientType.Linear:** در یک گرادیانت خطی، رنگ‌ها از دمای شروع به انتها در یک خط ریخته شده است.
- **GradientType.Radial:** در گرادیانت شعاعی، رنگ‌ها از نقطه شروع در یک الگوی دایره‌ای بیرون می آیند.
- **GradientType.Angle:** در یک گرادیانت زاویه، گرادیان از نقطه شروع در جهت‌های مخالف مخالف مخالف مخالف می گردد.
- **GradientType.Reflected:** در گرادیانت بازتابی، رنگ بر روی هر دو طرف نقطه شروع بازتاب می شود.
- **GradientType.Diamond:** گرادیانت الماس شکل مانند الماس از نقطه شروع ایجاد می کند.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

## **پشتیبانی از خاصیت مقیاس برای لایه پرکردن گرادیانت**
این مقاله نحوه اندازه‌گیری لایه FillLayer با پر کردن گرادیانت با استفاده از Aspose.PSD برای .NET را نشان می دهد. به این منظور، یک خصیه جدید به نام [**مقیاس**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) به [**تنظیمات FillLayer**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings) اضافه شد.

در زیر، نمایش کد نشان می دهد چگونه از خصیه **مقیاس** استفاده کنیم.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}

## **لایه‌های پر شده با رنگ پرکردن**
این مقاله نحوه پر کردن لایه [PSD](https://wiki.fileformat.com/image/psd/) با رنگ را نشان می دهد. لطفا از کلاس [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) برای اضافه کردن رنگ به لایه PSD استفاده کنید. کد زیر یک پرونده PSD را بارگیری می کند، به کلاس لایه پرشده دسترسی پیدا می کند و رنگ را با استفاده از [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings) تنظیم می‌کند.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}
