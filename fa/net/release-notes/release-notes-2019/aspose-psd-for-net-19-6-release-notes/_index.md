---
title: Aspose.PSD برای .NET 19.6 - یادداشت‌های نسخه
type: docs
weight: 70
url: /fa/net/aspose-psd-for-net-19-6-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-127|قابلیت تبدیل پرونده PSD به PSB و بالعکس|ویژگی|
|PSDNET-154|پورت کردن منابع Aspose.Imaging 19.5 به Aspose.PSD|بهبود|
|PSDNET-155|پاک‌سازی API عمومی مرتبط با Aspose.PSD|بهبود|
|PSDNET-159|حذف ویژگی IsLicensed|بهبود|
|PSDNET-102|تبدیل PSB به JPG متوقف می‌شود|اشکال|
|PSDNET-150|لایه متنی جدید اضافه شده در موقعیت نادرستی در ویرایش در فتوشاپ جابه‌جا می‌شود|اشکال|

## **تغییرات در API عمومی**
# **APIهای اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F:Aspose.PSD.FileFormat.Cdr
- F:Aspose.PSD.FileFormat.Cmx
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P:Aspose.PSD.Image.BufferSizeHint
- P:Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M:Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P:Aspose.PSD.LoadOptions.BufferSizeHint
- T:Aspose.PSD.MemoryManagement.Configuration
- P:Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T:Aspose.PSD.ResolutionUnit
- F:Aspose.PSD.ResolutionUnit.None
- F:Aspose.PSD.ResolutionUnit.Inch
- F:Aspose.PSD.ResolutionUnit.Cm
# **APIهای حذف شده:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
...

## **مثال‌های استفاده:**
**PSDNET-127. قابلیت تبدیل پرونده PSD به PSB و بالعکس**

{{< highlight java >}}

 // قابلیت تبدیل پرونده PSD به PSB و بالعکس

            string sourceFilePathPsb = "2layers.psb";

            string outputFilePathPsd = "ConvertFromPsb.psd";

            using (Image img = Image.Load(sourceFilePathPsb))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psd };

                img.Save(outputFilePathPsd, options);

            }

            string sourceFilePathPsd = "2layers.psd";

            string outputFilePathPsb = "ConvertFromPsd.psb";

            using (Image img = Image.Load(sourceFilePathPsd))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psb };

                img.Save(outputFilePathPsb, options);

            }

{{< /highlight >}}

**PSDNET-102. تبدیل PSB به JPG متوقف می‌شود**

{{< highlight java >}}

  // تبدیل PSB به JPG متوقف می‌شود  

            string[] sourceFileNames = new string[] { 

...

{{< /highlight >}}

**PSDNET-150: لایه متنی جدید اضافه شده در موقعیت نادرستی در ویرایش در فتوشاپ**

{{< highlight java >}}

             // لایه متنی جدید اضافه شده در موقعیت نادرستی در ویرایش در فتوشاپ

    string sourceFileName = "OneLayer.psd";

    string exportPath = "...

{{< /highlight >}}```

OneLayer_Edited.psd";

    int leftPos = 99;

    int topPos = 47;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        im.AddTextLayer("متنی", new Rectangle(leftPos, topPos, 99, 47));

        TextLayer textLayer = (TextLayer)im.Layers[1];

        if (textLayer.Left != leftPos || textLayer.Top != topPos) 

        {

            throw new Exception("لایه متنی ایجاد شده نادرست است");

        }

        im.Save(exportPath);

    }

{{< /highlight >}}
```