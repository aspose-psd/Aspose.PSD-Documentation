---
title: Manipulating Adobe Photoshop Formats
type: docs
weight: 20
url: /fa/net/manipulating-adobe-photoshop-formats/
---

## **ادغام لایه‌های PSD در لایه‌های دیگر**

## **صادر کردن تصویر به صورت PSD**
PSD، مستند PhotoShop، قالب پیش‌فرض فایلی است که توسط Adobe Photoshop برای کار با تصاویر استفاده می‌شود. Aspose.PSD به شما امکان می‌دهد فایل‌ها را به صورت PSD بارگذاری، ویرایش و ذخیره کنید تا بتوانند در Photoshop باز شده و ویرایش شوند. این مقاله نحوه ذخیره فایل به عنوان PSD با Aspose.PSD را نشان می‌دهد، و همچنین برخی از تنظیماتی که می‌توانند در زمان ذخیره به این فرمت استفاده شوند را بررسی می‌کند. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) یک کلاس تخصصی در فضای‌نام [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) است که برای صادر کردن تصاویر به PSD استفاده می‌شود. برای صادر کردن به صورت PSD، یک نمونه از کلاس Image ایجاد کنید، آن‌را از یک فایل تصویر موجود (به عنوان نمونه‌های کوچک‌نمایی) بارگذاری کنید یا از ابتدا ایجاد کنید. این مقاله نحوه این عملی را توضیح می‌دهد. در مثال‌های زیر، یک تصویر از ابتدا ایجاد می‌شود. بعد از ایجاد و پر کردن داده پیکسل، تصویر را با استفاده از متد Save کلاس Image ذخیره کنید و یک شیء PsdOptions را به عنوان آرگومان دوم ارائه دهید. چندین ویژگی کلاس PsdOptions برای تبدیل پیشرفته تنظیم می‌شود. برخی از ویژگی‌ها شامل ColorMode، [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) و Version می‌باشند. Aspose.PSD از روش‌های فشرده‌سازی زیر از طریق شمارش CompressionMethod پشتیبانی می‌کند:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

حالت‌های رنگ زیر از طریق شمارش [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes) پشتیبانی می‌شوند:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

منابع اضافی، مانند منابع بندانگشتی برای PSD v4.0 و v5.0 و بالاتر یا منابع شبکه و راهنما برای PSD v4.0 و بالاتر اضافه شده‌اند. کد زیر یک پرونده تصویر از ابتدا ایجاد می‌کند، پیکسل‌ها را پر می‌کند و آن را با فشرده‌سازی RLE و حالت رنگی خاکستری به PSD ذخیره می‌کند. کد موارد زیر به شما نشان می‌دهد چگونه یک تصویر را به صورت PSD صادر کنید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}

## **وارد کردن تصویر به لایه PSD**
این مقاله نشان می‌دهد چگونه از Aspose.PSD برای اضافه یا وارد کردن یک تصویر به یک لایه PSD استفاده کنیم. APIهای Aspose.PSD روش‌های کارآمد و آسان برای دستیابی به این هدف را ارائه کرده‌اند. Aspose.PSD متد DrawImage از کلاس Layer را برای اضافه یا وارد کردن یک تصویر به یک فایل PSD ارائه کرده است. متد DrawImage نیاز به موقعیت و مقادیر تصویر برای اضافه یا وارد کردن یک تصویر به یک فایل PSD دارد. مراحل وارد کردن تصویر به لایه PSD به شرح زیر است:

- یک فایل PSD را به عنوان تصویر با استفاده از متد Factory Load ارائه شده توسط کلاس Image بارگذاری کنید.
- یک نمونه از کلاس Layer از جریان با فایل Png، Jpeg، Tiff، Gif، Bmp، Psd یا j2k ایجاد کنید
- لایه را به Psd با استفاده از متد AddLayer اضافه کنید
- نتایج را ذخیره کنید.

کد زیر نشان می‌دهد چگونه تصویر را به لایه PSD وارد کنید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

## **جایگزینی رنگ در لایه‌های PSD**
این مقاله نشان می‌دهد چگونه از Aspose.PSD برای اضافه یا وارد کردن یک تصویر به یک لایه PSD استفاده کنیم. APIهای Aspose.PSD روش‌های کارآمد و آسان برای دستیابی به این هدف را ارائه کرده‌اند. Aspose.PSD متد DrawImage کلاس Layer را برای اضافه یا وارد کردن یک تصویر به یک فایل PSD ارائه کرده است. متد DrawImage نیاز به موقعیت و مقادیر تصویر برای اضافه یا وارد کردن یک تصویر به یک فایل PSD دارد. مراحل وارد کردن تصویر به لایه PSD به شرح زیر است:

