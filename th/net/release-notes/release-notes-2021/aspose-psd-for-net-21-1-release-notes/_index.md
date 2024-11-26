---
title: Aspose.PSD สำหรับ .NET 21.1 - บันทึกการออกอากาศ
type: docs
weight: 120
url: /th/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้ประกอบด้วยบันทึกการออกอากาศสำหรับ [Aspose.PSD สำหรับ .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: ข้อยกเว้นเมื่อพยายามแปลงไฟล์ Psd ที่เฉพาะเจาะจงเป็น png|ข้อบกพร่อง|
|PSDNET-792|ข้อยกเว้นในขณะบันทึก PSD พร้อมวัตถุอัจฉริยะเป็น PNG|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้าไป:**
- ไม่มี

# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้:**
**PSDNET-766. Aspose.PSD 20.10: ข้อยกเว้นเมื่อพยายามแปลงไฟล์ Psd ที่เฉพาะเจาะจงเป็น png**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. ข้อยกเว้นในขณะบันทึก PSD พร้อมวัตถุอัจฉริยะเป็น PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // ค้นหาชั้นวัตถุอัจฉริยะ
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // เรากำลังโหลดชั้นวัตถุอัจฉริยะจาก Memory Stream
                        // แต่เราสามารถใช้ smart.ExportContents(somePath) เพื่อส่งออกวัตถุอัจฉริยะไปยังไฟล์
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // ค้นหาชั้นข้อความ
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // เราสามารถใช้ UpdateText โดยง่าย
                                        // แต่วิธีนี้ทำให้เราสามารถแก้ไขข้อความตามชิ้น
                                        // สร้างชั้นข้อความหลายบรรทัดและคุณสมบัติอื่น ๆ ของข้อความและย่อหน้า
                                        // โปรดระวัง หากเนื้อหาวัตถุอัจฉริยะไม่ใช่ PSD คุณไม่สามารถใช้วิธีนี้ในการแก้ไขข้อความ
                                        // ในกรณีนั้นคุณควรใช้ Graphic API: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "ดีที่สุด";

                                        // คุณควรเปลี่ยนขนาดข้อความหากต้องการให้ภาพดูดี
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // มันดีกว่าที่จะใช้ ReplaceContents มันจะรีเรนเดอร์วัตถุอัจฉริยะโดยอัตโนมัติ
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // ด้วยวิธีนี้เรากำลังบันทึกไฟล์ PSD ที่เปลี่ยนแปลงแล้ว
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
