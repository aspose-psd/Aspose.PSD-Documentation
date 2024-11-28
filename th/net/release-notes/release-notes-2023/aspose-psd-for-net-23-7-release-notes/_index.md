---
title: บันทึกการปล่อย Aspose.PSD สำหรับ .NET 23.7
type: เอกสาร
weight: 60
url: /th/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการปล่อยสำหรับ [Aspose.PSD สำหรับ .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                                                  | **หมวดหมู่** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | เพิ่มความสามารถในการส่งออกชั้นของไฟล์ PSD แต่ละชั้นเป็นไฟล์ Animated Gif                                        | คุณลักษณะ |
| PSDNET-1441 | กำหนดคุณสมบัติ Fill ของชั้นรูปร่างจากทรัพยากร vscg                                                       | คุณลักษณะ |
| PSDNET-1534 | เพิ่มประเภทของการหงุด (arc & arch)                                                                           | คุณลักษณะ |
| PSDNET-1543 | เปลี่ยนแอปพลิเคชันที่บันทึกไฟล์ PSD เป็น Aspose.PSD ถ้าคุณลักษณะ UpdateMetadata ถูกตั้งเป็นจริง       | คุณลักษณะ |
| PSDNET-1567 | เพิ่มพื้นที่การคำนวณของภาพการหงุด                                                                                  | คุณลักษณะ |
| PSDNET-1471 | Black and white adjustment Layer processes semi-transparency ผิดพลาด                                           | บั๊ก     |
| PSDNET-1505 | SmartObject ReplaceContents (เมื่อตัวเลือก AllowWarpRepaint เปิดใช้งาน) ล้มหลังจาก 2 นาทีของการคำนวณ         | บั๊ก     |
| PSDNET-1585 | เพิ่มความสามารถในการรับค่าตำแหน่งทิศเลี้ยงที่แท้จริงของ LayerGroup                                                | บั๊ก     |
| PSDNET-1589 | การปรับขนาดของชั้นทำงานผิดพลาดเมื่อไฟล์ psd มี VogkResource ด้วยโครงสร้างในจุด                   | บั๊ก     |
| PSDNET-1608 | TextBound ไม่ทำงานตามที่คาดหวัง                                                                           | บั๊ก     |
| PSDNET-1612 | เพิ่มชั้นที่สร้างด้วยสร้างค่าเริ่มต้นเข้าไปยังภาพ PSD ไม่เพิ่มองค์ประกอบเริ่มต้นไปด้วย          | บั๊ก     |
| PSDNET-1623 | การละเว้น Timeline.LoopesCount เมื่อส่งออกไปยัง GIF แอนิเมชัน                                         | บั๊ก     |


## **การเปลี่ยนแปลง API สาธารณะ**
# **เพิ่มAPI:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **ลบAPI:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **ตัวอย่างการใช้:**

**PSDNET-802. เพิ่มความสามารถในการส่งออกชั้นของไฟล์ PSD แต่ละชั้นเป็นไฟล์ Animated Gif**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // สร้างเฟรมสำหรับแต่ละชั้น
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // อัปเดตสถานะปัจจุบัน
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. กำหนดคุณสมบัติ Fill ของชั้นรูปร่างจากทรัพยากร vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// ตรวจสอบการบันทึกการเปลี่ยนแปลง
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objek tidak sama.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Black and white adjustment Layer processes semi transparency ผิดพลาด**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// ตรวจสอบการบันทึกการเปลี่ยนแปลง
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("ชั้นที่ 2 ควรเป็น BlackWhiteAdjustmentLayer");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objek tidak sama.");
    }
}
{{< /highlight >}}

**PSDNET-1505. SmartObject ReplaceContents (เมื่อตัวเลือก AllowWarpRepaint เปิดใช้งาน) ล้มหลัง 2 นาทีของการคำนวณ**

{{< highlight csharp >}}
string sourceFile = "mug 4.psd";
string changeFile = "artwork for replace.png";
string outputFile = "export.png";

int newHeight = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer smartObjectLayer = (SmartObjectLayer)psdImage.Layers[3];

    var scale = (double)newHeight / smartObjectLayer.Height;
    var newWidth = (int)Math.Round(smartObjectLayer.Width * scale);

    PsdImage innerImage = new PsdImage(newWidth, newHeight);
    innerImage.SetResolution(72, 72);

    Stream innerStream = new FileStream(changeFile, FileMode.Open);
    Layer layer = new Layer(innerStream) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        innerImage.AddLayer(layer);

        smartObjectLayer.ReplaceContents(innerImage);
        smartObjectLayer.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        innerImage.Dispose();
        innerStream.Dispose();
        layer.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. เพิ่มประเภทของการหงุด (arc & arch)**

{{< highlight csharp >}}
string sourceArcFile = "arc_warp.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_warp.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. เปลี่ยนแอปพลิเคชันที่บันทึกไฟล์ PSD เป็น Aspose.PSD ถ้าคุณลักษณะ UpdateMetadata ถูกตั้งเป็นจริง**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // หากคุณต้องการให้เครื่องมือสร้างเปลี่ยน ตรวจสอบให้แน่ใจว่าคุณสมบัติ "UpdateMetadata" ถูกตั้งเป็นจริง มันถูกตั้งเป็นจริงตามค่าเริ่มต้น
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // บันทึกรูปภาพ
    image.Save(path, psdOptions);

    // ตรวจสอบเครื่องมือสร้างในโค้ด
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // ที่นี่จะมีข้อมูลเครื่องมือสร้างที่อัปเดต
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. เพิ่มพื้นที่การคำนวณของภาพการหงุด**

{{< highlight csharp >}}
string sourceFile = "mug4_warp.psd";
string outputFile = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. เพิ่มความสามารถในการรับค่าตำแหน่งทิศเลี้ยงที่แท้จริงของ LayerGroup**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objek tidak sama.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layers = image.Layers;

    for (int i = 0; i < layers.Length; i++)
    {
        var layer = layers[i];

        if (layer is LayerGroup)
        {
            // รับ LayerGroup
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // คำนวณตำแหน่งเลี้ยงที่แท้จริง Left, Top, Right, และ Bottom
            foreach (var innerLayer in group.Layers)
            {
                if (innerLayer is AdjustmentLayer || innerLayer.Bounds.IsEmpty)
                {
                    continue;
                }

                expectedLeft = Math.Min(expectedLeft, innerLayer.Left);
                expectedTop = Math.Min(expectedTop, innerLayer.Top);
                expectedRight = Math.Max((expectedLeft + group.Width), (innerLayer.Left + innerLayer.Width));
                expectedBottom = Math.Max((expectedTop + group.Height), (innerLayer.Top + innerLayer.Height));
            }

            // LayerGroup ตำแหน่งที่ลึก, บน, ขวา, และล่างถูกคำนวณอย่างเหมาะสมตอนนี้
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. ปรับขนาดของชั้นทำงานผิดพลาดเมื่อไฟล์ psd มี VogkResource ด้วยโครงสร้างในจุด**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer layer = image.Layers[0];

        layer.Resize(50, 50);

        AssertAreEqual(layer.Height, 50);
        AssertAreEqual(layer.Width, 50);
    }
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objek tidak sama.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound ไม่ทำงานตามที่คาดหวัง**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
