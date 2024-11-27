---
title: ویرایش ماسک لایه‌های رستر در فایل PSD از طریق API
type: docs
weight: 20
url: /fa/editing-raster-layer-masks-in-psd-file-via-api/
---

## **بررسی کلی**
**جهت خودکارسازی ویرایش فرمت PSD و تغییر فایل PSD بدون استفاده از Adobe® Photoshop® می‌توانید از API Aspose.PSD استفاده کنید که در زیر ارائه شده است. در اینجا قطعات کد C# و .NET وجود دارد که می‌تواند به شما در تغییر فایل‌های PSD کمک کند.**

با استفاده از ماسک‌های لایه و وکتور PSD، می‌توانیم پیکسل‌های لایه را مخفی کرده و نمایش دهیم بدون حذف دائمی آن‌ها. ماسک‌های رستر همچنین به عنوان یک ماسک لایه یا ماسک کاربر شناخته می‌شوند. دسترسی به هر دو ماسک رستر و وکتور در Aspose.PSD از طریق خصوصیت لایه [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) فراهم شده است که ممکن است شامل نمونه‌های کلاس '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' و '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' باشد که کلاس‌های فرزند کلاس انتزاعی 'LayerMaskData' هستند. در صورت داشتن هر دو ماسک رستر و وکتور در یک لایه، نمونه [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull) ارائه می‌شود. اگر یک لایه تنها یک ماسک رستر یا یک ماسک وکتور دارد، نمونه [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort) ارائه می‌شود. اگر خاصیت LayerMaskData مقدار null داشته باشد، به این معنی است که لایه هیچ ماسکی ندارد یا فقط یک ماسک وکتور غیرفعال دارد.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>یک ماسک رستر و یک ماسک وکتور غیرفعال از نوع LayerMaskDataShort</p><p>یک ماسک رستر غیرفعال از نوع LayerMaskDataShort</p><p>یک ماسک رستر و یک ماسک وکتور از نوع LayerMaskDataFull</p><p>یک ماسک رستر از نوع LayerMaskDataShort</p><p>یک ماسک وکتور از نوع LayerMaskDataShort</p><p>یک ماسک وکتور غیرفعال (اما منبع وکتور وجود دارد)</p>|
| :- | :- |

## **چگونه می‌توان یک ماسک رستر لایه را در فایل PSD بگیریم؟**
ابتدا باید مشخص کنیم که آیا یک لایه هر دو ماسک وکتور و لایه دارد یا خیر:

کد نمونه زیر نشان می‌دهد چگونه ماسک رستر لایه را بدست آوریم

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

