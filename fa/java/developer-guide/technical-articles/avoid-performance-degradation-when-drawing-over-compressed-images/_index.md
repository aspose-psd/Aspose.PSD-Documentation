---
title: جلوگیری از کاهش عملکرد هنگام رسم روی تصاویر فشرده
type: docs
weight: 40
url: /fa/java/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **جلوگیری از کاهش عملکرد هنگام رسم روی تصاویر فشرده**
بعضی اوقات ممکن است بخواهید عملیات گرافیکی بسیار گسترده‌ای را روی یک تصویر فشرده انجام دهید. وقتی Aspose.PSD بخواهد تصاویر را در حالت فشرده و غیر فشرده کند، ممکن است کاهش عملکرد رخ دهد. رسم روی تصاویر فشرده همچنین ممکن است باعث جریمه در عملکرد شود.
### **راه حل**
برای جلوگیری از کاهش عملکرد، توصیه می‌کنیم تصویر را به یک فرمت غیر فشرده یا raw تبدیل کنید قبل از انجام عملیات گرافیکی.
### **استفاده از مسیر فایل**
در مثال زیر، یک تصویر PSD به فرمت raw (بدون فشرده سازی) تبدیل شده و بر روی دیسک ذخیره می‌شود. سپس تصویر غیر فشرده قبل از انجام عملیات گرافیکی روی آن بارگذاری می‌شود. این تکنیک همچنین برای فایل‌های BMP و GIF قابل اجرا است.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **استفاده از یک شیء جریان**
قطعه کد زیر نحوه تبدیل تصویر PSD به فرمت raw (بدون فشرده سازی) و ذخیره آن بر روی دیسک با استفاده از جریان را نشان می‌دهد.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
