---
title: کار با لایه‌های متنی
type: docs
weight: 170
url: /fa/net/کار-با-لایه-های-متنی/
---

## **افزودن لایه متنی**
Aspose.PSD برای .NET به شما امکان افزودن لایه متنی در یک فایل PSD را می‌دهد. مراحل افزودن لایه متنی در یک فایل PSD به شرح زیر است:

- بارگذاری یک فایل PSD به عنوان تصویر با استفاده از متد فابریک [Load](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) ارائه شده توسط کلاس [Image](https://reference.aspose.com/psd/net/aspose.psd/image)
- فراخوانی متد [AddTextLayer](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) که متن را و یک نمونه از کلاس [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) را دریافت می‌کند
- ذخیره نتیجه

قطعه کد زیر نحوه افزودن لایه متنی در یک فایل PSD را نمایش می‌دهد

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **تنظیم موقعیت لایه متنی**
Aspose.PSD برای .NET به شما امکان تنظیم موقعیت یک لایه متنی در یک فایل PSD را می‌دهد. مراحل تنظیم موقعیت لایه متنی در یک فایل PSD به شرح زیر است:

- بارگذاری یک فایل PSD به عنوان تصویر با استفاده از متد فابریک Load ارائه شده توسط کلاس Image
- فراخوانی متد AddTextLayer هنگامی که موقعیت چپ و بالای لایه متنی مشخص می‌شود
- ذخیره نتیجه

قطعه کد زیر نحوه تنظیم موقعیت لایه متنی در یک فایل PSD را نمایش می‌دهد

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}
## **دریافت ویژگی‌های متن از یک لایه متنی**
با استفاده از Aspose.PSD برای .NET، شما می‌توانید ویژگی‌های متنی اجزای مختلف موجود در لایه متنی PSD را دریافت و به‌روز رسانی کنید. این مقاله نحوه دریافت پاراگراف‌ها، استایل‌ها و ویژگی‌های متنی لایه متنی را نشان می‌دهد و آن‌ها را به‌روز می‌کند.

قطعه کد زیر نشان می‌دهد چگونه می‌توانید به این نیاز پاسخ دهید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


در اینجا مثال دیگری وجود دارد که نشان می‌دهد چگونه یک توسعه دهنده می‌تواند قالب‌بندی متن‌های مختلف از [TextLayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) با استفاده از [Aspose.PSD برای .NET](https://products.aspose.com/psd/net) را بدست آورد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}
## **به‌روزرسانی لایه متنی در فایل PSD**
Aspose.PSD برای .NET به شما امکان مدیریت متن در لایه متنی یک فایل PSD را می‌دهد. لطفا از کلاس Aspose.PSD.FileFormats.Psd.Layers.TextLayer برای به‌روزرسانی متن در لایه PSD استفاده کنید. قطعه کد زیر یک فایل PSD را بارگذاری می‌کند، به لایه متنی دسترسی پیدا می‌کند، متن را به‌روزرسانی می‌کند و فایل PSD را با یک نام جدید با استفاده از متد [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index) ذخیره می‌کند.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **پشتیبانی از لایه‌های متنی در زمان اجرا**
این مقاله نحوه افزودن لایه‌های متنی در زمان اجرا برای تصاویر PSD را نشان می‌دهد. قطعه کد زیر ارائه شده است.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
