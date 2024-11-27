---
title: جلوگیری از کاهش عملکرد هنگام رسم بر روی تصاویر فشرده شده
type: docs
weight: 10
url: /fa/net/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **جلوگیری از کاهش عملکرد هنگام رسم بر روی تصاویر فشرده شده**
بعضی وقت‌ها نیاز است که عملیات گرافیکی بسیار گسترده‌ای را بر روی تصویر فشرده انجام دهید. هنگامی که Aspose.PSD مجبور به فشرده‌سازی و از حالت فشرده خارج کردن تصاویر در حال اجرا باشد، کاهش عملکرد ممکن است رخ دهد. رسم بر روی تصاویر فشرده همچنین ممکن است بازه‌ای عملکردی را به همراه داشته باشد.
### **راه‌حل**
برای جلوگیری از کاهش عملکرد، توصیه می‌کنیم تصویر را به یک فرمت فشرده‌نشده ‌یا raw، تبدیل کنید قبل از انجام عملیات گرافیکی.
### **استفاده از مسیر فایل**
در مثال زیر، یک تصویر PSD به فرمت raw (بدون فشرده‌سازی) تبدیل شده و در دیسک ذخیره می‌شود. سپس تصویر فشرده‌نشده باز می‌شود قبل از انجام عملیات گرافیکی بر روی آن. این تکنیک به همان اندازه برای فایل‌های BMP و GIF نیز صدق می‌کند.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **استفاده از یک شیء جریان**
کد مثال زیر نشان می‌دهد که چگونه تصویر PSD به فرمت raw (بدون فشرده‌سازی) تبدیل شده و با استفاده از MemoryStream در دیسک ذخیره شده است.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
