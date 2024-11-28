---
title: دفاتر کلاسه Aspose.PSD CLI NLP برای .NET 24.6 - یادداشت های انتشار
type: docs
weight: 90
url: /fa/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

این صفحه حاوی یادداشت های انتشار برای [Aspose.PSD CLI NLP Editor برای .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/) می‌باشد.

{{% /alert %}}

| **کلید**   | **خلاصه**                                                                                     | **دسته‌بندی** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | انتشار اولیه برنامه های کلای Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor |  ارتقاء |


## **مثال‌های استفاده:**


**PSDNET-2110. انتشار اولیه برنامه کلای Aspose.PSD CLI NLP Editor**

## **استفاده از خط فرمان:**


{{% alert color="primary" %}}
ابتدا این ابزار دات‌نت را نصب کنید:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

قبل از استفاده اولین بار از اجرای این فرمان پیشنهاد می‌شود:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
بعد از این دستور، قادر خواهید بود که این برنامه را با نام کوتاه nlp.cli اجرا نمایید به‌جای Aspose.PSD.CLI.NLP.Editor. می‌توانید نام کوتاه خود را مشخص کنید.
{{% /alert %}}

**مثال‌های استفاده**

1. این فرمان فایل اولیه (که می‌تواند با aspose.psd باز شود) را از پوشه فعلی تبدیل به فرمت png با شفافیت خواهد کرد. همچنین، لایسنس تعیین خواهد شد. شما تنها یکبار باید لایسنس را مشخص کنید. اجراهای بعدی لایسنس از مسیر مشخص‌شده استفاده خواهد کرد. این فرمان گزاره verbose log پردازش NLP را نمایش خواهد داد اگر در دسترس باشد.
{{< highlight bash >}}nlp.cli فایل را از این پوشه به فرمت png با alpha تبدیل کنید --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}


2. این فرمان فایلی را با نام بیشترین شباهت با "smth.psd" پیدا می‌کند. سپس تنظیمات کنتراست را اعمال و آن را با بهترین کیفیت به فرمت jpeg ذخیره خواهد کرد. نام فایل خروجی چاپ خواهد شد. این فایل smth.jpg خواهد بود.
{{< highlight bash >}}تنظیم کنتراست روی 10 از لایه با نام ellipse در فایل smth.psd و ذخیره آن به output.jpg با بهترین کیفیت{{< /highlight >}}


3. این فرمان فایل را در مسیر مشخص‌شده پیچیده و اندازه آن را به 25٪ کاهش خواهد داد. فایل خروجی چاپ خواهد شد. آن در پوشه فعلی کنسول ذخیره خواهد شد.
{{< highlight bash >}}تغییر اندازه فایل C:\Users\someuser\Desktop\input.psd به 25%{{< /highlight >}}


4. این فرمان فایل input.psd را در C:\Users\someuser\Desktop\ پیدا خواهد کرد. سپس لایه با شاخص 3 را پیدا کرده و آن را به عرض 50px و ارتفاع 100px تغییر اندازه خواهد داد. سپس این لایه را به عنوان PDF در C:\Users\someuser\Desktop\output.pdf ذخیره خواهد کرد.
{{< highlight bash >}}تغییر اندازه لایه با شاخص 3 از C:\Users\someuser\Desktop\input.psd به عرض 50 و ارتفاع 100 و ذخیره آن در C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}


5. این فرمان فایل smth.psd را در پوشه فعلی باز خواهد کرد، اما همه اثرات غیرفعال خواهند شد. و سپس این فایل را به فرمت BMP تبدیل و به عنوان output.bmp در پوشه فعلی ذخیره خواهد کرد.
{{< highlight bash >}}Open smth.psd بدون اثرات و آن را به عنوان output.bmp ذخیره کنید{{< /highlight >}}


**اخطار**

این یک برنامه آزمایشی می‌باشد. لطفاً آن را امتحان کرده و بازخورد خود را ارسال کنید. هر گونه بازخورد قدردانی خواهد شد. ما می‌خواهیم برنامه NO-Code را به سطح بعدی برسانیم. ادغام آسان با هر لوله سازی ساخت یا فرآیند تجاری هدف ما است.
