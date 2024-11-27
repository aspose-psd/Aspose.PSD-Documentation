---
title: تنزيلات أسبوز.بي.إس.دي للبايثون عبر .نت 24.2 - ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD for Python via .NET 24.2](https://pypi.org/project/aspose-psd/).

{{% /alert %}}

| **المفتاح** | **الملخص** | **التصنيف** |
|:-------------|:------------|:------------|
| PSDPYTHON-28 | معالجة خاصية Angle لإعدادات PatternFillSettings | ميزة |
| PSDPYTHON-29 | دعم التحجيم العمودي والأفقي لطبقة النص | ميزة |
| PSDPYTHON-33 | تنفيذ عرض سليم للخلفية في تنسيق AI القائم على PDF | ميزة |
| PSDPYTHON-34 | تغيير آلية الانحراف في الانحناء | تحسين |
| PSDPYTHON-35 | تسريع الانحناء | تحسين |
| PSDPYTHON-36 | استثناء "فشل تحميل الصورة." عند فتح المستند | خلل |
| PSDPYTHON-37 | إصلاح حفظ ملفات psd التي تحتوي على نمط Stroke | خلل |
| PSDPYTHON-38 | النمط النصي غير صحيح في كائن ذكي عند استخدام ReplaceContents | خلل |
| PSDPYTHON-39 | إصلاح عرض Cubic Bezier في ملف AI | خلل |



## **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المُضافة:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs المُزيلة:**
- لا شيء


## **أمثلة الاستخدام:**

**PSDPYTHON-28. معالجة خاصية Angle لإعدادات PatternFillSettings**

{{< highlight python >}}

        اسم_الملف = "PatternFillLayerWide_0"
        ملف_المصدر = اسم_الملف + ".psd"
        ملف_الإخراج = اسم_الملف + "_output.psd"

        خيارات_التحميل = PsdLoadOptions()
        خيارات_التحميل.load_effects_resource = True
        مع PsdImage.load(ملف_المصدر, خيارات_التحميل) as صورة:
            صورة = cast(PsdImage, صورة)
            طبقةالتعبئة = cast(FillLayer, صورة.layers[1])
            إعداداتالتعبئة = طبقةالتعبئة.fill_settings
            إعداداتالتعبئة.angle = 70
            طبقةالتعبئة.update()
            صورة.save(ملف_الإخراج, PsdOptions())

        مع PsdImage.load(ملف_الإخراج, خيارات_التحميل) as صورة:
            صورة = cast(PsdImage, صورة)
            طبقةالتعبئة = cast(FillLayer, صورة.layers[1])
            إعداداتالتعبئة = طبقةالتعبئة.fill_settings

            assert إعداداتالتعبئة.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. دعم التحجيم العمودي والأفقي لطبقة النص**

{{< highlight python >}}

            ملف_المصدر = "1719_src.psd"
            ملف_الإخراج = "output.png"

            مجلدات_الخطوط = "1719_Fonts"
            مجلدات_الخطوط = قائمة(FontSettings.get_fonts_folders())
            مجلدات_الخطوط.append(مجلدات_الخطوط)
            FontSettings.set_fonts_folders(مجلدات_الخطوط, True)

            with PsdImage.load(ملف_المصدر) as صورة:
                صورة.save(ملف_الإخراج, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. تنفيذ عرض سليم للخلفية في تنسيق AI القائم على PDF**

{{< highlight python >}}

           ملف_المصدر = "pineapples.ai"
           ملف_الإخراج = "pineapples.png"

           with AiImage.load(ملف_المصدر) as صورة:
               صورة.save(ملف_الإخراج, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. تغيير آلية الانحراف في الانحناء**

{{< highlight python >}}

        ملف_المصدر = "crow_grid.psd"       
        ملف_الإخراج = الحصول_على_ملف_في_المجلد_المخرج("export.png")

        خيارات = PsdLoadOptions()
        خيارات.load_effects_resource = True
        خيارات.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
        with PsdImage.load(ملف_المصدر, خيارات) as صورة:
            صورة.save(ملف_الإخراج, pngOpt)

{{< /highlight >}}

**PSDPYTHON-35. تسريع الانحناء**

{{< highlight python >}}

        ملف_المصدر = "output.psd"
        ملف_الإخراج = "export.png"

        خيارات = PsdLoadOptions()
        خيارات.load_effects_resource = True
        خيارات.allow_warp_repaint = True

        start_time = time.time()

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(ملف_المصدر, خيارات) as صورة:
            صورة.save(ملف_الإخراج, pngOpt)

        elapsed_time = time.time() - start_time

        # القيمة القديمة = 193300
        # القيمة الجديدة = 55500
        time_in_sec = int(elapsed_time * 1000)
        if time_in_sec > 100000:
            raise Exception("وقت المعالجة طويل جدًا")        
			
{{< /highlight >}}

**PSDPYTHON-36. استثناء "فشل تحميل الصورة." عند فتح المستند**

{{< highlight python >}}
        ملف_المصدر1 = "PRODUCT.ai"
        ملف_الإخراج1 = "PRODUCT.png"

        with AiImage.load(ملف_المصدر1) as صورة:
            صورة.save(ملف_الإخراج1, PngOptions())

        ملف_المصدر2 = "Dolota.ai"
        ملف_الإخراج2 = "Dolota.png"

        with AiImage.load(ملف_المصدر2) as صورة:
            صورة.save(ملف_الإخراج2, PngOptions())       

        ملف_المصدر3 = "ARS_novelty_2108_out_01(1).ai"
        ملف_الإخراج3 = "ARS_novelty_2108_out_01(1).png"

        with AiImage.load(ملف_المصدر3) as صورة:
            صورة.save(ملف_الإخراج3, PngOptions())

        ملف_المصدر4 = "bit_gear.ai"      
        ملف_الإخراج4 = "bit_gear.png"

        with AiImage.load(ملف_المصدر4) as صورة:
            صورة.save(ملف_الإخراج4, PngOptions())

        ملف_المصدر5 = "test.ai"
        ملف_الإخراج5 = "test.png"

        with AiImage.load(ملف_المصدر5) as صورة:
            صورة.save(ملف_الإخراج5, PngOptions())
{{< /highlight >}}

**PSDPYTHON-37. إصلاح حفظ ملفات PSD التي تحتوي على نمط Stroke**

{{< highlight python >}}
        ملف_المصدر = "StrokeShapePattern.psd"
        ملف_الإخراج = "StrokeShapePattern_output.psd"

        newPatternBounds = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        newPattern = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdImage.load(ملف_المصدر) as صورة:
            صورة = cast(PsdImage, صورة)
            طبقةالشكل = cast(ShapeLayer, صورة.layers[1])
            strokeInternalFillSettings = طبقةالشكل.fill

            pattResource = None
            for globalLayerResource in صورة.global_layer_resources:
                pattResource = as_of(globalLayerResource, PattResource)
                if pattResource is not None:
                    patternItem = pattResource.patterns[0]  
                    patternItem.pattern_id = guid
                    patternItem.name = newPatternName
                    patternItem.set_pattern(newPattern, newPatternBounds)
                    break

            strokeInternalFillSettings.pattern_name = newPatternName
            strokeInternalFillSettings.pattern_id = guid + "\0"

            طبقةالشكل.update()

            صورة.save(ملف_الإخراج)

        with PsdImage.load(ملف_الإخراج) as صورة:
            صورة = cast(PsdImage, صورة)
            طبقةالشكل = cast(ShapeLayer, صورة.layers[1])
            strokeInternalFillSettings = طبقةالشكل.fill

            assert guid.upper() == strokeInternalFillSettings.pattern_id
            assert newPatternName == strokeInternalFillSettings.pattern_name + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. النمط النصي غير صحيح في كائن ذكي عند استخدام ReplaceContents**

{{< highlight python >}}
        ملف_المدخل = "source.psd"
        الناتج2 = "output.png"

        خيارات_التحميل = PsdLoadOptions()
        خيارات_التحميل.load_effects_resource = True

        with PsdImage.load(ملف_المدخل, خيارات_التحميل) as صورة:
            صورةPSD = cast(PsdImage, صورة)
            كائن_ذكي = cast(SmartObjectLayer, صورةPSD.layers[1])

            صورةكائن_ذكي = cast(PsdImage, كائن_ذكي.load_contents(خيارات_التحميل))

            مع صورةكائن_ذكي:
                كائن_ذكي.replace_contents(صورةكائن_ذكي)

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            صورةPSD.save(الناتج2, pngOpt)

{{< /highlight >}}

**PSDPYTHON-39. إصلاح عرض Cubic Bezier في ملف AI**

{{< highlight python >}}
        ملف_المصدر = "Typography.ai"
        مسار_الإخراج = "Typography.png"

        with AiImage.load(ملف_المصدر) as صورة:
            صورة.save(مسار_الإخراج, PngOptions())

{{< /highlight >}}