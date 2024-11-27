---
title: اسپوز.PSD برای .NET 21.2 - یادداشت‌های انتشار
type: docs
weight: 110
url: /fa/net/aspose-psd-for-net-21-2-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار برای [Aspose.PSD برای .NET 21.2](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته بندی**|
| :- | :- | :- |
|PSDNET-404|پشتیبانی از vogkResource|ویژگی|
|PSDNET-809|ترازمندی‌های لایه اشیای هوشمند نادرست هنگامی که محتوای اشیای هوشمند را با فایلی با ابعاد و وضوح متفاوت جایگزین می‌کنیم|ویژگی|
|PSDNET-752|خطا: عدم تبدیل لایه FillLayer به SmartObjectLayer|خطا|
|PSDNET-778|اضافه کردن لایه گروه در ترتیب معکوس لایه‌های جدید|خطا|
|PSDNET-790|وارد کردن تصویر در لایه SmartObject منجر به خرابی PSD می‌شود|خطا|
|PSDNET-810|استثناء در هنگام بارگذاری فایل‌ها|خطا|
|PSDNET-824|منبع vogk نادرست پس از بارگذاری و ذخیره تصویر PSD با لایه‌های شکل و مسیرهای برداری|خطا|
|PSDNET-827|استثناء در بارگذاری ساختار ReferenceStructure و EnumeratedReferenceStructure|خطا|

## **تغییرات API عمومی**
# **API‌های اضافه:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginType
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginResolution
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginShapeBox
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginRadiiRectangle
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidatedPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginIndexPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginTypePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginResolutionPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginRadiiRectanglePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginShapeBBoxPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Left
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Top
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Right
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bottom
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.QuadVersion
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bounds
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.QuadVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.String,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(Aspose.PSD.Image,Aspose.PSD.ResolutionSetting)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(System.String,Aspose.PSD.ResolutionSetting)

# **API‌های حذف شده:**
- هیچ یک

## **مثال‌های استفاده:**

**PSDNET-404. پشتیبانی از vogkResource**

{{< highlight csharp >}}
            // این مثال نشان می‌دهد که بارگذاری و ذخیره تصویر PSD با لایه‌های شکل و مسیرهای برداری به درستی کار می‌کند.
{{< /highlight >}}

**PSDNET-752. خطا: عدم تبدیل FillLayer به SmartObjectLayer**

{{< highlight csharp >}}
            // کد‌های نمونه
{{< /highlight >}}

**PSDNET-778. اضافه کردن گروه لایه با ترتیب معکوس**

{{< highlight csharp >}}
            // کد‌های نمونه
{{< /highlight >}}

**PSDNET-790. وارد کردن تصویر در لایه SmartObject منجر به خرابی PSD می‌شود**

{{< highlight csharp >}}
            // کد‌های نمونه
{{< /highlight >}}

**PSDNET-809. اشتباه در ترازمندی لایه‌های هوشمند هنگام جایگزینی محتوای اشیای هوشمند با فایلی که ابعاد و وضوح متفاوت دارد**

{{< highlight csharp >}}
            // کد‌های نمونه
{{< /highlight >}}

**PSDNET-810. استثنا در هنگام بارگذاری فایل‌ها**

{{< highlight csharp >}}
            // کد‌های نمونه
{{< /highlight >}}

**PSDNET-824. منبع vogk نادرست پس از بارگذاری و ذخیره تصویر PSD با لایه‌های شکل و مسیرهای برداری**

{{< highlight csharp >}}
            // این مثال نشان می‌دهد که بارگذاری و ذخیره تصویر PSD با لایه‌های شکل و مسیرهای برداری به درستی کار می‌کند و ویژگی‌های Live Shape حفظ می‌شود.
{{< /highlight >}}

**PSDNET-827. استثناء در بارگذاری ساختار ReferenceStructure و EnumeratedReferenceStructure**

{{< highlight csharp >}}
            // کد‌های نمونه
{{< /highlight >}}