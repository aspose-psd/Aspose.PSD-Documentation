---
title: فرارسیدنی‌های نسخه Aspose.PSD برای پایتون از طریق .NET 24.2
type: docs
weight: 10
url: /fa/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل فرارسید‌های نسخه [Aspose.PSD for Python via .NET 24.2](https://pypi.org/project/aspose-psd/) می‌باشد.

{{% /alert %}}

| **کلید**     | **خلاصه**                                                                  | **دسته** |
|:-----------|:------------------------------------------------------------|:--------|
| PSDPYTHON-28 | رسیدگی به ویژگی Angle برای تنظیمات پر کردن الگو                         |   ویژگی   |
| PSDPYTHON-29 | پشتیبانی از مقیاس عمودی و افقی برای لایه متن                     |   ویژگی   |
| PSDPYTHON-33 | [قالب AI] پیاده‌سازی صحیح تصویر پس‌زمینه در قالب مبتنی بر PDF AI  |   ویژگی   |
| PSDPYTHON-34 | تغییر مکانیزم Distort در warp                                           | بهبود    |
| PSDPYTHON-35 | افزایش سرعت warp                                                          | بهبود    |
| PSDPYTHON-36 | استثناء "بارگذاری تصویر ناموفق" هنگام باز کردن سند                 |   باگ    |
| PSDPYTHON-37 | رفع مشکل ذخیره‌سازی فایل‌های psd دارای الگوی Stroke                |   باگ    |
| PSDPYTHON-38 | استایل متن اشتباه در یک شیوه هوشمند زمانی که از ReplaceContents استفاده می‌کنیم |   باگ    |
| PSDPYTHON-39 | [قالب AI] رفع اشکال رندرینگ Cubic Bezier در فایل AI              |   باگ    |



## **تغییرات API های عمومی**
# **APIهای اضافه شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIهای حذف شده:**
- هیچ

## **مثال‌های استفاده:**

## **مثال‌های استفاده:**

**PSDPYTHON-28. رسیدگی به ویژگی Angle برای تنظیمات پر کردن الگو**

{{< highlight python >}}

    نام_پرونده = "PatternFillLayerWide_0"
    پرونده_منبع = نام_پرونده + ".psd"
    پرونده_خروجی = نام_پرونده + "_output.psd"

    گزینه_بارگذاری = گزینه‌های_بارگذاری_Psd()
    گزینه_بارگذاری.load_effects_resource = True
    with تصویر_Psd.load(پرونده_منبع, گزینه_بارگذاری) as img:
        تصویر = cast(تصویر_Psd, img)
        لایه_پر = cast(لایه_پر, تصویر.layers[1])
        تنظیمات_پر = لایه_پر.fill_settings
        تنظیمات_پر.angle = 70
        لایه_پر.update()
        تصویر.save(پرونده_خروجی, گزینه‌های_Psd())

    with تصویر_Psd.load(پرونده_خروجی, گزینه_بارگذاری) as img:
        تصویر = cast(تصویر_Psd, img)
        لایه_پر = cast(لایه_پر, تصویر.layers[1])
        تنظیمات_پر = لایه_پر.fill_settings

        assert تنظیمات_پر.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. پشتیبانی از مقیاس عمودی و افقی برای لایه متن**

{{< highlight python >}}

       پرونده_منبع = "1719_src.psd"
       پرونده_خروجی = "output.png"

       # اضافه کردن چند فونت
       پوشه_فونتها = "1719_Fonts"
       پوشه_فونتها = list(FontSettings.get_fonts_folders())
       پوشه_فونتها.append(پوشه_فونتها)
       FontSettings.set_fonts_folders(پوشه_فونتها, True)

       with تصویر_Psd.load(پرونده_منبع) as تصویر:
           تصویر.save(پرونده_خروجی, گزینه‌های_Png())

{{< /highlight >}}

**PSDPYTHON-33. [قالب AI] پیاده‌سازی صحیح تصویر پس‌زمینه در قالب مبتنی بر PDF AI**

{{< highlight python >}}

       پرونده_منبع = "pineapples.ai"
       پرونده_خروجی = "pineapples.png"

       with تصویر_Ai.load(پرونده_منبع) as تصویر:
           تصویر.save(پرونده_خروجی, گزینه‌های_Png())

{{< /highlight >}}

**PSDPYTHON-34. تغییر مکانیزم Distort در warp**

{{< highlight python >}}

       پرونده_منبع = "crow_grid.psd"       
       پرونده_خروجی = self.GetFileInOutputFolder("export.png")

       گزینه = گزینه‌های_بارگذاری_Psd()
       گزینه.load_effects_resource = True
       گزینه.allow_warp_repaint = True

       گزینه‌های_Png = گزینه‌های_Png()
       گزینه‌های_Png.compression_level = 9
       گزینه‌های_Png.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
       with تصویر_Psd.load(پرونده_منبع, گزینه) as img:
           img.save(پرونده_خروجی, گزینه‌های_Png)

{{< /highlight >}}

**PSDPYTHON-35. افزایش سرعت warp**

{{< highlight python >}}

       پرونده_منبع = "output.psd"
       پرونده_خروجی = "export.png"

       گزینه = گزینه‌های_بارگذاری_Psd()
       گزینه.load_effects_resource = True
       گزینه.allow_warp_repaint = True

       زمان_شروع = زمان.time()

       گزینه‌های_Png = گزینه‌های_Png()
       گزینه‌های_Png.compression_level = 9
       گزینه‌های_Png.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

       with تصویر_Psd.load(پرونده_منبع, گزینه) as img:
           img.save(پرونده_خروجی, گزینه‌های_Png)

       زمان_گذشته = زمان.time() - زمان_شروع

       # مقدار قدیمی = 193300
       # مقدار جدید =  55500
       زمان_به_ثانیه = int(زمان_گذشته * 1000)
       if زمان_به_ثانیه > 100000:
           raise استثناء("زمان پردازش بیش از حد طولانی است")

{{< /highlight >}}

**PSDPYTHON-36. استثناء "بارگذاری تصویر ناموفق" هنگام باز کردن سند**

{{< highlight python >}}
       پرونده_منبع1 = "PRODUCT.ai"
       پرونده_خروجی1 = "PRODUCT.png"

       with تصویر_Ai.load(پرونده_منبع1) as تصویر:
           تصویر.save(پرونده_خروجی1, گزینه‌های_Png())

       پرونده_منبع2 = "Dolota.ai"
       پرونده_خروجی2 = "Dolota.png"

       with تصویر_Ai.load(پرونده_منبع2) as تصویر:
           تصویر.save(پرونده_خروجی2, گزینه‌های_Png())       
        
       پرونده_منبع3 = "ARS_novelty_2108_out_01(1).ai"
       پرونده_خروجی3 = "ARS_novelty_2108_out_01(1).png"

       with تصویر_Ai.load(پرونده_منبع3) as تصویر:
           تصویر.save(پرونده_خروجی3, گزینه‌های_Png())

       پرونده_منبع4 = "bit_gear.ai"      
       پرونده_خروجی4 = "bit_gear.png"

       with تصویر_Ai.load(پرونده_منبع4) as تصویر:
           تصویر.save(پرونده_خروجی4, گزینه‌های_Png())

       پرونده_منبع5 = "test.ai"
       پرونده_خروجی5 = "test.png"

       with تصویر_Ai.load(پرونده_منبع5) as تصویر:
           تصویر.save(پرونده_خروجی5, گزینه‌های_Png())
{{< /highlight >}}

**PSDPYTHON-37. رفع مشکل ذخیره‌سازی فایل‌های psd با الگوی Stroke**

{{< highlight python >}}
	    پرونده_منبع = "StrokeShapePattern.psd"
        پرونده_خروجی = "StrokeShapePattern_output.psd"

        مرز_الگو_جدید = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        نام_الگو_جدید = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        الگو_جدید = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with تصویر_Psd.load(پرونده) as img:
            تصویر = cast(تصویر_Psd, img)
            لایه_شکل = cast(لایه_شکل, تصویر.layers[1])
            تنظیمات_پر_داخلی__فیل = لایه_شکل.fill

            pattResource = None
            for کلید رویت‌لایه in تصویر.global_layer_resources:
                pattResource = as_of(کلید رویت‌لایه, PattResource)
                if pattResource is not None:
                    patternItem = pattResource.patterns[0]  # اطلاعات الگوی داخلی Stroke
                    patternItem.pattern_id = guid
                    patternItem.name = نام_الگو_جدید
                    patternItem.set_pattern(الگو_جدید, مرز_الگو_جدید)
                    break

            تنظیمات_پر_داخلی__فیل.pattern_name = نام_الگو_جدید
            تنظیمات_پر_داخلی__فیل.pattern_id = guid + "\0"

            لایه_شکل.update()

            تصویر.save(پرونده_خروجی)

        # بررسی داده‌های تغییر‌یافته.
        with تصویر_Psd.load(پرونده_خروجی) as img:
            تصویر = cast(تصویر_Psd, img)
            لایه_شکل = cast(لایه_شکل, تصویر.layers[1])
            تنظیمات_پر_داخلی__فیل = لایه_شکل.fill

            assert guid.upper() == تنظیمات_پر_داخلی__فیل.pattern_id
            assert نام_الگو_جدید == تنظیمات_پر_داخلی__فیل.pattern_name + "\0"
{{< /highlight >}}

**PSDPYTHON-38. استایل متن اشتباه در یک شیوه هوشمند زمانی که از ReplaceContents استفاده می‌کنیم**

{{< highlight python >}}
        فایل_ورودی = "source.psd"
        خروجی2 = "output.png"

        گزینه‌های_بارگذاری_Psd = گزینه‌های_بارگذاری_Psd()
        گزینه‌های_بارگذاری_Psd.load_effects_resource = True

        with تصویر_Psd.load(فایل_ورودی, گزینه‌های_بارگذاری_Psd) as image:
            تصویر_Psd = cast(تصویر_Psd, image)
            لایه_شیوه_هوشمند = cast(لایه_شیوه_هوشمند, تصویر_Psd.layers[1])

            تصویر_شیوه_هوشمند = cast(تصویر_Psd, لایه_شیوه_هوشمند.load_contents(گزینه‌های_بارگذاری_Psd))

            with تصویر_شیوه_هوشمند:
                لایه_شیوه_هوشمند.replace_contents(تصویر_شیوه_هوشمند)

            گزینه_پی‌ان‌جی = گزینه‌های_Png()
            گزینه_پی‌ان‌جی.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            تصویر_Psd.save(خروجی2, گزینه_پی‌ان‌جی)

{{< /highlight >}}

**PSDPYTHON-39. [قالب AI] رفع اشکال رندرینگ Cubic Bezier در فایل AI**

{{< highlight python >}}

        پرونده_منبع = "Typography.ai"
        مسیر_خروجی = "Typography.png"

        with تصویر_Ai.load(پرونده_منبع) as تصویر:
            تصویر.save(مسیر_خروجی, گزینه‌های_Png())

{{< /highlight >}}
