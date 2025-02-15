---
title: مثال استفاده از لایه‌های گروهی در Aspose.PSD برای C#
weight: 100
type: docs
description: استفاده از لایه گروهی در فایل PSD از طریق C#
keywords: [لایه گروه، گروه لایه، افزودن لایه به گروه، پی‌اس‌دی ای‌پی‌آی، سی‌شارپ، کد نمونه]
url: fa/net/psd-group-layer/
---

## مرور

لایه‌های گروهی در Aspose.PSD برای C# امکان سازماندهی و دستکاری بهینه لایه‌ها در یک فایل PSD را فراهم می‌کنند. با استفاده از لایه‌های پوشه، شما می‌توانید چندین لایه را با هم گروه‌بندی کرده و تبدیلات یا اثراتی را بر روی کل گروه اعمال کنید.

این مثال ایجاد یک تصویر PSD جدید با استفاده از `PsdImage.Create` را نشان می‌دهد. سپس، یک شیء `LayerGroup` با استفاده از `AddLayerGroup` از شیء `PsdImage` ایجاد می‌شود. لایه گروه با نام "پوشه" ایجاد می‌شود، در فهرست 0 قرار داده می‌شود و قابل مشاهده قرار داده می‌شود.

سپس، دو شیء `Layer` با تنظیمات خود برای `DisplayName` ایجاد می‌شوند. این لایه‌ها به لایه گروه با استفاده از `AddLayer` اضافه می‌شوند.

لایه‌های درون گروه می‌توانند از طریق خاصیت `Layers` شیء `LayerGroup` دسترسی داشته باشند. این مثال ادعا می‌کند که نام نمایش اولین و دومین لایه‌ها در گروه "لایه 1" و "لایه 2" هستند.

پس از اصلاح لایه‌های گروه، تصویر PSD به‌روزرسانی شده با استفاده از متد `Save` شیء `PsdImage` ذخیره می‌شود.

این مثال ابتدایی، نحوه کار با لایه‌های گروهی با استفاده از Aspose.PSD برای C# را معرفی می‌کند. این کتابخانه ویژگی‌های پیشرفته‌ای برای دستکاری و تبدیل لایه‌ها در فایل‌های PSD ارائه می‌دهد. برای کسب اطلاعات جزئی‌تر و مثال‌های بیشتر، به مستندات Aspose.PSD برای C# مراجعه کنید.

در زیر، یک کد نمونه که استفاده از لایه‌های گروهی در Aspose.PSD برای C# را نشان می‌دهد:

## مثال

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

برای اطلاعات و مثال‌های جزئی‌تر، لطفاً به [مستندات Aspose.PSD برای C#](https://docs.aspose.com/psd/net/) مراجعه نمایید.
