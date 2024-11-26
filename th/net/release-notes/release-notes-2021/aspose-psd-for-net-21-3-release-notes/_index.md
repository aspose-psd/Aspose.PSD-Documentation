---
title: Aspose.PSD for .NET 21.3 - บันทึกการเปลี่ยนแปลง
type: docs
weight: 100
url: /th/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการเปลี่ยนแปลงสำหรับ [Aspose.PSD for .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-823|เพิ่ม SectionDividerLayer เพื่อปรับปรุงประสบการณ์กับกลุ่มเลเยอร์|การปรับปรุง|
|PSDNET-694|เมื่ออ่าน PattResource ความกว้างและความสูงถูกสลับกัน|ข้อบกพร่อง|
|PSDNET-789|การผสมผสานผิดพลาดของเอฟเฟกต์เลเยอร์มากกว่าหนึ่ง|ข้อบกพร่อง|
|PSDNET-805|การจัดลำดับและเหตุสรรค์การผสมผสานไม่ถูกต้องเมื่อมีเอฟเฟกต์เลเยอร์มากกว่าหนึ่ง|ข้อบกพร่อง|
|PSDNET-842|คุณสมบัติของเอฟเฟกต์ตารางไม่ได้บันทึกลงในไฟล์ PSD|ข้อบกพร่อง|

## **การเปลี่ยนแปลงใน Public API**
# **API ที่เพิ่มเติม:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้งาน:**

**PSDNET-694. เมื่ออ่าน PattResource ความกว้างและความสูงถูกสลับกัน**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // เรียกใช้การเรนเดอร์แบบรูปแบบ

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. การผสมผสานผิดพลาดของเอฟเฟกต์เลเยอร์มากกว่าหนึ่ง**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // ค้นหาเลเยอร์ข้อความ
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Best";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                        break;
                    }
                }
                // ในทางนี้เรากำลังบันทึกไฟล์ PSD ที่เปลี่ยนแปลงไว้
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. การจัดลำดับและเหตุสรรค์การผสมผสานไม่ถูกต้องเมื่อมีเอฟเฟกต์เลเยอร์มากกว่าหนึ่ง**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // ในทางนี้เรากำลังบันทึกไฟล์ PSD ที่เปลี่ยนแปลงไว้
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. เพิ่ม SectionDividerLayer เพื่อปรับปรุงประสบการณ์กับกลุ่มเลเยอร์**

{{< highlight csharp >}}
            // รหัสต่อไปนี้แสดงเลเยอร์ SectionDividerLayer และวิธีการรับข้อมูลจาก LayerGroup ที่เกี่ยวข้องกัน

            // ลำดับเลเยอร์
            //    [0]: '</Layer group>' SectionDividerLayer สำหรับ Group 1
            //    [1]: 'Layer 1' Regular Layer
            //    [2]: '</Layer group>' SectionDividerLayer สำหรับ Group 2
            //    [3]: '</Layer group>' SectionDividerLayer สำหรับ Group 3
            //    [4]: 'Group 3' GroupLayer
            //    [5]: 'Group 2' GroupLayer
            //    [6]: 'Group 1' GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "ออบเจ็กต์ไม่เท่ากัน");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // สร้างลำดับของเลเยอร์
                // เพิ่ม LayerGroup 'Group 1'
                LayerGroup group1 = image.AddLayerGroup("Group 1", 0, true);
                // เพิ่ม regular layer
                Layer layer1 = new Layer();
                layer1.DisplayName = "Layer 1";
                group1.AddLayer(layer1);
                // เพิ่ม LayerGroup 'Group 2'
                LayerGroup group2 = group1.AddLayerGroup("Group 2", 1);
                // เพิ่ม LayerGroup 'Group 3'
                LayerGroup group3 = group2.AddLayerGroup("Group 3", 0);

                // รับ SectionDividerLayer's
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // ใช้วิธี SectionDividerLayer.GetRelatedLayerGroup() เพื่อรับข้อมูล LayerGroup ที่เกี่ยวข้อง
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // เหมือนกับ LayerGroup เดิม
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // เหมือนกับ LayerGroup เดิม
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // เหมือนกับ LayerGroup เดิม

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Group 1' มี 5 เลเยอร์
            }
{{< /highlight >}}

**PSDNET-842. คุณสมบัติของเอฟเฟกต์ตารางไม่ได้บันทึกลงในไฟล์ PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "ออบเจ็กต์ไม่เท่ากัน");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // จะไม่เกิดข้อผิดพลาดของ ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // ตรวจสอบค่าที่บันทึก
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