- یک فایل PSD را به عنوان تصویر با استفاده از متد Factory Load ارائه شده توسط کلاس Image بارگذاری کنید.
- یک نمونه از کلاس Layer ایجاد کرده و لایه تصویر PSD را به آن اختصاص دهید.
- تصویری که نیاز به اضافه شدن به آن دارد را بارگذاری کنید یا یکی از ابتدا ایجاد کنید.
- متد Layer.DrawImage را فراخوانی کنید و مکان و نمونه تصویر را مشخص کنید.
- نتایج را ذخیره کنید.

کد زیر نشان می‌دهد چگونه تصویر را به لایه PSD وارد کنید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}

## **ایجاد تصاویر انگشتی از فایل‌های PSD**
PSD فرمت سندی بومی از اپلیکیشن فتوشاپ Adobe است. Adobe Photoshop (نسخه 5.0 و بالاتر) اطلاعات تصویر بندانگشتی برای نمایش پیش‌نمایش را در یک بلوک منبع تصویر ذخیره می‌کند که شامل یک هدر 28 بایتی ابتدایی و یک تصویر تصویری JFIF به رنگ‌های RGB (قرمز، سبز، آبی) است. API Aspose.PSD یک مکانیزم ساده برای دسترسی به منابع فایل PSD ارائه می‌دهد. این منابع همچنین شامل منبع بندانگشتی است که به موازات می‌توانند برداشته و به هارد دیسک ذخیره شوند طبق نیاز برنامه. کد زیر نشان می‌دهد چگونه تصاویر انگشتی را از فایل‌های PSD ایجاد کنید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}

## **ایجاد فایل‌های PSD شاخص**
API Aspose.PSD برای .NET می‌تواند فایل‌های PSD شاخص از ابتدا ایجاد کند. این مقاله استفاده از کلاس‌های PsdOptions و [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) را برای ایجاد یک PSD شاخص در زمان رسم بر روی کانوس تازه‌ای ارائه می‌دهد. اقدامات ساده زیر برای ایجاد یک فایل PSD شاخص لازم است:

- یک نمونه از PsdOptions ایجاد کرده و منبع آن را تنظیم کنید.
- ویژگی ColorMode را PsdOptions به ColorModes.Indexed تنظیم کنید.
- یک بافت جدید از رنگ‌ها از فضای RGB ایجاد کرده و آن را به عنوان ویژگی Palette PsdOptions تنظیم کنید.
- ویژگی CompressionMethod را به الگوریتم فشرده مورد نیاز تنظیم کنید.
- با فراخوانی متد PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) یک تصویر PSD جدید ایجاد کنید.
- گرافیک را رسم کنید یا دیگر عملیات‌ها را انجام دهید.
- متد PsdImage.Save را فراخوانی کنید تا همه تغییرات اعمال شود.


کد زیر نشان می‌دهد چگونه فایل‌های PSD شاخص ایجاد کنید.


{{< gist "aspose-com-gists" "8a4d34ce56d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}

## **صادر کردن لایه PSD به تصویر رستر**
Aspose.PSD برای .NET به شما امکان صادر کردن لایه‌ها در یک فایل PSD به تصاویر رستر را می‌دهد. لطفا از [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) برای صادر کردن لایه به تصویر استفاده کنید. کد نمونه زیر یک فایل PSD را بارگذاری می‌کند و هر یک از لایه‌های آن را به یک تصویر PNG با استفاده از Aspose.PSD.FileFormats.Psd.Layers.Layer.Save صادر می‌کند. پس از صادر شدن همه لایه‌ها به تصاویر PNG، می‌توانید آن‌ها را با استفاده از مشاهده‌کننده تصویر مورد علاقه خود باز کنید. کد زیر نشان می‌دهد چگونه یک لایه PSD را به تصویر رستر صادر کنید.


{{< gist "aspose-com-gists" "8a9d34ce5642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}

## **به روزرسانی لایه متنی در فایل PSD**
Aspose.PSD برای .NET به شما امکان مدیریت متن در لایه متنی یک فایل PSD را می‌دهد. لطفا از کلاس [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) برای به‌روزرسانی متن در لایه PSD استفاده کنید. کد نمونه زیر یک فایل PSD را بارگذاری می‌کند، به لایه متن دسترسی پیدا می‌کند، متن را به‌روزرسانی می‌کند و فایل PSD را با نام جدیدی با استفاده از [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](