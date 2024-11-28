---
title: บันทึกการอัปเดต Aspose.PSD for .NET 21.9
type: docs
weight: 40
url: /th/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-574|ทำให้การบีบอัด RLE เป็นค่าเริ่มต้นสำหรับการบันทึก PSD เพื่อหลีกเลี่ยงการสร้างไฟล์ PSD ที่ใหญ่เกินไป|คุณลักษณะ|
|PSDNET-747|รองรับ Overlay Pattern Layer Effects ด้วยโหมดสี multichannel ในไฟล์ PSD|คุณลักษณะ|
|PSDNET-951|หลังจากสร้างเลเยอร์ใหม่แล้ว Properties ของมันจะเป็นค่าว่างซึ่งทำให้ไม่สามารถทำการจัดการ (เช่นการปรับขนาด)|บั๊ก|
|PSDNET-955|ไม่รองรับวิธีการบีบอัด ZipWithPrediction สำหรับ 8 บิต|บั๊ก|

## **การเปลี่ยนแปลงสาธารณะใน API**
# **API ที่เพิ่มเข้ามา:**
- ไม่มี

# **API ที่ถูกเอาออก:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-574. ทำให้ RLE Compression เป็นค่าเริ่มต้นสำหรับการบันทึก PSD เพื่อหลีกเลี่ยงไฟล์ PSD ที่ใหญ่เกินไป**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. รองรับ Overlay Pattern Layer Effects ด้วยโหมดสี multichannel ในไฟล์ PSD**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // ไม่ควรเกิดข้อผิดพลาด
            using (var im = Image.Load(fileName, loadOptions))
            {
                // ไม่ควรเกิดข้อผิดพลาด
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. หลังจากสร้างเลเยอร์ใหม่ Properties ของมันจะเป็นค่าว่างซึ่งทำให้ไม่สามารถทำการจัดการ (เช่นการปรับขนาด)**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ReplaceColor(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // สีแดง
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // สีเขียว
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // สีน้ำเงิน
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Layer2 = null;
            Layer Layer3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region เพิ่มเลเยอร์ 1

                using (var stream = new FileStream(layer1File, FileMode.Open))
                {
                    Layer2 = new Layer(stream);

                    Layer2.Resize(image.Width, image.Height);
                    var width = Layer2.Width;
                    var height = Layer2.Height;

                    Layer2.Left = 675;
                    Layer2.Top = 0;

                    Layer2.Right = Layer2.Left + width;
                    Layer2.Bottom = Layer2.Top + height;

                    image.AddLayer(Layer2);
                }

                #endregion

                using (var stream = new FileStream(layer2File, FileMode.Open))
                {
                    Layer3 = new Layer(stream);
                    // แทนที่สีขาวด้วยสีโปร่งใส
                    ReplaceColor(Layer3, Color.White, 256, Color.Transparent);
                    Layer2.DrawImage(new Point(0, 0), Layer3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. ไม่รองรับวิธีการบีบอัด ZipWithPrediction สำหรับ 8 บิต**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