در غیر این صورت، نوع خصوصیت LayerMaskData Layer LayerMaskDataShort است. در این صورت، بیایید بررسی کنیم که آیا لایه تنها دارای یک ماسک رستر است یا خیر با بررسی خصوصیت Flags. باید حاوی [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** پرچم نباشد، در غیر این صورت ماسک یک کش وکتور است**.**

برای گرفتن کد ماسک:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

اگر نیاز به **استخراج یک ماسک رستر** به عنوان LayerMaskDataShort (برای عملیات بعدی) حتی زمانی که هر دو ماسک وجود دارند، LayerMaskDataFull باید استخراج و به LayerMaskDataShort تبدیل شود. کد زیر برای هر دو حالت قابل استفاده است:

استخراج ماسک رستر از PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **چگونه می‌توان چک کرد که یک لایه در فایل PSD ماسک رستر دارد؟**
کد C# زیر ممکن است به شما کمک کند تا چک کنید که یک لایه دارای ماسک رستر است:

چگونگی اطلاع از اینکه آیا ماسک رستر به [لایه PSD](/psd/fa/net/psd-layer/) اعمال شده است

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **چگونه می‌توان یک ماسک رستر لایه را در فایل PSD حذف / اضافه / به‌روز کرد؟**
فقط حذف / اضافه / به‌روز کردن LayerMaskData کافی نیست برای ذخیره‌سازی صحیح زیرا کانال‌ها به‌روز نمی‌شوند؛ هر چند ممکن است نمایش صحیحی فراهم کند. این باعث تغییر کانال‌های ماسک نمی‌شود:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

باید از روش AddLayerMask لایه برای حذف / اضافه / به‌روز کردن استفاده کنیم.

این همچنین ماسک و کانال‌ها را اضافه / به‌روز می‌کند:

{{< gist "aspose-com-gists" "8a4c7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

این همچنین هر دو ماسک و کانال‌ها را حذف می‌کند:

{{< gist "aspose-com-gists" "8a4c7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **حذف یک ماسک رستر لایه در تصویر PSD**
ابتدا، باید بررسی کنیم که آیا ماسک در فرمت کوتاه است و اگر وجود ندارد با فراخوانی AddLayerMask می‌توانیم ماسک رستر را حذف کنیم. اما اگر در فرمت کامل باشد، باید آن را به فرمت کوتاه تبدیل کرده و فقط ماسک وکتور را باقی بگذاریم. برای حذف یک ماسک لایه می‌توان از این قطعه کد C# .NET استفاده کرد:

قطعه کد چگونگی حذف ماسک لایه از فایل PSD.

{{< gist "aspose-com-gists" "8a4c7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **به‌روز‌رسانی یک ماسک رستر لایه در تصویر PSD**
این کار آسان است: اگر ماسک در فرمت کوتاه باشد، باید ImageData و MaskRectangle را تغییر می‌دهیم، در غیر این صورت باید [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)و [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle) را تغییر دهیم. این قطعه کد C# .NET می‌تواند برای به‌روز‌رسانی یک ماسک لایه استفاده شود:

به‌روزرسانی ماسک لایه PSD با C#

{{< gist "aspose-com-gists" "8a4c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

در ادامه، یک مثال از اقدامات ممکن که ماسک رستر را تغییر می‌دهد آورده شده است. این مثال یک ماسک کاربر را معکوس می‌کند:

به‌روزرسانی ماسک لایه PSD با C#

{{< gist "aspose-com-gists" "8a4c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **به‌روز‌رسانی یک ماسک وکتور در فایل PSD هنگامی که یک ماسک رستر لایه وجود دارد**
فرض بر این است که مسیر وکتور را کاربر قبلاً تغییر داده است. سپس می‌تواند به‌سادگی ماسک وکتور را با فراخوانی متد لایه [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask) به‌روز کند:

به‌روز‌رسانی [ماسک وکتور لایه PSD](/psd/fa/net/layer-vector-mask/) با C#

{{< gist "aspose-com-gists" "8a4c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **افزودن یک ماسک رستر لایه در فایل PSD**
اگر یک لایه هیچ ماسکی نداشته باشد، می‌توانیم ماسک رستر داده داده شده را فقط با فراخوانی متد AddLayerMask لایه اضافه کنیم.

اگر ماسک [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)پرچم را نداشته باشد، به این معنی است که در حال حاضر دارای یک ماسک رستر است و باید آن را به‌روز کنیم همانند آنچه توضیح داده شده است. در غیر این صورت، اگر این ماسک در قالب کوتاه باشد، باید به قالب کامل تبدیل شود. در غیر این صورت، آن را به صورت عادی استفاده کنیم. سپس با ویژگی‌های داده شده ماسک، UserMaskData، UserMaskRectangle و سایر ویژگی‌ها را به‌روز نماییم. این قطعه کد C# .NET می‌تواند برای اضافه کردن (به‌روزرسانی) یک ماسک لایه مورد استفاده قرار گیرد:

اضافه کردن ماسک لایه جدید به PSD

{{< gist "aspose-com-gists" "8a4c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **چگونه می‌توان چک کرد که یک ماسک لایه فعال است؟**
برای دریافت وضعیت فعال بودن ماسک رستر لایه می‌توانیم وضعیت پرچم LayerMaskFlags.Disabled را در خصوصیت Flags برای LayerMaskDataShort یا در RealFlags برای LayerMaskDataFull بررسی کنیم. این قطعه کد C# .NET می‌تواند برای گرفتن وضعیت فعال بودن یک ماسک لایه استفاده شود:

بررسی اینکه ماسک فعال است:

{{< gist "aspose-com-gists" "8a4c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **چگونه می‌توان یک ماسک رستر لایه را فعال یا غیرفعال کرد؟**
برای فعال یا غیرفعال کردن یک ماسک رستر لایه می‌توانیم وضعیت پرچم LayerMaskFlags.Disabled را در خصوصیت Flags برای LayerMaskDataShort یا در RealFlags برای LayerMaskDataFull تغییر دهیم. ا
