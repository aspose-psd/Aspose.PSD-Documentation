---
title: Aspose.PSD for .NET 22.10 - บันทึกการออกแบบ
type: docs
weight: 30
url: /th/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการออกแบบสำหรับ [Aspose.PSD for .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- การปล่อยออกมีปัญหาทับถั่วเมื่อส่งออก 16 บิต ดังนั้นเราขอแนะนำให้ระมัดระวังเมื่อใช้คุณสมบัตินี้ในการปล่อยออกนี้
โปรดอย่าอัปเดต Aspose.PSD เป็น 22.9-22.10 หากการประมวลผลรูปภาพ 16 บิตเป็นฟังก์ชันหลักของคุณ

เรากำลังทำการหาทางแก้ไขปัญหาเหล่านี้

{{% /alert %}}

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-1287|ลบคุณสมบัติล้าสมัยใน Lfx2Resource|การปรับปรุง|
|PSDNET-1071|Aspose.PSD ไม่สามารถเปิด PSD (RGB/16 บิต) ด้วยการบีบอัด ZipWithoutPrediction|ข้อบกพร่อง|
|PSDNET-1257|เอฟเฟกของไทม์ไลน์หายไปและแสดงอย่างแปลกประหลาด (ใน Photoshop)|ข้อบกพร่อง|
|PSDNET-1278|การโปร่งใสไม่ทำงานสำหรับเอ็ฟเฟกต์ปักขอบด้วยตำแหน่งภายใน|ข้อบกพร่อง|
|PSDNET-1279|การเกิดข้อผิดพลาด: ปัญหาในการเปิดไฟล์ PSD|ข้อบกพร่อง|
|PSDNET-1284|การอัพเดทข้อความล้มเหลวด้วยสัญลักษณ์เอเชียบางรูปแบบ ข้อผิดพลาดในการวิเคราะห์สัญลักษณ์เฉพาะ|ข้อบกพร่อง|
|PSDNET-1291|การอัพเดทข้อความล้มเหลวด้วยสัญลักษณ์เอเชียบางรูปแบบ ข้อผิดพลาดในการเรนเดอร์สัญลักษณ์เฉพาะ|ข้อบกพร่อง|
|PSDNET-1292|ข้อผิดพลาดในการเปิดไฟล์ที่ส่งออกโดย Photoshop หลังจากบันทึกสัญลักษณ์เอเชียบางรูปแบบ|ข้อบกพร่อง|


## **การเปลี่ยนแปลง API สาธารณะ**
# **เพิ่ม API:**
- ไม่มี


# **API ที่ถูกลบ:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **ตัวอย่างการใช้งาน:**

**PSDNET-1071. Aspose.PSD ไม่สามารถเปิด PSD (RGB/16 บิต) ด้วยการบีบอัด ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. เอฟเฟกของไทม์ไลน์หายไปและแสดงอย่างแปลกประหลาด (ใน Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // สร้างไทม์ไลน์พร้อมกับเฟรมเพียงหลายเฟรม
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. การโปร่งใสไม่ทำงานสำหรับเอ็ฟเฟกต์ปักขอบด้วยตำแหน่งภายใน**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. การเกิดข้อผิดพลาด: ปัญหาในการเปิดไฟล์ PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. การอัพเดทข้อความล้มเหลวด้วยสัญลักษณ์เอเชียบางรูปแบบ ข้อผิดพลาดในการวิเคราะห์สัญลักษณ์เฉพาะ**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // เลือกสัญลักษณ์ที่มีปัญหา

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. ลบคุณสมบัติล้าสมัยใน Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // อัพเดตเอฟเฟกต์ตัวเลือกโหมดผสม
    effect.BlendMode = BlendMode.Darken;

    // อัพเดตเอฟเฟกต์ตัวเลือกความทศพทม
    effect.Opacity = 128; // 50%

    // อัพเดตเอฟเฟกต์สตรอกความทศพทม
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. การอัพเดตข้อความล้มเหลวด้วยสัญลักษณ์เอเชียบางรูปแบบ ข้อผิดพลาดในการเรนเดอร์สัญลักษณ์เฉพาะ**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // เลือกสัญลักษณ์ที่มีปัญหา

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. ข้อผิดพลาดในการเปิดไฟล์ที่ส่งออกโดย Photoshop หลังจากบันทึกสัญลักษณ์เอเชียบางรูปแบบ**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}
