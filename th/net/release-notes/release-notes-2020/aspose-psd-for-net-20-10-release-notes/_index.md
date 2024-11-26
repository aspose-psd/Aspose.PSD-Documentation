---
title: บันทึกการอัปเดต Aspose.PSD สำหรับ .NET 20.10
type: ข้อมูลเอกสาร
weight: 30
url: /th/net/aspose-psd-สำหรับ-net-20-10-บันทึกการอัปเดต/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD สำหรับ .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**สรุป**|**ประเภท**|
| :- | :- | :- |
|PSDNET-565|ข้อยกเว้นในขณะบันทึกไฟล์ PSD ที่เฉพาะเจาะจงที่มีเลเยอร์ข้อความ|ข้อบกพร่อง|
|PSDNET-680|ฟอนต์หายไปหลังจากสังเกตไป-กลับกับ Aspose.PSD|ข้อบกพร่อง|
|PSDNET-704|การแสดงผลของเลเยอร์ Smart Object|คุณลักษณะ|
|PSDNET-707|การสนับสนุนการแปลงแต่ง Smart Object ที่ไม่ทำลงทรรยากร|คุณลักษณะ|
|PSDNET-711|เลเยอร์ข้อความขยับตำแหน่งหลังจากบันทึกโดยไม่มีการเปลี่ยนแปลงใด ๆ|ข้อบกพร่อง|
|PSDNET-720|Aspose.PSD 20.8: ข้อยกเว้นการแปลง Psd เป็น Tiff|ข้อบกพร่อง|

## **การเปลี่ยนแปลงใน Public API**
# **เพิ่ม API:**
- ไม่มี
# **ลบ API:**
- ไม่มี

## **ตัวอย่างการใช้:**
**PSDNET-565. ข้อยกเว้นในขณะบันทึกไฟล์ PSD ที่เฉพาะเจาะจงที่มีเลเยอร์ข้อความ**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. ฟอนต์หายไปหลังจากสังเกตไป-กลับกับ Aspose.PSD**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void AreEqual(int expected, int actual)
            {
                if (expected != actual)
                {
                    throw new Exception("ค่าไม่เท่ากัน");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-704. การแสดงผลของเลเยอร์ Smart Object**
{{< highlight csharp >}}
            // ตัวอย่างนี้แสดงถึงวิธีการแทนที่เนื้อหาของเลเยอร์ซมาร์ทออบเจกต์ Adobe® Photoshop® และการแสดงผลอย่างถูกต้อง
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // ตัวอย่างนี้แสดงถึงวิธีการอัปเดตแคชภาพของเลเยอร์ซมาร์ทออบเจกต์ Adobe® Photoshop® และการแสดงผลอย่างถูกต้อง
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-707. การสนับสนุนการแปลงแต่ง Smart Object ที่ไม่ทำลงทรรยากร**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // ตัวอย่างเหล่านี้แสดงการแปลงขนาดไฟล์ PSD ด้วย SmartObjectLayer
            // เราสามารถปรับขนาด, หมุน, แกว่ง, เอียง, แปลงทิศทางเปียน หรืองอเลเยอร์โดยไม่สูญเสียข้อมูลหรือคุณภาพของภาพต้นฉบับเพราะการแปลงไม่ส่งผลต่อข้อมูลต้นฉบับ

            // ตัวอย่างนี้แสดงการปรับขนาดภาพ Adobe® Photoshop® ด้วยเลเยอร์ซมาร์ทออบเจกต์:
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // ตัวอย่างนี้แสดงการปรับขนาดของไฟล์ PSD ด้วยเลเยอร์ซมาร์ทออบเจกต์
            void ExampleOfSmartObjectImageResizeSupport(string fileName)
            {
                const int scale = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Resize_" + fileName + ".psd";
                string outputPngPath = outputDir + "Resize_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int newWidth = image.Width * scale;
                    int newHeight = image.Height * scale;
                    image.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // ตัวอย่างนี้แสดงการปรับขนาดของเลเยอร์ซมาร์ทออบเจกต์ Adobe® Photoshop®
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // ตัวอย่างนี้แสดงการปรับขนาดของเลเยอร์ซมาร์ทออบเจกต์ในไฟล์ PSD
            void ExampleOfSmartObjectLayerResizeSupport(string fileName)
            {
                const double scale = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ResizeLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int newWidth = (int)(smartObjectLayer.Width * scale);
                    int newHeight = (int)(smartObjectLayer.Height * scale);
                    smartObjectLayer.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // ตัวอย่างนี้แสดงการตัดเลเยอร์ซมาร์ทออบเจกต์ Adobe® Photoshop®
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // ตัวอย่างนี้แสดงการตัดเลเยอร์ซมาร์ทออบเจกต์ในไฟล์ PSD
            void ExampleOfSmartObjectLayerCropSupport(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "CropLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "CropLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // ตัวอย่างนี้แสดงวิธีการตัดเลเยอร์ซมาร์ทออบเจกต์ Adobe® Photoshop®:
            ExampleOfSmartObjectImageCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageCropSupport("gorilla");

            // ตัวอย่างนี้แสดงวิธีการตัดไฟล์ PSD ด้วยเลเยอร์ซมาร์ทออบเจกต์
            void ExampleOfSmartObjectImageCropSupport(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Crop_" + fileName + ".psd";
                string outputPngPath = outputDir + "Crop_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Crop(25, 10, 30, 5);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
**PSDNET-711. เลเยอร์ข้อความขยับตำแหน่งหลังจากบันทึกโดยไม่มีการเปลี่ยนแปลงใด ๆ**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("ค่าเท่ากัน");
                }
            }

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PsdOptions(image));
            }

            using (PsdImage image = (PsdImage)Image.Load(output))
            {
                TextLayer txtLayer = (TextLayer)image.Layers[2];

                AreNotEqual(txtLayer.Left, txtLayer.TransformMatrix[4]);
                AreNotEqual(txtLayer.Top, txtLayer.TransformMatrix[5]);
            }
{{< /highlight >}}
**PSDNET-720. Aspose.PSD 20.8: ข้อยกเว้นการแปลง Psd เป็น Tiff**
{{< highlight csharp >}}
            using (var psdImage = (PsdImage)Image.Load("sarbarg.fin12.psd"))
            {
                psdImage.Save("result.tiff", new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
            }
{{< /highlight >}}