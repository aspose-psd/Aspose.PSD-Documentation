---
title: ข้อความปล่อย Aspose.PSD for .NET 19.8
type: สารบัญ
weight: 50
url: /th/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีข้อความปล่อยสำหรับ Aspose.PSD for .NET 19.8

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-184|โหลด JPEG, PNG และไฟล์ภาพอื่นๆ ไปยัง PsdImage จากสตรีม|คุณลักษณะ|
|PSDNET-134|สร้างการเติบโตของ Fill Layer: Gradient|คุณลักษณะ|
|PSDNET-166|การบันทึก PSD เป็น PDF ไม่ให้ข้อความที่เลือกได้|คุณลักษณะ|
|PSDNET-158|สนับสนุนการบันทึก PSB เป็น PDF|คุณลักษณะ|
|PSDNET-189|การใช้หน่วยความจำสูงในการโหลด PSD กับโหมดการอ่านอย่างเดียว|ปรับปรุง|
|PSDNET-171|หลังจากสร้างเลเยอร์ข้อความใหม่ PSD กลายเป็นไฟล์ที่ไม่สามารถอ่านได้สำหรับ PS|บัค|
|PSDNET-156|ข้อยกเว้นในการโหลด PSD|บัค|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API เพิ่มเติม:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **API ที่ถูกลบ:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **ตัวอย่างการใช้:**
**PSDNET-184. โหลด JPEG, PNG และไฟล์ภาพอื่น ๆ ไปยัง PsdImage จากสตรีม**

{{< highlight java >}}

    // โหลด JPEG, PNG และไฟล์ภาพอื่น ๆ ไปยัง PsdImage จากสตรีม

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. สร้างการเติบโตของ Fill Layer: Gradient**

{{< highlight java >}}

             // สร้างการเติบโตของ Fill Layer: Gradient

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. การบันทึก PSD เป็น PDF ไม่ให้ข้อความที่เลือกได้**

{{< highlight java >}}

  // การบันทึก PSD เป็น PDF ไม่ให้ข้อความที่เลือกได้

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. หลังจากสร้างเลเยอร์ข้อความใหม่ PSD กลายเป็นไฟล์ที่ไม่สามารถอ่านได้สำหรับ PS**

{{< highlight java >}}

 // หลังจากสร้างเลเยอร์ข้อความใหม่บนเซิร์ฟเวอร์ออก, ไฟล์ PSD กลายเป็นไฟล์ที่ไม่สามารถอ่านได้สำหรับ PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. ข้อยกเว้นในการโหลด PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. การใช้หน่วยความจำสูงในการโหลด PSD ด้วยโหมดอ่านอย่างเดียว**

{{< highlight java >}}

 // การใช้หน่วยความจำสูงในการโหลด PSD ด้วยโหมดอ่านอย่างเดียว

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // การใช้งานหน่วยความจำต้องน้อยกว่า 100 เมกะไบต์สำหรับตัวอย่างเหล่านี้

            if (memoryUsed > 100)

            {

                throw new Exception("การใช้หน่วยความจำมากเกินไป");

            }

{{< /highlight >}}

**PSDNET-158. สนับสนุนการบันทึก PSB เป็น PDF**

{{< highlight java >}}

 // สนับสนุนการบันทึก PSB เป็น PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
