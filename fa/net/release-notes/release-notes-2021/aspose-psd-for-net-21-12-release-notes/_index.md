---
title: Aspose.PSD برای .NET 21.12 - یادداشت‌های انتشار
type: docs
weight: 10
url: /fa/net/aspose-psd-for-net-21-12-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای .NET 21.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-997|افزودن قابلیت محدود کردن فونت‌ها به صورت برنامه‌ریزی شده|ویژگی|
|PSDNET-785|Aspose.PSD 20.10: شکست در بارگذاری PSD|اشکال|
|PSDNET-812|خطای بارگذاری تصویر در هنگام بارگذاری PSD|اشکال|
|PSDNET-870|خطای بارگذاری تصویر در لایه PSD با CompressionMethod پشتیبانی نشده|اشکال|
|PSDNET-918|Aspose.PSD 21.6: روش فشرده‌سازی برای یک فایل PSD پشتیبانی نمی‌شود|اشکال|
|PSDNET-984|ذخیره‌سازی نادرست مسیر برداری با ماسک|اشکال|
|PSDNET-1001|فونت نادرست در TextPortion در یک فایل خاص|اشکال|
|PSDNET-1031|خطای CompressionMethod پشتیبانی نشده در بارگذاری تصویر|اشکال|
|PSDNET-1033|اندازه آرایه خارج از محدوده در ذخیره‌سازی در فایل خاص|اشکال|
|PSDNET-1036|افزودن پشتیبانی از PathStructure برای جلوگیری از خطا در بارگذاری فایل|اشکال|

## **تغییرات API عمومی**
# **API های افزوده شده:**
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

# **API های حذف شده:**
- هیچکدام

## **مثال های استفاده:**

**PSDNET-785. Aspose.PSD 20.10: شکست در بارگذاری PSD**

{{< highlight csharp >}}
            string src = "ShimadzuLetterhead100.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src, new PsdLoadOptions() { ReadOnlyMode = true }))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-812. خطای بارگذاری تصویر در هنگام بارگذاری PSD**

{{< highlight csharp >}}
            string src = "5-MX10600_Amazon_DEVICES_2_1000x1000.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-870. خطای بارگذاری تصویر در لایه PSD با CompressionMethod پشتیبانی نشده**

{{< highlight csharp >}}
            string srcFile = "sourceFile.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-918. Aspose.PSD 21.6: روش فشرده‌سازی برای یک فایل PSD پشتیبانی نمی‌شود**

{{< highlight csharp >}}
            string srcFile = "Fb-blue-jury (1).psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-984. ذخیره‌سازی نادرست مسیر برداری با ماسک**

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

**PSDNET-997. افزودن قابلیت محدود کردن فونت‌ها به صورت برنامه‌ریزی شده**

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

**PSDNET-1001. فونت نادرست در TextPortion در یک فایل خاص**

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

                // باید Myriad Pro را بگیریم، اما در واقع AdobeInvisFont را می‌بینیم
                image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-1031. خطای CompressionMethod پشتیبانی نشده در بارگذاری تصویر**

{{< highlight csharp >}}
            string srcFile = "shirt-error.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-1033.  Index out of range on the saving in the specific file**

{{< highlight csharp >}}
            string srcFile = "237708.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1036. Add support of PathStructure to avoid the load file error**

{{< highlight csharp >}}
            string srcFile = "shirt-color.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}
