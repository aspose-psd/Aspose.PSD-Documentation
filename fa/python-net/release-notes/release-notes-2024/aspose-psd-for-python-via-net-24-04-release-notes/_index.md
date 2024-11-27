---
title: یادداشت‌های نسخه 24.4 Aspose.PSD برای پایتون از طریق .NET
type: docs
weight: 10
url: /fa/python-net/aspose-psd-for-python-via-net-24-4-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه [Aspose.PSD برای پایتون از طریق .NET 24.4](https://pypi.org/project/aspose-psd/) می‌باشد.

{{% /alert %}}

| **کلید**     | **خلاصه**                                                                 | **دسته‌بندی**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [فرمت AI] اضافه کردن بررسی منبع XObjectForm                     | قابلیت     |
| PSDPYTHON-51 | اضافه کردن سازنده برای لایه شکل                                    | قابلیت     |
| PSDPYTHON-52 | رفع مشکل تبدیل فایل Psd از RGB به CMYK                            | باگ        |
| PSDPYTHON-53 | عدم امکان صادر کردن فایل خاص PSD با استفاده از Aspose.PSD         | باگ        |



## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **API‌های حذف شده:**
- هیچکدام


## **مثال‌های استفاده:**

**PSDPYTHON-50. [فرمت AI] اضافه کردن بررسی منبع XObjectForm**

{{< highlight python >}}
        نام_فایل_منبع = "مثال.ai"
        مسیر_خروجی = "خروجی_مثال.png"

        با AiImage.load(نام_فایل_منبع) as تصویر:
            تصویر.save(مسیر_خروجی, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. اضافه کردن سازنده برای لایه شکل**

{{< highlight python >}}
     def چک_سازنده_لایه_شکل():
        فایل_خروجی = "خروجی_اضافه_شکل.psd"

        with PsdImage(600, 400) as psd_جدید:
            لایه_شکل = psd_جدید.add_shape_layer()

            شکل_جدید = تولید_شکل_جدید(psd_جدید.size)
            شکل‌های_جدید = [شکل_جدید]
            لایه_شکل.path.set_items(شکل‌ها_جدید)

            لایه_شکل.update()

            psd_جدید.save(فایل_خروجی)

        with PsdImage.load(فایل_خروجی) as تصویر:
            تصویر = cast(PsdImage, تصویر)
            assert len(تصویر.layers) == 2

            لایه_شکل = cast(ShapeLayer, تصویر.layers[1])
            پر_داخلی = لایه_شکل.fill
            تنظیمات_خط = لایه_شکل.stroke
            پر_خط = لایه_شکل.stroke.fill

            assert len(لایه_شکل.path.get_items()) == 1
            assert len(لایه_شکل.path.get_items()[0].get_items()) == 3

            assert پر_داخلی.color.to_argb() == -16127182

            assert تنظیمات_خط.size == 7.41
            assert not تنظیمات_خط.enabled
            assert تنظیمات_خط.line_alignment == StrokePosition.CENTER
            assert تنظیمات_خط.line_cap == LineCapType.BUTT_CAP
            assert تنظیمات_خط.line_join == LineJoinType.MITER_JOIN
            assert پر_خط.color.to_argb() == -16777216
			
    def تولید_شکل_جدید(اندازه_تصویر):
        شکل_جدید = PathShape()

        نقطه1 = PointF(20, 100)
        نقطه2 = PointF(200, 100)
        نقطه3 = PointF(300, 10)

        گره1 = BezierKnotRecord()
        گره1.is_linked = True
        گره1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(نقطه1, اندازه_تصویر),
                    Release_24_04_Tests.PointFToResourcePoint(نقطه1, اندازه_تصویر),
                    Release_24_04_Tests.PointFToResourcePoint(نقطه1, اندازه_تصویر)
                ]

        گره2 = BezierKnotRecord()
        گره2.is_linked = True
        گره2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(نقطه2, اندازه_تصویر),
                    Release_24_04_Tests.PointFToResourcePoint(نقطه2, اندازه_تصویر),
                    Release_24_04_Tests.PointFToResourcePoint(نقطه2, اندازه_تصویر)
                ]

        گره3 = BezierKnotRecord()
        گره3.is_linked = True
        گره3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(نقطه3, اندازه_تصویر),
                    Release_24_04_Tests.PointFToResourcePoint(نقطه3, اندازه_تصویر),
                    Release_24_04_Tests.PointFToResourcePoint(نقطه3, اندازه_تصویر)
                ]

        گره‌های_بزرگ = [
            گره1,
            گره2,
            گره3
        ]

        شکل_جدید.set_items(گره‌های_بزرگ)

        return شکل_جدید
		
    def PointFToResourcePoint(نقطه, اندازه_تصویر):
        نسبت_تصویر_به_Psd = 256 * 65535
        return Point(
            int(round(نقطه.y * (نسبت_تصویر_به_Psd / اندازه_تصویر.height))),
            int(round(نقطه.x * (نسبت_تصویر_به_Psd / اندازه_تصویر.width)))
        )

    def assert_are_equal(مقدار_مورد_انتظار, مقدار_واقعی, پیام=None):
        if مقدار_مورد_انتظار != مقدار_واقعی:
            raise Exception(پیام or "شی‌ها برابر نیستند.")
			
{{< /highlight >}}

**PSDPYTHON-52. رفع مشکل تبدیل فایل Psd از RGB به CMYK**

{{< highlight python >}}
     def چک_تبدیل_از_Rgb_به_Cmyk():
        فایل_منبع = "frog_nosymb.psd"
        فایل_خروجی = "frog_nosymb_output.psd"

        with PsdImage.load(فایل_منبع) as تصویر:
            تصویر_psd = cast(PsdImage, تصویر)
            تصویر_psd.has_transparency_data = False

            گزینه‌های_psd = PsdOptions(تصویر_psd)
            گزینه‌های_psd.color_mode = ColorModes.CMYK
            گزینه‌ها.psd.compression_method = CompressionMethod.RLE
            گزینه‌ها.psd.channels_count = 4

            تصویر_psd.save(فایل_خروجی, گزینه‌ها_psd)

        with PsdImage.load(فایل_خروجی) as تصویر:
            تصویر_psd = cast(PsdImage, تصویر)
            assert not تصویر_psd.has_transparency_data
            assert تصویر_psd.layers[0].channels_count == 4

        def assert_are_equal(مقدار_مورد_انتظار, مقدار_واقعی, پیام=None):
            if مقدار_مورد_انتظار != مقدار_واقعی:
                raise Exception(پیام or "شی‌ها برابر نیستند.")			

    def assert_are_equal(مقدار_مورد_انتظار, مقدار_واقعی, پیام=None):
        if مقدار_مورد_انتظار != مقدار_واقعی:
            raise Exception(پیام or "شی‌ها برابر نیستند.")
				
{{< /highlight >}}

**PSDPYTHON-53. عدم امکان صادر کردن فایل خاص PSD با استفاده از Aspose.PSD**

{{< highlight python >}}
        فایل_منبع = "1966source.psd"
        خروجی_Png = "خروجی.png"

        گزینه‌های_بارگذاری = PsdLoadOptions()
        گزینه‌های_بارگذاری.load_effects_resource = True

        with PsdImage.load(فایل_منبع, گزینه‌های_بارگذاری) as تصویر_psd:
            تصویر_psd.save(خروجی_Png, PngOptions())
			
{{< /highlight >}}
