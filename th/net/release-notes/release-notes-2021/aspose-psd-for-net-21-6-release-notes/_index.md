---
title: บันทึกการเปลี่ยนแปลง Aspose.PSD for .NET 21.6
type: docs
weight: 70
url: /th/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการเปลี่ยนแปลงสำหรับ [Aspose.PSD for .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-546|การเคลิปมาส์สำหรับกลุ่มไม่แสดงผลถูกต้อง|ข้อบกพร่อง|
|PSDNET-547|มาส์ปกติหรือเวกเตอร์สำหรับกลุ่มเลเยอร์ถูกเพิกเฉยในการแสดงผล|ข้อบกพร่อง|
|PSDNET-647|PSD ภาพที่มีเวกเตอร์เลเยอร์มาส์ถูกปิดใช้งานเมื่อบันทึกจะเปิดใช้งานเวกเตอร์เมสก์|ข้อบกพร่อง|
|PSDNET-786|ข้อยกเว้นเมื่อสร้างชั้นข้อความที่มีตัวอักษรมากกว่า 255 ตัวอักษร|ข้อบกพร่อง|
|PSDNET-900|ข้อความของชั้นข้อความไม่สามารถแสดงผลบน Linux|ปรับปรุง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- ไม่มี

# **API ที่ถูกนำออก:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-546. การเคลิปมาส์สำหรับกลุ่มไม่แสดงผลถูกต้อง**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. มาส์ปกติหรือเวกเตอร์สำหรับกลุ่มเลเยอร์ถูกเพิกเฉยในการแสดงผล**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. PSD ภาพที่มีเวกเตอร์เลเยอร์มาส์ถูกปิดใช้งานเมื่อบันทึกจะเปิดใช้งานเวกเตอร์เมสก์**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. ข้อยกเว้นเมื่อสร้างชั้นข้อความที่มีตัวอักษรมากกว่า 255 ตัวอักษร**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
