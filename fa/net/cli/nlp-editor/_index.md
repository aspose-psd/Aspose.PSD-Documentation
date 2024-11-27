---
title: برنامه ویرایشگر NLP CLI Aspose.PSD برای .NET
type: docs
weight: 10
url: /fa/net/cli/nlp-editor/
is_root: false
keywords: ابزار CLI فتوشاپ NLP پردازش زبان طبیعی فرمت فایل PSD کتابخانه C# API PSD مبتنی بر Aspose.PSD
description: برنامه Aspose.PSD CLI NLP Editor برای فرمت‌های فایل PSD، PSB و AI بدون نیاز به نصب Adobe Photoshop یا Adobe Illustrator و قابل اجرا از طریق کنسول بدون کد اضافی است. این برنامه از پردازش زبان طبیعی برای ویرایش فایل‌های PSD پشتیبانی می‌کند.
---

**![لوگو محصول Aspose.PSD برای .NET](home_1.png)**

**خوش آمدید به برنامه ویرایشگر NLP CLI Aspose.PSD برای .NET**

برنامه ویرایشگر NLP CLI Aspose.PSD یک ابزار کنسولی سبک برای ویرایش فایل‌های PSD با استفاده از دستورات زبان طبیعی است. ادغام آسان در لوله‌های CI/CD.

**توجه**

این یک برنامه تجربی است. لطفاً آن را امتحان کنید و بازخورد خود را اعلام کنید. هر گونه بازخورد بسیار قدردانی شده است. ما می‌خواهیم به سطح بالاتری از برنامه بدون کد برسیم. ادغام آسان با هر لوله ساخت یا فرآیند تجاری، هدف ما است.

**اصلی‌ترین قابلیت‌های برنامه ویرایشگر NLP CLI Aspose.PSD برای .NET**

1. انجام عملیات بر روی فایل‌های PSD، PSB، AI با استفاده از دستورات زبان طبیعی.
2. پشتیبانی از عملیات‌های مختلف مانند تبدیل، تنظیم، تغییر اندازه و غیره.
3. اتوماسیون CI/CD بدون نیاز به کد.
4. پشتیبانی از نوشتن درخواست‌ها به زبان طبیعی برای ویرایش فایل‌های PSD.

## **استفاده از خط فرمان:**

{{% alert color="primary" %}}
اولین کار نصب این ابزار dotnet است:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

پیشنهاد می‌کنیم قبل از استفاده از نسخه اولین، دستور زیر را اجرا کنید:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
پس از این دستور، شما قادر به اجرای این برنامه با نام کوتاه nlp.cli به جای Aspose.PSD.CLI.NLP.Editor خواهید بود. شما می‌توانید نام خود را مشخص کنید.
{{% /alert %}}

**پارامترهای موجود برای ابزار Aspose.PSD.CLI.Crop**

| **آرگومان** | **توضیح**                         |
|:-------------|:----------------------------------------|
| هر متن     | ضروری. فرمان خود در زبان طبیعی برای به‌روزرسانی فایل PSD یا PSB      |
| لایسنس      | مسیر لایسنس.                    |
| وربوز      | نمایش اطلاعات بیشتر در یک فرمان خاص. |
| تنظیم        | ایجاد فایل bat در پوشه‌های ابزار برای فراخوانی سریع از کنسول. مثال: --setup psd.nlp. سپس شما می‌توانید ابزار را با فرمان psd.nlp فراخوانی کنید |

**مثال‌های استفاده**

1. این دستور اولین فایل پیداشدنی را (که با aspose.psd قابل باز شدن است) از پوشه فعلی تبدیل و آن را به فرمت png با شفافیت ذخیره می‌کند. همچنین، لایسنس تنظیم می‌شود. شما تنها باید یک بار لایسنس را مشخص کنید. در اجراهای بعد، لایسنس از مسیر مشخص شده استفاده خواهد شد. اگر پردازش NLP در دسترس باشد، این دستور لاگ وربوز پردازش NLP را نشان خواهد داد.
{{< highlight bash >}}
  nlp.cli تبدیل فایل از این پوشه به فرمت png با آلفا --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. این دستور فایلی را که نام مشابه‌ترین به "smth.psd" است پیدا می‌کند. سپس کنتراست آن را تنظیم می‌کند و آن را با بهترین کیفیت به فرمت jpeg ذخیره می‌کند. نام فایل خروجی چاپ خواهد شد. این فایل smth.jpg خواهد بود.
{{< highlight bash >}}
 تنظیم کنتراست در 10 از لایه با نام ellipse در فایل smth.psd و ذخیره آن به output.jpg با بهترین کیفیت
{{< /highlight >}}

