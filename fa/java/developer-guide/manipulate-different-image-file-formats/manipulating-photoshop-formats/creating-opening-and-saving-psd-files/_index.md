---
title: ایجاد، باز کردن و ذخیره‌سازی پرونده‌های PSD
type: docs
weight: 10
url: /fa/creating-opening-and-saving-psd-files/
---

## **صدور تصویر به فرمت PSD**
PSD، مستند فتوشاپ، فرمت پیش‌فرضی است که توسط Adobe Photoshop برای کار با تصاویر استفاده می‌شود. Aspose.PSD به شما اجازه می‌دهد تا پرونده‌ها را به فرمت PSD بارگذاری، ویرایش و ذخیره کنید تا بتوانند در فتوشاپ باز شده و ویرایش شوند. این مقاله نشان می‌دهد چگونه با استفاده از Aspose.PSD پرونده‌ای را به فرمت PSD ذخیره کنید، و همچنین برخی از تنظیماتی که می‌تواند در هنگام ذخیره کردن به این فرمت استفاده شود مورد بحث قرار می‌دهد. PsdOptions کلاس ویژه‌ای در فضای‌نام ImageOptions است که برای صدور تصاویر به PSD استفاده می‌شود. برای صدور به PSD، یک نمونه از کلاس Image ایجاد کنید، یا از یک تصویر موجود (Thumbnail ها به عنوان مثال) بارگذاری شود یا از ابتدا ایجاد شود. این مقاله توضیح می‌دهد چگونه. در مثال‌های زیر، یک تصویر از ابتدا ایجاد می‌شود. هنگامی که ایجاد شده و داده‌های پیکسل پر شده است، تصویر را با استفاده از متد Save کلاس Image ذخیره کنید و یک شیء PsdOptions را به عنوان آرگومان دوم ارائه دهید. تعدادی از خاصیت‌های کلاس PsdOptions می‌تواند برای تبدیل پیشرفته تنظیم شود. برخی از خاصیت‌ها عبارت‌اند از ColorMode، CompressionMethod و Version. Aspose.PSD از طریق شرح فشرده‌سازی زیر از طریق به ازای فشرده‌سازی رو‌باز حمایت می‌کند:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

حالت‌های رنگ زیر از طریق نابرش‌های ColorModes پشتیبانی می‌شود:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



منابع اضافی می‌توانند اضافه شوند، مانند منابع بند انگشتی برای PSD v4.0، v5.0 و بالاتر، یا منابع تور و راهبرد برای PSD v4.0 و بالاتر. کد زیر یک فایل BMP را از ابتدا ایجاد می‌کند، پیکسل‌ها را پر می‌کند و آن را با حالت فشرده‌سازی RLE و حالت رنگی خاکستری به PSD ذخیره می‌کند. کد زیر نشان می‌دهد چگونه تا تصویر را به PSD صدور کنید.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **وارد کردن تصویر به لایه PSD**
این مقاله نحوه استفاده از Aspose.PSD برای افزودن یا وارد کردن یک تصویر به یک لایه PSD را نشان می‌دهد. API های Aspose.PSD متداول و آسانی را برای دستیابی به این هدف ارائه داده‌اند. Aspose.PSD متد DrawImage کلاس Layer را برای اضافه کردن/وارد کردن تصویر به یک پرونده PSD ارائه داده است. متد DrawImage نیازمند مکان و مقادیر تصویر برای اضافه کردن/وارد کردن تصویر به یک پرونده PSD است. مراحل وارد کردن تصویر به لایه PSD به شدت ساده است:

- یک پرونده PSD را به عنوان تصویر با استفاده از متد فکتوری Load کلاس Image بارگذاری کنید.
- یک نمونه از کلاس لایه ایجاد کرده و لایه تصویر PSD را به آن اختصاص دهید.
- تصویری که باید اضافه یا ایجاد شود را بارگذاری کنید.
- در حالی که مکان و نمونه تصویر خود را مشخص می‌کنید، متد Layet.DrawImage را فراخوانی کنید.
- نتایج را ذخیره کنید.


کد زیر نشان می‌دهد چگونه تصویر را به لایه PSD وارد کنید.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **ایجاد Miniature ها از پرونده‌های PSD**
PSD فرمت مستندی است که در برنامه فتوشاپ Adobe ایجاد شده است. فتوشاپ Adobe (نسخه 5.0 و بالاتر) اطلاعات Miniature را برای نمایش پیش‌نمایش در یک بلاک منبع تصویر در نظر می‌گیرد که از یک هدر 28 بایتی اولیه تشکیل شده و سپس یک Miniature JFIF به ترتیب RGB (قرمز، سبز، آبی) دنبال می‌شود. API Aspose.PSD یک مکانیزم آسان برای دسترسی به منابع پرونده PSD فراهم می‌کند. این منابع شامل منبع Miniature می‌شود که به نوبه خود می‌تواند برداشته و مطابق نیاز برنامه بر روی دیسک ذخیره شود. کد زیر نشان می‌دهد چگونه Miniature ها را از پرونده‌های PSD ایجاد کنید.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **ایجاد پرونده‌های PSD با نمای فهرست**
Aspose.PSD برای Java API می‌تواند پرونده‌های PSD با نمای فهرست از ابتدا ایجاد کند. این مقاله استفاده از کلاس‌های PsdOptions و PsdImage برای ایجاد یک PSD با نمای فهرست در حین رسم برخی از اشکال روی کانون ایجاد شده جدید را نشان می‌دهد. گام‌های ساده زیر برای ایجاد یک پرونده PSD با نمای فهرست مورد نیاز است:

- یک نمونه از PsdOptions ایجاد کرده و منبع آن را تنظیم کنید.
- خواص ColorMode کلاس PsdOptions را به ColorModes.Indexed تنظیم کنید.
- یک پالتی از رنگ‌ها از فضای RGB ایجاد کنید و آن را به عنوان خاصیت Palette کلاس PsdOptions تنظیم کنید.
- خاصیت CompressionMethod را به الگوریتم فشرده‌سازی مورد نیاز تنظیم کنید.
- با فراخوانی PsdImage.Create یک تصویر PSD جدید ایجاد کنید.
- گرافیک را رسم کنید یا عملیات دیگری را بر اساس نیاز انجام دهید.
- PsdImage.Save را فراخوانی کنید تا تمام تغییرات اعمال شود.



کد زیر نشان می‌دهد چگونه پرونده‌های PSD با نمای فهرست ایجاد کنید.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **صدور لایه PSD به تصویر رستر**
Aspose.PSD برای Java به شما امکان صدور لایه‌ها در یک پرونده PSD به تصاویر رستر را می‌دهد. لطفاً از متد Aspose.PSD.FileFormats.Psd.Layers.Layer.Save برای صدور لایه به تصویر استفاده کنید. کد نمونه زیر یک فایل PSD را بارگذاری کرده و هر یک از لایه‌های آن را به یک تصویر PNG با استفاده از Aspose.PSD.FileFormats.Psd.Layers.Layer.Save صدور می‌کند. هنگامی که تمام لایه‌ها به تصاویر PNG صادر می‌شوند، می‌توانید آن‌ها را با استفاده از نمایشگر تصویر مورد علاقه خود باز کنید. کد زیر نشان می‌دهد چگونه لایه PSD را به تصویر راستر صادر کنید.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}
