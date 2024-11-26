---
title: Aspose.PSD for .NET 22.9 - บันทึกการอัปเดต
type: docs
weight: 40
url: /th/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- ในการอัปเดตนี้มี regression ในกรณีของการส่งออก 16 บิต ดังนั้นเราขอแนะนำให้ระมัดระวังในการใช้คุณสมบัตินี้ในการอัปเดตนี้
โปรดอย่าอัปเดต Aspose.PSD เป็นเวอร์ชัน 22.9 หากการประมวลผลภาพ 16 บิตเป็นความสาคัญของคุณ
- สำหรับรุ่น Photoshop หลายรุ่นผู้ใช้อาจพบหน้าต่างที่มีข้อผิดพลาดที่อ่านชั้นอ่าน ซึ่งจะไม่ส่งผลต่อการทำงานกับไฟล์ PSD

เรากำลังทำงานกับการแก้ไขปัญหาเหล่านี้

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-1237|สร้างโมเดล LayerStyleFX ภายในที่จะมีเอฟเฟกต์และข้อมูลที่เกี่ยวข้องสำหรับการใช้โมเดลเดียวในทรัพยากรเอฟเฟกต์ Lfx2  lmfx  และ mlst|การปรับปรุง|
|PSDNET-1227|เพิ่มการอ่านและเขียนโครงสร้าง 'Lefx' ด้วยข้อมูลเอฟเฟกต์สำหรับสถานะเลเยอร์ในโมเดลไทม์ไลน์|คุณสมบัติ|
|PSDNET-1230|การปรับสถานะของเลเยอร์ไทม์ไลน์ไปยังเลเยอร์ใน PsdImage|คุณสมบัติ|
|PSDNET-1072|ความทศนิยมที่ไม่ถูกต้องเมื่อบันทึกไฟล์ PSD (RGB/16 บิต) ในการส่งออกไปยัง 8 บิต|ข้อบกพร่อง|
|PSDNET-1140|คำยินยอมในขั้นตอนของส่วนทรัพยากรเลเยอร์ทั่วโลกเมื่อเปิดเอกสาร PSB|ข้อบกพร่อง|
|PSDNET-1266|การหลุดหน่วงขณะประมวลผลไฟล์ที่เฉพาะเจาะจง|ข้อบกพร่อง|


## **การเปลี่ยนแปลง APIs สาธารณะ**
# **APIs ที่เพิ่มเติม:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **APIs ที่ถูกลบ:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **ตัวอย่างการใช้:**

**PSDNET-1072. ความทศนิยมที่ไม่ถูกต้องเมื่อบันทึกไฟล์ PSD (RGB/16 บิต) ในการส่งออกไปยัง 8 บิต**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // ตัวเลือกการบันทึก 16 บิต
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // บันทึกรูปภาพพร้อมกับสี 16 บิต
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. คำยินยอมในขั้นตอนของส่วนทรัพยากรเลเยอร์ทั่วโลกเมื่อเปิดเอกสาร PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // ตรวจสอบการมีข้อผิดพลาด
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. เพิ่มการอ่านและเขียนโครงสร้าง 'Lefx' ด้วยข้อมูลเอฟเฟกต์สำหรับสถานะเลเยอร์ในโมเดลไทม์ไลน์**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var layerStateEffects11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    layerStateEffects11.AddDropShadow();
    layerStateEffects11.AddGradientOverlay();

    var layerStateEffects21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    layerStateEffects21.AddStroke(FillType.Color);
    layerStateEffects21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. การปรับสถานะของเลเยอร์ไทม์ไลน์ไปยังเลเยอร์ใน PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_animated.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // เปลี่ยนเฟรมที่ใช้งานจาก 0 เป็น 1 เพื่อเปิดให้เริ่มใช้การปรับสถานะเลเยอร์
    timeLine.ActiveFrame = 1;

    // ปรับเปลี่ยนใน PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. การหลุดหน่วงขณะประมวลผลไฟล์ที่เฉพาะเจาะจง**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total used bytes before test: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // ตรวจสอบการเปิดบันทึก
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total used bytes after test: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "พบการหลุดหน่วงในฟังก์ชันพื้นฐาน!");
{{< /highlight >}}
