---
title: บันทึกการเปลี่ยนแปลง Aspose.PSD สำหรับ .NET 18.8
type: docs
weight: 50
url: /th/net/aspose-psd-for-net-18-8-release-notes/
---

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-68|สนับสนุนคุณสมบัติ LayerCreationDateTime|คุณลักษณะ|
|PSDNET-67|สนับสนุนการเน้นสี SheetColor|คุณลักษณะ|
|PSDNET-66|สามารถผสานเลเยอร์ระหว่างกันได้|คุณลักษณะ|
|PSDNET-65|เพิ่มการสนับสนุนบางอย่างของคุณสมบัติ Text Layer BoundBox|คุณลักษณะ|
|PSDNET-64|เพิ่มการสนับสนุน IopaResource|คุณลักษณะ|
|PSDNET-56|สนับสนุนเลเยอร์เอฟเฟกสำหรับรูปแบบ PSD|คุณลักษณะ|
|PSDNET-55|สนับสนุน InterruptMonitor สำหรับ .Net|คุณลักษณะ|
|PSDNET-50|ทำให้เลเยอร์ซ้อนกันได้|คุณลักษณะ|
|PSDNET-49|เพิ่มการแสดงผลของคุณสมบัติความทึบแสงในเลเลอร์|คุณลักษณะ|
|PSDNET-43|นำสมการเส้นโค้ง Adjustment Layer|คุณลักษณะ|
|PSDNET-42|เพิ่มการสนับสนุน Curves Adjustment Layer|คุณลักษณะ|
|PSDNET-41|นำเสนอการแสดงผลของ Levels Adjustment Layer|คุณลักษณะ|
|PSDNET-40|เพิ่มการสนับสนุน Levels Adjustment Layer|คุณลักษณะ|
|PSDNET-37|เพิ่มการสนับสนุน Channel Mixer Adjustment Layer|คุณลักษณะ|
|PSDNET-35|เพิ่มการสนับสนุน Hue/Saturation Adjustment Layer|คุณลักษณะ|
|PSDNET-34|นำเสนอการแสดงผลของ Exposure Adjustment Layer สำหรับการส่งออก|คุณลักษณะ|
|PSDNET-31|เพิ่มการสนับสนุนสำหรับการแสดงผลของ ChannelMixer adjustment layer|คุณลักษณะ|
|PSDNET-26|เพิ่มการสนับสนุน Clipping mask|คุณลักษณะ|
|PSDNET-13|เพิ่มการสนับสนุนเลเลอร์มาสก์|คุณลักษณะ|
|PSDNET-9|เพิ่มการสนับสนุน Photo Filter adjustment layer|คุณลักษณะ|
|PSDNET-8|เพิ่มการสนับสนุนเลเลอร์ Channel mixer adjustment|คุณลักษณะ|
|PSDNET-7|เพิ่มการสนับสนุน Exposure adjustment layer|คุณลักษณะ|
|PSDNET-6|เพิ่มการสนับสนุน Brightness/Contrast adjustment layer|คุณลักษณะ|
|PSDNET-5|เพิ่มการสนับสนุนบางส่วนของการปรับที่|คุณลักษณะ|
|PSDNET-3|เพิ่มการสนับสนุน PSD NoBreak ตัวเลือกข้อความ|คุณลักษณะ|
|PSDNET-2|ความสามารถในการเพิ่ม Text Layer ในเวลาการทำงาน|คุณลักษณะ|
|PSDNET-62|Codec สามารถบันทึกได้ภาพช่อง 16 บิตไม่ได้|ปรับปรุง|
|PSDNET-61|บันทึกภาพ PSD ผลิตสีไม่ถูกต้อง|ปรับปรุง|
|PSDNET-60|พิกัดของมุมบนซ้ายไม่ถูกต้องในการปรับปรุง|ปรับปรุง|
|PSDNET-59|ข้อยกเว้นในการปรับปรุงชั้นข้อความ|ปรับปรุง|
|PSDNET-58|เปิดเผยคุณสมบัติของรูปภาพ JPEG2000 ให้เป็นสาธารณะ|ปรับปรุง|
|PSDNET-57|แก้ไขตัวเลือก 24bpp สำหรับการส่งออกเป็น BMP|ปรับปรุง|
|PSDNET-46|ข้อความการปรับปรุงถูกละเลยสำหรับการแปลง PSD สี CMYK เป็น TIFF หรือ JPG|ปรับปรุง|

## ตัวอย่างการใช้งาน:
**PSDNET-68 การสนับสนุนคุณสมบัติ LayerCreationDateTime**

{{< highlight java >}}

// ตัวอย่างการใช้งาน LayerCreationDateTime property

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // ตรวจสอบว่าวันที่และเวลาการสร้างได้รับการอัปเดตบนเลเยอร์ที่สร้างขึ้นใหม่

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 การสนับสนุนการเน้นสี SheetColor**

{{< highlight java >}}

// ตัวอย่างการใช้งานคุณสมบัติ SheetColorHighlight

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);



    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 ความสามารถในการผสานเลเยอร์ระหว่างกัน**

{{< highlight java >}}

// ตัวอย่างการผสานเลเลอร์หนึ่งในอีกหนึ่งเลเลอร์

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

	im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 เพิ่มการสนับสนุนบางส่วนของคุณสมบัติ Text Layer BoundBox**

{{< highlight java >}}

// ตัวอย่างกล่องข้อความ

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // ขนาดของเลเลอร์คือขนาดของพื้นที่ที่สร้าง

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox คือขนาดเลเลอร์สูงสุดสำหรับ Text Layer

    // ภายในพื้นที่นี้ PS จะพยายามปรับข้อความของคุณ

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 เพิ่มการสนับสนุน IopaResource**

