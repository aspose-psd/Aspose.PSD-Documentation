---
title: Aspose.PSD for .NET 21.12 - บันทึกการเผยแพร่
type: docs
weight: 10
url: /th/net/aspose-psd-for-net-21-12-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการเผยแพร่สำหรับ [Aspose.PSD for .NET 21.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-997|เพิ่มความสามารถในการจำกัดแบบโปรแกรมของแบบอักษร|คุณลักษณะ|
|PSDNET-785|Aspose.PSD 20.10: ล้มเหลวในการโหลด PSD|ข้อบกพร่อง|
|PSDNET-812|ข้อยกเว้นการโหลดภาพขณะโหลด PSD|ข้อบกพร่อง|
|PSDNET-870|ข้อยกเว้นการโหลดภาพขณะโหลดเลเยอร์ PSD ที่มีวิธีการบีบอัดที่ไม่รองรับ|ข้อบกพร่อง|
|PSDNET-918|Aspose.PSD 21.6: วิธีการบีบอัดไม่รองรับสำหรับไฟล์ PSD|ข้อบกพร่อง|
|PSDNET-984|การบันทึกเส้นทางเวกเตอร์ผิดพลาดกับโมฆะ|ข้อบกพร่อง|
|PSDNET-1001|ฟอนต์ไม่ถูกต้องในส่วนข้อความในไฟล์ที่ระบุ|ข้อบกพร่อง|
|PSDNET-1031|ข้อยกเว้นไม่รองรับวิธีการบีบอัดในการโหลดภาพ|ข้อบกพร่อง|
|PSDNET-1033|ตำแหน่งเกินขอบเขตในการบันทึกในไฟล์ที่ระบุ|ข้อบกพร่อง|
|PSDNET-1036|เพิ่มการสนับสนุนของ PathStructure เพื่อหลีกเลี่ยงข้อผิดพลาดในการโหลดไฟล์|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา**
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

# **API ที่ถูกลบออก**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-785. Aspose.PSD 20.10: ล้มเหลวในการโหลด PSD**

{{< highlight csharp >}}
            string src = "ShimadzuLetterhead100.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src, new PsdLoadOptions() { ReadOnlyMode = true }))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-812. ข้อยกเว้นการโหลดภาพขณะโหลด PSD**

{{< highlight csharp >}}
            string src = "5-MX10600_Amazon_DEVICES_2_1000x1000.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-870. ข้อยกเว้นการโหลดภาพขณะโหลดเลเยอร์ PSD ที่มีวิธีการบีบอัดที่ไม่รองรับ**

{{< highlight csharp >}}
            string srcFile = "sourceFile.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-918. Aspose.PSD 21.6: วิธีการบีบอัดไม่รองรับสำหรับไฟล์ PSD**

{{< highlight csharp >}}
            string srcFile = "Fb-blue-jury (1).psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-984. การบันทึกเส้นทางเวกเตอร์ผิดพลาดกับโมฆะ**

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

**PSDNET-997.  เพิ่มความสามารถในการจำกัดแบบโปรแกรมของแบบอักษร**

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

**PSDNET-1001. ฟอนต์ไม่ถูกต้องในส่วนข้อความในไฟล์ที่ระบุ**

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

                // เราควรได้รับ Myriad Pro, แต่เราเห็น AdobeInvisFont
                image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-1031. ข้อยกเว้นไม่รองรับวิธีการบีบอัดในการโหลดภาพ**

{{< highlight csharp >}}
            string srcFile = "shirt-error.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-1033. ตำแหน่งเกินขอบเขตในการบันทึกในไฟล์ที่ระบุ**

{{< highlight csharp >}}
            string srcFile = "237708.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1036. เพิ่มการสนับสนุนของ PathStructure เพื่อหลีกเลี่ยงข้อผิดพลาดในการโหลดไฟล์**

{{< highlight csharp >}}
            string srcFile = "shirt-color.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}
