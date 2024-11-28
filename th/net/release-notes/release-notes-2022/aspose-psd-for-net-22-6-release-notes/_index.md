---
title: Aspose.PSD for .NET 22.6 - บันทึกการออกเวอร์ชัน
type: docs
weight: 70
url: /th/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการออกเวอร์ชันสำหรับ [Aspose.PSD for .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-940|สร้าง API สำหรับการรับค่าแฮชที่ไม่ตรงกันสำหรับเลเยอร์ที่คล้ายกันในไฟล์ที่แตกต่างกัน|ปรับปรุง|
|PSDNET-678|การเรนเดอร์รูปแบบ FillLayer ไม่ถูกต้องเมื่อมีรูปแบบมากกว่าหนึ่งและการจัดเรียงเลเยอร์ถูกเปลี่ยนแปลง|ข้อผิดพลาด|
|PSDNET-1125|ข้อยกเว้นในขณะโหลดไฟล์ PSD ที่ระบุกับโหมดสี CMYK|ข้อผิดพลาด|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash

# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-678. การเรนเดอร์รูปแบบ FillLayer ไม่ถูกต้องเมื่อมีรูปแบบมากกว่าหนึ่งและการจัดเรียงเลเยอร์ถูกเปลี่ยนแปลง**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. สร้าง API สำหรับการรับค่าแฮชที่ไม่ตรงกันสำหรับเลเยอร์ที่คล้ายกันในไฟล์ที่แตกต่างกัน**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    // ฟังก์ชันต่าง ๆ จะถูกเพิ่มทีหลัง
}
{{< /highlight >}}

**PSDNET-1125. ข้อยกเว้นในขณะโหลดไฟล์ PSD ที่ระบุกับโหมดสี CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}