---
title: تبدیل PSD بین انواع گونه های مختلف رنگ
type: مستندات
weight: 50
url: /fa/net/psd-convert-between-different-color-modes/
---

با این مقاله می‌توانید انواع حالت‌های رنگی پشتیبانی شده توسط Aspose.PSD را یاد بگیرید.

Aspose.PSD، به عنوان یک مثال، تبدیل از 8 به 16 بیت برای هر پیکسل و برعکس را پشتیبانی می‌کند. تبدیل‌های CMYK ICC-Profile و دیگر تبدیل‌های از یک نوع عمق بیت به نوع دیگر. در اینجا می‌توانید نمونه‌ها از چگونگی تبدیل به حالت خاکستری در فایل PSD را ببینید.

## **تبدیل از CMYK، RGB، خاکستری به حالت رنگی خاکستری**
کد نمونه زیر نشان می‌دهد چطور می‌توان درون نرم‌افزار بدون استفاده از فتوشاپ، از CMYK، RGB یا خاکستری به رنگی خاکستری تبدیل کرد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}


## **تصویر فتوشاپ 16 بیت به حالت خاکستری 8 بیت تبدیل شود**
اما اگر نیاز به تبدیل تصویر 16 بیت خاکستری فتوشاپ به حالت خاکستری 8 بیتی داشته باشید، باید از کد زیر استفاده کنید. 8 بیت، یک عمق معمولی در فایل‌های PSD است.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}


## **تبدیل خاکستری به RGB**
حالت پیچیده‌تر دیگر اگر نیاز به تبدیل تصویر خاکستری PSD به تصویر RGB داشته باشید.

تصاویر خاکستری تنها یک کانال دارند، اما تصاویر RGB سه کانال دارند: R - قرمز، G - سبز، B - آبی. Aspose.PSD قادر است خاکستری را به RGB تبدیل کند.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
