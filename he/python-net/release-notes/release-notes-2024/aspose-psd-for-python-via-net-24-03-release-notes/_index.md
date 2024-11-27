---
title: Aspose.PSD עבור Python via .NET 24.3 - הערות לגרסה
type: docs
weight: 10
url: /he/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את ההערות לגרסה של [Aspose.PSD עבור Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **מפתח**     | **סיכום**                                                          | **קטגוריה**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [פורמט AI] הפחתת זמן טעינה של תמונות AI מרובות עמודים גדולות         | שדרוג      |
| PSDPYTHON-45 | קובץ PSD לא נקרא לאחר המרת 8 ביט ל-16 ביט                   |     באג     |
| PSDPYTHON-46 | קובץ PSD לא נקרא לאחר המרת 8 ביט ל-32 ביט                   |     באג     |
| PSDPYTHON-47 | [פורמט AI] תיקון לעיבוד קו קצר בקובץ AI                         |     באג     |



## **שינויים ב-API הציבוריים**
# **APIs שנתרמו:**
- אין

# **APIs שהוסרו:**
- אין


## **דוגמאות שימוש:**

**PSDPYTHON-42. [פורמט AI] הפחתת זמן טעינה של תמונות AI מרובות עמודים גדולות**

{{< highlight python >}}
   # אין דוגמה
{{< /highlight >}}

**PSDPYTHON-45. קובץ PSD לא נקרא לאחר המרת 8 ביט ל-16 ביט**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # הכל בסדר
                pass
            else:
                raise Exception("משאב גלובלי שגוי, המשאב הראשון צריך להיות Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. קובץ PSD לא נקרא לאחר המרת 8 ביט ל-32 ביט**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # הכל בסדר
                pass
            else:
                raise Exception("משאב גלובלי שגוי, המשאב הראשון צריך להיות Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [פורמט AI] תיקון לעיבוד קו קצר בקובץ AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