{{< highlight java >}}

// การเปลี่ยนคุณสมบัติความทึบสีโดยการเปลี่ยน IopaResource

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];



    var resources = layer.Resources;

    foreach (var resource in resources)

    {

        if (resource is IopaResource)

        {

            var iopaResource = (IopaResource)resource;

            iopaResource.FillOpacity = 200;

        }

    }



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-56 สนับสนุนเอฟเฟกส์เลเยอร์สำหรับรูปแบบ PSD**

{{< highlight java >}}

 using (

    PsdImage image =

        (PsdImage)

        Aspose.PSD.Image.Load(

            sourceFileName,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                output,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 การสนับสนุน InterruptMonitor สำหรับ .Net**

{{< highlight java >}}

         public void InterruptMonitorTest(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // เวลาถามควรน้อยกว่าเวลาที่ต้องใช้ในการแปลงรูปภาพทั้งหมด (โดยไม่ต้องหยุด)

                System.Threading.Thread.Sleep(3000);

                // หยุดกระบวนการ

                monitor.Interrupt();

                System.Console.WriteLine("หยุดกระทำการบันทึกเธรด #{0} เมื่อ {1}", thread.ManagedThreadId, System.DateTime.Now);

                // รอจนกระทำการหยุด...

                thread.Join();

            }

            finally

            {

                // ถ้าไฟล์ที่จะลบไม่มีอยู่จริง จะไม่สร้างข้อยกเว้น

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// เริ่มการแปลงภาพและรอจนกว่าจะหยุด

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// ตำแหน่งของอินพุทภาพ

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// ตำแหน่งสำหรับเลเลอร์ที่อยู่

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Interrupt monitor.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// ตัวเลือกการบันทึก

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// สร้างอินสแตนซ์ของคลาส SaveImageWorker

            /// </summary>

            /// <param name="inputPath">ตำแหน่งของอินพุทภาพ.</param>

            /// <param name="outputPath">ตำแหน่งสำหรับเลเลอร์ที่อยู่.</param>

            /// <param name="saveOptions">ตัวเลือกการบันทึก.</param>

            /// <param name="monitor">Interrupt monitor.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// พยายามแปลงภาพจากรูปแบบหนึ่งเป็นอีกหนึ่งรูปแบบ รวมกับการแก้ไขกระทำการหยุด

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("คาดว่ากระทำการหยุด.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("กระทำการบันทึกเธรด #{0} เสร็จเมื่อ {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 ทำให้เป็นไปได้ในการรวมเลเยอร์**

{{< highlight java >}}

 // การผสาน PSD ทั้งหมด

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// ผสานเลเยอร์หนึ่งในอีกเลเยอร์หนึ่ง

string sourceFileName="ThreeRegularLayersSemiTransparent.psd";
string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))
{
    var bottomLayer = im.Layers[0];
    var middleLayer = im.Layers[1];
    var topLayer = im.Layers[2];
    var layer1 = im.MergeLayers(bottomLayer, middleLayer);
    var layer2 = im.MergeLayers(layer1, topLayer);
    // ตั้งค่าเลเยอร์หลายชั้น
    im.Layers = new Layer[] { layer2 };
    im.Save(exportPath);	 
}

{{< /highlight >}}

**PSDNET-49 เพิ่มการแสดงผลของคุณสมบัติความทึบแสงในเลเลอร์**

{{< highlight java >}}

 // เปลี่ยนคุณสมบัติความทึบสี

string sourceFileName = "FillOpacitySample.psd";
string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))
{
    var layer = im.Layers[2];
    layer.FillOpacity = 5;
    im.Save(exportPath);	
}

{{< /highlight >}}

**PSDNET-43 นำเสนอสมการเส้นโค้ง Adjustment Layer**

{{< highlight java >}}

 // การแก้ไขเลเยอร์เส้นโค้ง

string sourceFileName = "CurvesAdjustmentLayer";
string psdPathAfterChange = "CurvesAdjustmentLayerChanged";
string pngExportPath = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)
{
    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))
    {
        foreach (var layer in im.Layers)
	    {
            if (layer is CurvesLayer)
            {
                var curvesLayer = (CurvesLayer)layer;
                if (curvesLayer.IsDiscreteManagerUsed)
                {
                    var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();
                    for (int i = 10; i < 50; i++)
                    {
                        manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));
                    }
                }
                else
                {
                    var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();
                    manager.AddCurvePoint(0, 50, 100);
                    manager.AddCurvePoint(0, 150, 130);
                }
            }
        }
    }
    // บันทึก PSD
    im.Save(psdPathAfterChange + j.ToString() + ".psd");
    // บันทึก PNG
    var saveOptions = new PngOptions();
    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;
    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);
}

{{< /highlight >}}

**PSDNET-42 เพิ่มการสนับสนุน Curves Adjustment Layer**

{{< highlight java >}}

 // การแก้ไขเลเยอร์เส้นโค้ง

string sourceFileName = "CurvesAdjustmentLayer";
string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)
{
    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))
    {
        foreach (var layer in im.Layers)
	    {
            if (layer is CurvesLayer)
            {
                var curvesLayer = (CurvesLayer)layer;
                if (curvesLayer.IsDiscreteManagerUsed)
                {
                    var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();
                    for (int i = 10; i < 50; i++)
                    {
                        manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));
                    }
                }
                else
                {
                    var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();
                    manager.AddCurvePoint(0, 50, 100);
                    manager.AddCurvePoint(0, 150, 130);
                }
            }
	    }
    }
    // บันทึก PSD
    im.Save(psdPathAfterChange + j.ToString() + ".psd");
}

{{< /highlight >}}