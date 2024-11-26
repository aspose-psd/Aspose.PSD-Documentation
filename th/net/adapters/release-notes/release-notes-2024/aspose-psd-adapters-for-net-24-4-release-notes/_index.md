---
title: รายละเอียดการอัปเดต Aspose.PSD Adapters สำหรับ .NET 24.4
type: เอกสาร
weight: 100
url: /th/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีรายละเอียดการอัปเดตสำหรับ [Aspose.PSD Adapters สำหรับ .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Key**     | **สรุป**                                                         | **หมวดหมู่** |
|:------------|:-----------------------------------------------------------------|:--------------|
| PSDNET-1985 | เผยแพร่ครั้งแรกของ Aspose.PSD.Adapters.Imaging ไปยัง Nuget  | ปรับปรุง |


## **การเปลี่ยนแปลง API สาธารณะ**
# **เพิ่ม API:**
- ไม่มี

# **นำ API ออก:**
- ไม่มี

## **ตัวอย่างการใช้:**

โปรดตรวจสอบ[หน้าเอกสารของ Aspose.PSD.Adapters](/psd/th/net/adapters)

**PSDNET-1985. ตัวอย่างการใช้ Aspose.PSD.Adapters อย่างครบถ้วน**

{{< highlight csharp >}}
// เพิ่มการเปิดใช้งานของตัวปรับเครียดในการกำหนดค่าเริ่มต้นของคุณ 
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// เปิดใช้งาน Exporters เพิ่มเติม
Aspose.PSD.Adapters.Imaging.EnableExporters();

// เพื่อใช้งานกับตัวปรับเครียด คุณต้องเป็นที่มีใบอนุญาตของทั้ง Aspose.PSD และ Adaptee
// นี่คือวิธีการใช้ใบอนุญาตของ Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// นี่คือตัวอย่างของวิธีการใช้ใบอนุญาตของ Adaptee สำหรับ Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// จากนั้นคุณสามารถรันโค้ดใดๆ ของ Adapters หรือ PSD หรือ Imaging library

// หลังจากนี้ ทุกไฟล์เหล่านี้สามารถถูกเปิดโดย Aspose.PSD โดยไม่ต้องมีโค้ดเพิ่มเติมเช่น
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // หลังจากการดำเนินการของโค้ดนี้ คุณจะได้ไฟล์ PSD ที่ถูกสร้างจาก WEBP และสามารถใช้ Filter, Layers และ Adjustments ของ Aspose.PSD รวมถึงการทำการแปลงฟังก์ชัน Warp
}

// คุณสามารถสร้าง Adaptees' Images เพื่อใช้งานรูปภาพเป็นรูปแบบ PSD เพิ่มเติม
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // ใช้ Aspose.Imaging API ในการแก้ไขไฟล์ WEBP ด้วยคุณลักษณะที่เฉพาะเจาะจงของ Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // จากนั้นเพียงแค่ใช้เมธอด ToPsdImage() และแก้ไขไฟล์เหมือน PSD ด้วยคุณลักษณะเหมือน Photoshop รวมถึงการใช้เลเยอร์, ฟิลเตอร์อัจฉริยะ และวัตถุอัจฉริยะ
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("ข้อความบางอย่าง", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // บันทึกไฟล์ PSD สุดท้ายโดยใช้ Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// หากคุณไม่ต้องการใช้ Loaders หรือ Exporters ที่ให้มาจาก Adapters เพียงเท่านี้คุณสามารถปิดใช้งาน
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
