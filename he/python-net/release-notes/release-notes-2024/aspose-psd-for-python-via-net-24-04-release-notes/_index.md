---
title: Aspose.PSD עבור Python via .NET 24.4 - הערות לגרסה
type: docs
weight: 10
url: /he/python-net/aspose-psd-for-python-via-net-24-4-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הערות לגרסה עבור [Aspose.PSD עבור Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **מפתח**     | **סיכום**                                                          | **קטגוריה**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [פורמט AI] הוספת טיפול במשאב XObjectForm                        | תכונה     |
| PSDPYTHON-51 | הוספת בונה עבור השכבת צורה                                   | תכונה     |
| PSDPYTHON-52 | תיקון המרה של קובץ Psd מ-RGB ל-CMYK                          | באג         |
| PSDPYTHON-53 | לא ניתן לייצא קובץ PSD מסוים באמצעות Aspose.PSD               | באג         |



## **שינויים ב-API הציבורי**
# **APIs החדשים:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **APIs ההוסרו:**
- ללא


## **דוגמאות שימוש:**

**PSDPYTHON-50. [פורמט AI] הוספת טיפול במשאב XObjectForm**

{{< highlight python >}}
        שם_קובץ_מקור = "דוגמה.ai"
        נתיב_פלט = "פלט_דוגמה.png"

        with AiImage.load(שם_קובץ_מקור) as תמונה:
            תמונה.save(נתיב_פלט, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. הוספת בונה עבור השכבת צורה**

{{< highlight python >}}
     def בדוק ShapeLayerConstructor():
        קובץ_פלט = "פלט_הוספת_שכבת_צורה.psd"

        with PsdImage(600, 400) as psd_חדש:
            shapeLayer = psd_חדש.add_shape_layer()

            צורה_חדשה = generate_new_shape(psd_חדש.size)
            צורות_חדשות = [צורה_חדשה]
            shapeLayer.path.set_items(צורות_חדשות)

            shapeLayer.update()

            psd_חדש.save(קובץ_פלט)

        with PsdImage.load(קובץ_פלט) as img:
            תמונה = cast(PsdImage, img)
            assert len(תמונה.layers) == 2

            shapeLayer = cast(ShapeLayer, תמונה.layers[1])
            internalFill = shapeLayer.fill
            strokeSettings = shapeLayer.stroke
            strokeFill = shapeLayer.stroke.fill

            assert len(shapeLayer.path.get_items()) == 1
            assert len(shapeLayer.path.get_items()[0].get_items()) == 3

            assert internalFill.color.to_argb() == -16127182

            assert strokeSettings.size == 7.41
            assert not strokeSettings.enabled
            assert strokeSettings.line_alignment == StrokePosition.CENTER
            assert strokeSettings.line_cap == LineCapType.BUTT_CAP
            assert strokeSettings.line_join == LineJoinType.MITER_JOIN
            assert strokeFill.color.to_argb() == -16777216
			
    def generate_new_shape(גודל_תמונה):
        צורה_חדשה = PathShape()

        נקודה1 = PointF(20, 100)
        נקודה2 = PointF(200, 100)
        נקודה3 = PointF(300, 10)

        קשיש1 = BezierKnotRecord()
        קשיש1.is_linked = True
        קשיש1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(נקודה1, גודל_תמונה),
                    Release_24_04_Tests.PointFToResourcePoint(נקודה1, גודל_תמונה),
                    Release_24_04_Tests.PointFToResourcePoint(נקודה1, גודל_תמונה)
                ]

        קשיש2 = BezierKnotRecord()
        קשיש2.is_linked = True
        קשיש2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(נקודה2, גודל_תמונה),
                    Release_24_04_Tests.PointFToResourcePoint(נקודה2, גודל_תמונה),
                    Release_24_04_Tests.PointFToResourcePoint(נקודה2, גודל_תמונה)
                ]

        קשיש3 = BezierKnotRecord()
        קשיש3.is_linked = True
        קשיש3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(נקודה3, גודל_תמונה),
                    Release_24_04_Tests.PointFToResourcePoint(נקודה3, גודל_תמונה),
                    Release_24_04_Tests.PointFToResourcePoint(נקודה3, גודל_תמונה)
                ]

        קשישי_בזיר = [
            קשיש1,
            קשיש2,
            קשיש3
        ]

        צורה_חדשה.set_items(קשישי_בזיר)

        return צורה_חדשה
		
    def PointFToResourcePoint(נקודה, גודל_תמונה):
        ImgToPsdRatio = 256 * 65535
        return Point(
            int(round(נקודה.y * (ImgToPsdRatio / גודל_תמונה.height))),
            int(round(נקודה.x * (ImgToPsdRatio / גודל_תמונה.width)))
        )

    def assert_are_equal(צפוי, בפועל, הודעה=None):
        if צפוי != בפועל:
            raise Exception(הודעה or "האובייקטים אינם שווים.")
			
{{< /highlight >}}

**PSDPYTHON-52. תיקון המרה של קובץ Psd מ-RGB ל-CMYK**

{{< highlight python >}}
     def בדוקConversionFromRgbToCmyk():
        קובץ_מקור = "frog_nosymb.psd"
        קובץ_פלט = "frog_nosymb_output.psd"

        with PsdImage.load(קובץ_מקור) as תמונה:
            תמונת_psd = cast(PsdImage, תמונה)
            תמונת_psd.has_transparency_data = False

            אפשרויות_psd = PsdOptions(תמונת_psd)
            אפשרויות_psd.color_mode = ColorModes.CMYK
            אפשרויות_psd.compression_method = CompressionMethod.RLE
            אפשרויות_psd.channels_count = 4

            תמונת_psd.save(קובץ_פלט, אפשרויות_psd)

        with PsdImage.load(קובץ_פלט) as תמונה:
            תמונת_psd = cast(PsdImage, תמונה)
            assert not תמונת_psd.has_transparency_data
            assert תמונת_psd.layers[0].channels_count == 4

        def assert_are_equal(צפוי, בפועל, הודעה=None):
            if צפוי != בפועל:
                raise Exception(הודעה or "האובייקטים אינם שווים.")			

    def assert_are_equal(צפוי, בפועל, הודעה=None):
        if צפוי != בפועל:
            raise Exception(הודעה or "האובייקטים אינם שווים.")
				
{{< /highlight >}}

**PSDPYTHON-53. לא ניתן לייצא קובץ PSD מסוים באמצעות Aspose.PSD**

{{< highlight python >}}
        שם_קובץ = "1966source.psd"
        פלט_PNG = "פלט.png"

        אפשרויות_טעינה = PsdLoadOptions()
        אפשרויות_טעינה.load_effects_resource = True

        with PsdImage.load(שם_קובץ, אפשרויות_טעינה) as תמונת_psd:
            תמונת_psd.save(פלט_PNG, PngOptions())
			
{{< /highlight >}}
