---
title: أسبوز.بي.إس.دي لـ .نت 21.12 - ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-psd-for-net-21-12-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [أسبوز.بي.إس.دي لـ .نت 21.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-997|إضافة القدرة على تحديد الخطوط برمجيًا|ميزة|
|PSDNET-785|Aspose.PSD 20.10: فشل في تحميل PSD|خلل|
|PSDNET-812|استثناء ImageLoad عند تحميل PSD|خلل|
|PSDNET-870|استثناء ImageLoad عند تحميل طبقة PSD ذات طريقة ضغط غير مدعومة|خلل|
|PSDNET-918|Aspose.PSD 21.6: طريقة الضغط غير مدعومة لملف PSD|خلل|
|PSDNET-984|حفظ غير صحيح لمسار الفيكتور مع قناع|خلل|
|PSDNET-1001|خط غير صحيح في TextPortion في ملف محدد|خلل|
|PSDNET-1031|استثناء عدم دعم طريقة الضغط عند تحميل الصورة|خلل|
|PSDNET-1033|مؤشر خارج النطاق عند الحفظ في الملف المحدد|خلل|
|PSDNET-1036|إضافة دعم لـ PathStructure لتجنب خطأ تحميل الملف|خلل|

## **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المُضافة:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Prefix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.StructureKey
- M:Aspose.PSD.FontSettings.SetAllowedFonts(System.String[])
- M:Aspose.PSD.FontSettings.IsFontAllowed(System.String)
- M:Aspose.PSD.FontSettings.GetReplacementFont(System.String)
- M:Aspose.PSD.FontSettings.GetFontReplacements(System.String)
- M:Aspose.PSD.FontSettings.SetFontReplacements(System.String,System.String[])
- M:Aspose.PSD.FontSettings.ClearFontReplacements

# **APIs المحذوفة:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDNET-785. Aspose.PSD 20.10: فشل في تحميل PSD**

{{< highlight csharp >}}
            string src = "ShimadzuLetterhead100.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src, new PsdLoadOptions() { ReadOnlyMode = true }))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-812. استثناء ImageLoad عند تحميل PSD**

{{< highlight csharp >}}
            string src = "5-MX10600_Amazon_DEVICES_2_1000x1000.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-870. استثناء ImageLoad عند تحميل طبقة PSD ذات طريقة ضغط غير مدعومة**

{{< highlight csharp >}}
            string srcFile = "sourceFile.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-918. Aspose.PSD 21.6: طريقة الضغط غير مدعومة لملف PSD**

{{< highlight csharp >}}
            string srcFile = "Fb-blue-jury (1).psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-984. حفظ غير صحيح لمسار الفيكتور مع قناع**

{{< highlight csharp >}}
            string srcFile = "PsdConvertToPngExample.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                psdImage.Save(
                    outputFilePng,
                    new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha, Progressive = true, CompressionLevel = 9 });
            }
{{< /highlight >}}

**PSDNET-997. إضافة القدرة على تحديد الخطوط برمجيًا**

{{< highlight csharp >}}
            string srcFile = "fonts_com_updated.psd";
            string output = "etalon_fonts_com_updated.psd.png";

            try
            {
                var fontList = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                FontSettings.SetAllowedFonts(fontList);

                var myriadReplacement = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                var calibriReplacement = new string[] { "Webdings", "Courier New", "Bookman Old Style" };
                var arialReplacement = new string[] { "Bookman Old Style", "Courier New", "Webdings" };
                var timesReplacement = new string[] { "Arial", "NotExistedFont", "Courier New" };

                FontSettings.SetFontReplacements("MyriadPro-Regular", myriadReplacement);
                FontSettings.SetFontReplacements("Calibri", calibriReplacement);
                FontSettings.SetFontReplacements("Arial", arialReplacement);
                FontSettings.SetFontReplacements("Times New Roman", timesReplacement);

                using (PsdImage image = (PsdImage)Image.Load(srcFile))
                {
                    image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            } 
            finally
            {
                FontSettings.SetAllowedFonts(null);
                FontSettings.ClearFontReplacements();
            }
{{< /highlight >}}

**PSDNET-1001. خط غير صحيح في TextPortion في ملف محدد**

{{< highlight csharp >}}
            string srcFile = "fonts_com.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                var tl = (TextLayer)image.Layers[1];
                var fontName = tl.TextData.Items[0].Style.FontName;
                if (fontName != "MyriadPro-Regular")
                {
                    throw new Exception("Incorrect font");
                }

                // يجب علينا الحصول على Myriad Pro، لكن نلاحظ AdobeInvisFont
                image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-1031. استثناء عدم دعم طريقة الضغط عند تحميل الصورة**

{{< highlight csharp >}}
            string srcFile = "shirt-error.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-1033.  مؤشر خارج النطاق عند الحفظ في الملف المحدد**

{{< highlight csharp >}}
            string srcFile = "237708.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1036. إضافة دعم لـ PathStructure لتجنب خطأ تحميل الملف**

{{< highlight csharp >}}
            string srcFile = "shirt-color.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}