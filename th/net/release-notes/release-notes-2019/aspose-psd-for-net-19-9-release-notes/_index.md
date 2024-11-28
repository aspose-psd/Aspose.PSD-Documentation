---
title: บันทึกการออก Aspose.PSD สำหรับ .NET 19.9
type: เอกสาร
weight: 40
url: /th/net/aspose-psd-for-net-19-9-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการออกสำหรับ [Aspose.PSD for .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-160|ดึงชื่อเลเยอค่าผิด|คุณลักษณะ|
|PSDNET-175|การรับคุณสมบัติข้อความจากส่วนข้อความที่ต่างกันใน PSD TextLayer|คุณลักษณะ|
|PSDNET-190|สนับสนุน Add กลุ่มเลเยอ|คุณลักษณะ|
|PSDNET-192|สนับสนุนคุณสมบัติขนาดสเกลสำหรับ Gradient Fill Layer|คุณลักษณะ|
|PSDNET-162|การปรับความสว่าง|การปรับปรุง|
|PSDNET-174|IndexOutOfRangeException เมื่อบันทึกรูปภาพ PSD ให้อยู่ในรูปแบบ JPEG|ข้อบกพร่อง|
|PSDNET-180|การปรับปรุงข้อความเลเยอผ่านข้อยกเว้น|ข้อบกพร่อง|
|PSDNET-182|การบันทึกรูปภาพ PSD หลังจากการดำเนินการ RotateFlip ทำให้ไฟล์เสียหายซึ่งไม่สามารถเปิดได้|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้าไป:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **API ที่ถูกนำออก:**
- ไม่มี

## **ตัวอย่างการใช้:**
**PSDNET-160. ชื่อเลเยอค่าผิด**

เพื่อแสดงชื่อเลเยออย่างถูกต้องให้ใช้คุณสมบัติ **DisplayName** ตอนนี้มี setter เพิ่มให้อ่านคุณสมบัตินี้และสามารถแก้ไขได้ เมื่อ Photoshop บันทึกชื่อเลเลเยอโดยใช้คุณสมบัติ Name ตัวอักษรเกาหลีจะถูกจัดเก็บเป็นไบต์ 63'?' ในรหัส ASCII ใช้คุณสมบัติ **DisplayName** เพราะคุณสมบัติ Name ไม่รองรับตัวอักษรเกาหลี

{{< highlight java >}}

             // ทำการเปลี่ยนแปลงชื่อเลเยอและบันทึก

            using (var image = (PsdImage)Image.Load("layers with names.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // ตั้งค่าค่าใหม่ไปยังคุณสมบัติ DisplayName

                    layer.DisplayName += "_changed";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. การรับคุณสมบัติข้อความจากส่วนข้อความที่ต่างกันใน PSD TextLayer**

{{< highlight java >}}

            const double Tolerance = 0.0001;

            var filePath = "ThreeColorsParagraphs.psd";

            var outputPath = "ThreeColorsParagraph_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var layer = im.Layers[i] as TextLayer;

                    if (layer != null)

                    {

                        var portions = layer.TextData.Items;

                        if (portions.Length != 4)

                        {

                            throw new Exception();

                        }

                        // ตรวจสอบข้อความของแต่ละส่วน

                        if (portions[0].Text != "Old " ||

                            portions[1].Text != "color" ||

                            portions[2].Text != " text\r" ||

                            portions[3].Text != "Second paragraph\r")

                        {

                            throw new Exception();

                        }

                        // ตรวจสอบข้อมูลย่อหน้า

                        // ย่อหน้ามีการคำนวณไม่เหมือนกัน

                        if (

                            portions[0].Paragraph.Justification != 0 ||

                            portions[1].Paragraph.Justification != 0 ||

                            portions[2].Paragraph.Justification != 0 ||

                            portions[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // คุณสมบัติอื่น ๆ ของย่อหน้าแรกและท่องหนึ่งเท่ากัน

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var paragraph = portions[j].Paragraph;

                            if (Math.Abs(paragraph.AutoLeading - 1.2) > Tolerance ||

                                paragraph.AutoHyphenate != false ||

                                paragraph.Burasagari != false ||

                                paragraph.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragraph.StartIndent) > Tolerance ||

                                Math.Abs(paragraph.EndIndent) > Tolerance ||

                                paragraph.EveryLineComposer != false ||

                                Math.Abs(paragraph.FirstLineIndent) > Tolerance ||

                                paragraph.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragraph.GlyphSpacing[0] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[1] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[2] - 1) > Tolerance ||

                                paragraph.Hanging != false ||

                                paragraph.HyphenatedWordSize != 6 ||

                                paragraph.KinsokuOrder != 0 ||

                                paragraph.LetterSpacing.Length != 3 ||

                                Math.Abs(paragraph.LetterSpacing[0]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[1]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[2]) > Tolerance ||

                                paragraph.LeadingType != LeadingMode.Auto ||

                                paragraph.PreHyphen != 2 ||

                                paragraph.PostHyphen != 2 ||

                                Math.Abs(paragraph.SpaceBefore) > Tolerance ||

                                Math.Abs(paragraph.SpaceAfter) > Tolerance ||

                                paragraph.WordSpacing.Length != 3 ||

                                Math.Abs(paragraph.WordSpacing[0] - 0.8) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[1] - 1.0) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[2] - 1.33) > Tolerance ||

                                Math.Abs(paragraph.Zone - 36.0) > Tolerance)

                            {

                                throw new Exception();

                            }

                        }

                        // ตรวจสอบข้อมูลสไตล์

                        // สไตล์มีสีและขนาดตัวอักษรที่ต่างกัน

                        if (Math.Abs(portions[0].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[1].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[2].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[3].Style.FontSize - 10) > Tolerance)

                        {

                            throw new Exception();

                        }

                        if (portions[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            portions[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            portions[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            portions[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var style = portions[j].Style;

                            if (style.AutoLeading != false ||

                                style.HindiNumbers != false ||

                                style.Kerning != 0 ||

                                style.Leading != 0 ||

                                style.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                style.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // ตัวอย่างการแก้ไขข้อความ

                        portions[0].Text = "Hello ";

                        portions[1].Text = "World";

                        // ตัวอย่างการลบส่วนข้อความ

                        layer.TextData.RemovePortion(3);

                        layer.TextData.RemovePortion(2);

                        // ตัวอย่างการเพิ่มส่วนข้อความใหม่

                        var createdPortion = layer.TextData.ProducePortion();

                        createdPortion.Text = "!!!\r";

                        layer.TextData.AddPortion(createdPortion);

                        portions = layer.TextData.Items;

                        // ตัวอย่างการแก้ไขย่อหน้าและสไตล์สำหรับส่วน

                        // ตั้งค่าย่อหน้าขวา

                        portions[0].Paragraph.Justification = 1;

                        portions[1].Paragraph.Justification = 1;

                        portions[2].Paragraph.Justification = 1;

                        // สีต่างกันสำหรับแต่ละสไตล์ จะถูกเปลี่ยนแต่การเรนเดอริ่งไม่รองรับอย่างเต็มรูปแบบ

                        portions[0].Style.FillColor = Color.Aquamarine;

                        portions[1].Style.FillColor = Color.Violet;

                        portions[2].Style.FillColor = Color.LightBlue;

                        // ฟอนต์ต่าง ๆ จะถูกเปลี่ยนแต่การเรนเดอริ่งไม่รองรับอย่างเต็มรูปแบบ

                        portions[0].Style.FontSize = 6;

                        portions[1].Style.FontSize = 8;

                        portions[2].Style.FontSize = 10;

                        layer.TextData.UpdateLayerData();

                        im.Save(outputPath, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. สนับสนุน Add กลุ่มเลเยอ**

{{< highlight java >}}

             // -กลุ่ม 1

            // --เลเยอ 1

            // --กลุ่ม 2

            // ---เลเยอ 2

            // ---เลเยอ 3

            // --เลเยอ 4

            string dataDir = "psdnet190_test.psd";

            var createOptions = new PsdOptions();

            createOptions.Source = new FileCreateSource(data