---
title: استفاده از فایل‌های PSD به عنوان قالب‌ها برای اتوماسیون - مورد کارت‌های تجاری
type: docs
weight: 10
url: /fa/net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **مرور**
این مقاله موارد استفاده‌شده اغلب را توضیح می‌دهد که کیش‌هایی روزآمد هستند که نیاز دارید تا برخی از لایه‌ها را به صورت برنامه‌نویسی در [فایل PSD](https://wiki.fileformat.com/image/psd/) به‌روز کنید، جائی که فایل PSD/PSB یک ساختار مانند قالب شناخته‌شده دارد. این می‌تواند برای ایجاد تعداد زیادی از کارت‌های تجاری برای افراد مختلف استفاده شود (مورد کارت‌های تجاری). یا نیاز دارید که یک ترجمه از فایل PSD به زبان‌های مختلف با جایگزینی برخی از مطالب گرافیکی در آن ایجاد کنید.

بعد از خواندن این مقاله خواهید دانست که چگونه می‌توانید این کار را انجام دهید:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **مورد ساده**
به عنوان مثال، شما یک قالب PSD با نام‌های لایه‌های شناخته‌شده دارید. بنابراین شما نیاز دارید تا با استفاده از زبان C# لایه PSD را تغییر، به‌روز و یا جایگزین کنید. در ابتدا شما باید فایل قالب را با Aspose.PSD باز کنید.

چگونه فایل PSD را از طریق C# باز کنیم؟

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

سپس ما نیاز داریم تا یک لایه‌ای که می‌خواهیم با نام آن جایگزین کنیم بیابیم. در ادامه یک اجرای ساده برای این کار وجود دارد.

چگونه لایه را در فایل PSD بر اساس نام آن پیدا کنیم

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



هنگامی که لایه پیدا شود، می‌توانیم آن را به روش عمومی به‌روز کنیم، با استفاده از [گرافیک](https://reference.aspose.com/psd/net/aspose.psd/graphics):

چگونه بر روی لایه PSD گرافیک کشیم

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

در این مورد، ما یک تصویر [PNG](https://wiki.fileformat.com/image/png/) جدید را بر روی لایه PSD وجودی کشیده‌ایم، بنابراین اطلاعات قدیمی در فایل جدید از بین می‌روند.

اما اگر نیز نیاز داریم تا متن را به‌روز کنیم؟ فرآیند مشابه خواهد بود. لایه [متن](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) را بر اساس نام آن پیدا کرده و سپس [لایه متن را در فایل فتوشاپ به‌روز کنیم](/psd/fa/net/render-text-with-different-colors-in-text-layer/).


چگونه متن لایه را در فتوشاپ با استفاده از C# به‌روز کنیم

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



در انتها نیاز داریم تا تغییرات خود را ذخیره کنیم:

چگونه فایل PSD تغییر یافته را با استفاده از [Aspose.PSD](https://products.aspose.com/psd/net) ذخیره کنیم

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



تصویر نهایی:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **مورد پیچیده‌تر با ویژگی‌های اضافی**
در بالا ما روش ساده‌تری را برای جایگزینی تصویر در یک لایه از فایل PSD نشان دادیم.

اما Aspose.PSD می‌تواند ویژگی‌های اضافی پیچیده‌تری مانند اضافه کردن یک لایه جدید، حذف کردن لایه‌های قدیمی و به‌روزرسانی لایه متن با استفاده از استیل‌های مختلف در متن چند خطی ارائه دهد.

ما می‌توانیم [لایه](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer)ای که می‌خواهیم جایگزین کنیم را پیدا کنیم، سپس شاخص آن را در لیست لایه‌ها پیدا کرده، آن را حذف کرده و بعد از ایجاد آن از [فایل Jpeg](https://wiki.fileformat.com/image/jpeg/) لایه جدید را در همان مکان قرار دهیم.

ایجاد یک لایه جدید از فایل و آن‌را به تصویر PSD با استفاده از [Aspose.PSD](https://products.aspose.com/psd/net) وارد کنید

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



به انتهای این قطعه کد فایل، ما موقعیت لایه را تصحیح می‌کنیم و آرایه لایه‌های جدید را به Psd Image ذخیره می‌کنیم.

چگونه ویژگی‌های لایه [PsdImage ](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage) را کپی کنیم

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



و در پایان، ما نیاز داریم تا لایه‌های متنی در تصویر PSD موجود را به کمک C# به‌روز کنیم. Aspose.PSD از [به‌روزرسانی لایه‌های متنی با بخش‌ها](/psd/fa/net/working-with-text-layers/) پشتیبانی می‌کند. هر [بخش متنی](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) ترکیبی منحصربه‌فرد از خصوصیت‌های استایل و پاراگراف را دارد.

چگونه ویژگی‌های لایه [PsdImage ](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage) را کپی کنیم

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



بنابراین، ما قالب PSD را از طریق کد با یک لایه جدید از فایل Jpeg، Png، J2k، Bmp، Gif، یا Tiff و یا متن چندخطی با [استایل‌های مختلف](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) در هر خط تغییر داده‌ایم.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
