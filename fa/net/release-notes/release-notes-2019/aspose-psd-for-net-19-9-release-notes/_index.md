---
title: یادداشت های آگاهی Aspose.PSD برای .NET 19.9
type: docs
weight: 40
url: /fa/net/aspose-psd-for-net-19-9-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی یادداشت های آگاهی برای [Aspose.PSD برای .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/) است.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-160|اشتباه در استخراج نام لایه|ویژگی|
|PSDNET-175|دریافت ویژگی های متن از قسمت متفاوت متن درون لایه متن PSD|ویژگی|
|PSDNET-190|پشتیبانی از اضافه کردن گروه لایه|ویژگی|
|PSDNET-192|پشتیبانی از ویژگی مقیاس برای لایه پر کردن گرادیان|ویژگی|
|PSDNET-162|تنظیم روشنایی|افزایش|
|PSDNET-174|IndexOutOfRangeException در زمان ذخیره تصویر PSD به عنوان JPEG|اغلاط|
|PSDNET-180|به‌روزرسانی متن لایه متن باعث پرتاب استثنا می‌شود|اغلاط|
|PSDNET-182|ذخیره تصویر PSD پس از عملیات RotateFlip یک فایل خراب تولید می‌کند که نمی‌توان آن را باز کرد|اغلاط|

## **تغییرات API عمومی**
# **API های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- ...

## **مثال‌های استفاده:**
**PSDNET-160. اشتباه در استخراج نام لایه**

برای نمایش نام لایه به درستی از خاصیت **DisplayName** استفاده کنید. یک setter برای این خاصیت اضافه شده است و می‌توان این خاصیت را ویرایش کرد. زمانی که Photoshop نام لایه را با استفاده از خاصیت Name ذخیره می‌کند، حروف کره‌ای به عنوان بایت 63'?' در ASCII ذخیره می‌شوند. از خاصیت **DisplayName** استفاده کنید زیرا خاصیت Name پشتیبانی از حروف کره‌ای را ندارد.

{{< highlight java >}}
...
{{< /highlight >}}

**PSDNET-175. دریافت ویژگی های متن از قسمت متفاوت متن درون لایه متن PSD**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDNET-190. پشتیبانی از اضافه کردن گروه لایه**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDNET-192. پشتیبانی از ویژگی مقیاس برای لایه پر کردن گرادیان**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDNET-174. IndexOutOfRangeException در زمان ذخیره تصویر PSD به عنوان JPEG**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDNET-180. به‌روزرسانی متن لایه متن باعث پرتاب استثنا می‌شود**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDNET-182. ذخیره تصویر PSD پس از عملیات RotateFlip یک فایل خراب تولید می‌کند که نمی‌توان آن را باز کرد**

{{< highlight java >}}
...
{{< /highlight >}}