3. این دستور فایل را در مسیر مشخص شده پیدا کرده و اندازه آن را به 25٪ کاهش می‌دهد. فایل خروجی چاپ خواهد شد. این فایل در پوشه فعلی کنسول ذخیره خواهد شد.
{{< highlight bash >}}
اندازه فایل C:\Users\someuser\Desktop\input.psd را به 25٪ کاهش دهید
{{< /highlight >}}

4. این دستور فایل input.psd را در C:\Users\someuser\Desktop\ پیدا خواهد کرد. سپس لایه با شماره 3 را پیدا کرده و آن را به عرض 50 پیکسل و ارتفاع 100 پیکسل تغییر اندازه می‌دهد. سپس این لایه به صورت PDF در C:\Users\someuser\Desktop\output.pdf ذخیره می‌کند.
{{< highlight bash >}}
 تغییر اندازه لایه با شماره 3 از C:\Users\someuser\Desktop\input.psd به عرض 50 و ارتفاع 100 و آن را در C:\Users\someuser\Desktop\output.pdf ذخیره کنید
 {{< /highlight >}}

 5. این دستور فایل smth.psd را در پوشه فعلی باز می‌کند، اما تمام اثرات غیرفعال خواهند بود. و سپس این فایل را به فرمت BMP تبدیل می‌کند و به output.bmp در پوشه فعلی ذخیره می‌کند.
 {{< highlight bash >}}
 باز کردن smth.psd بدون اثرات و ذخیره آن به output.bmp
  {{< /highlight >}}

**لطفاً سایر [برنامه‌های CLI Aspose.PSD](https://docs.aspose.com/psd/net/cli) برای .NET را برای افزودن پشتیبانی از فرمت‌های PSD، PSB و AI به گردش کار خود بررسی کنید**

1. [Aspose.PSD CLI Convert](/psd/fa/net/cli/convert)
2. [Aspose.PSD CLI Crop](/psd/fa/net/cli/crop)
3. [Aspose.PSD CLI Resize](/psd/fa/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/fa/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/fa/net/cli/nlp-editor)

**لطفاً [Aspose.PSD برای .NET](https://releases.aspose.com/psd/net/) یا [پلتفرم‌های دیگر]** را بررسی کنید

برنامه‌های CLI Aspose.PSD یک راه‌حل آماده برای عملیات محبوب هستند. اگر به یک راه‌حل انعطاف‌پذیر نیاز دارید، لطفاً نسخه کامل Aspose.PSD را بررسی کنید

1. [Aspose.PSD برای .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD برای Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD برای Python via .NET](https://releases.aspose.com/psd/python-net/)

## **منابع Aspose.PSD برای .NET**

در زیر لینک‌هایی به منابع مفیدی آورده شده است که ممکن است برای انجام وظایف خود نیاز داشته باشید.

- [مستندات آنلاین برنامه‌های CLI Aspose.PSD برای .NET](/psd/fa/net/cli/conversion)
- [یادداشت‌های انتشار برنامه‌های CLI Aspose.PSD برای .NET](/psd/fa/net/cli/conversion/release-notes/)
- [صفحه محصول برنامه‌های CLI Aspose.PSD برای .NET](https://products.aspose.com/psd/net/cli)
- [راهنمای مرجع API Aspose.PSD برای .NET](https://reference.aspose.com/net/psd)
- [دانلود نمونه‌ها در مخزن GitHub](https://github.com/aspose-psd/CLI-Applications)
- [انجمن پشتیبانی رایگان Aspose.PSD برای .NET](https://forum.aspose.com/c/psd)
- [دفترچه راهنمای پشتیبانی پولی Aspose.PSD برای .NET](https://helpdesk.aspose.com/)
