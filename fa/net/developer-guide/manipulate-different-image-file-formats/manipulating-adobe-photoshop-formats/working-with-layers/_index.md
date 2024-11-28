---
title: کار با لایه‌ها
type: docs
weight: 150
url: /fa/net/کار-با-لایه‌ها/
---

## **ایجاد یک گروه لایه**
یک گروه لایه از یک یا چند لایه تشکیل شده است و به کمک آن می‌توانید لایه‌های مشابه یا مرتبط را سازماندهی کنید. با استفاده از Aspose.PSD برای .NET، می‌توانید یک گروه لایه ایجاد کنید. به این منظور، یک متد جدید به نام [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) به کلاس **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** اضافه شده است تا گروه لایه را اضافه کند.

مراحل ایجاد گروه‌های لایه به شرح زیر است:

- یک نمونه از یک تصویر با استفاده از کلاس PsdImage به همراه عرض، ارتفاع و گزینه‌های تصویر مشخص ایجاد کنید.
- یک [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/layers/layergroup) با نام گروه مشخص و شاخص بسازید.
- یک نمونه از کلاس Layer بسازید و تصویر PSD را به آن اختصاص دهید.
- لایه ایجاد شده را با استفاده از متد AddLayer ارائه شده توسط کلاس LayerGroup به گروه لایه اضافه کنید.
- نتیجه را ذخیره کنید.

کد زیر نشان می‌دهد چگونه یک گروه لایه ایجاد کنید.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **تغییر نام یک لایه**
می‌توانید از هر نامی که می‌خواهید استفاده کنید، اما عمل معمول این است که از توصیف عمومی شی یا عنصری که در آن لایه استفاده می‌شود استفاده کنید. این مقاله نشان می‌دهد چگونه می‌توانید از Aspose.PSD برای .NET استفاده کنید تا نام یک لایه را تغییر دهید. به این منظور، یک ویژگی جدید به نام [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/displayname) به کلاس لایه اضافه شده است تا نام لایه را به درستی نمایش دهد. مشاهده شده است که هنگامی که فتوشاپ نام یک لایه را با استفاده از ویژگی [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/name) ذخیره می‌کند، کاراکترهای کره‌ای به عنوان بایت 63'?' در ASCII ذخیره می‌شوند. بنابراین، اگر می‌خواهید نام لایه را به درستی نمایش دهید از ویژگی **DisplayName** استفاده کنید زیرا ویژگی **Name** از کاراکترهای کره‌ای پشتیبانی نمی‌کند.

کد زیر نشان می‌دهد چگونه می‌توانید نام یک لایه را تغییر دهید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **پشتیبانی از لایه‌های متصل**
پیوستن لایه‌ها مانند گروه‌بندی لایه‌هاست. اگر دو یا چند لایه را به هم وصل کنید، به شما این امکان را می‌دهد که تغییرات خاصی را در هر دو لایه متصل اعمال کنید. به عنوان مثال، اگر تبدیلاتی را روی یک لایه اعمال کنید، به همه لایه‌های دیگری که به آنها وصل شده‌اند، اعمال می‌شود. این مقاله نشان می‌دهد چگونه می‌توانید لایه‌های متصل را دریافت و از وصل کردن آنها استفاده کنید با استفاده از [Aspose.PSD](https://products.aspose.com/psd).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
