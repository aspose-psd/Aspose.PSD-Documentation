---
title: Aspose.PSD สำหรับ .NET 24.3 - บันทึกการอัปเดต
type: docs
weight: 100
url: /th/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD สำหรับ .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **สรุป**                                                          | **หมวดหมู่** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [รูปแบบ AI] ลดเวลาในการโหลดรูปภาพ AI หลายหน้าขนาดใหญ่     |     การปรับปรุง     |
| PSDNET-1905 | ไฟล์ PSD หลังจากแปลงจาก 8 บิตเป็น 16 บิตกลายเป็นเขียนไม่อ่านได้ |     บั๊ก     |
| PSDNET-1906 | ไฟล์ PSD หลังจากแปลงจาก 8 บิตเป็น 32 บิตกลายเป็นเขียนไม่อ่านได้ |     บั๊ก     |
| PSDNET-1921 | [รูปแบบ AI] แก้ไขปัญหาการแสดงเส้นโค้งสั้นในไฟล์ AI                 |     บั๊ก     |

## **การเปลี่ยนแปลงของ Public API**
# **APIs ที่เพิ่มเข้ามา:**
- ไม่มี

# **APIs ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้งาน:**

**PSDNET-1905. ไฟล์ PSD หลังจากแปลงจาก 8 บิตเป็น 16 บิตกลายเป็นเขียนไม่อ่านได้**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // ถูกต้อง
    }
    else
    {
        throw new Exception("ข้อมูลทรัพยากรโลกไม่ถูกต้อง, ข้อมูลทรัพยากรแรกควรเป็น Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. ไฟล์ PSD หลังจากแปลงจาก 8 บิตเป็น 32 บิตกลายเป็นเขียนไม่อ่านได้**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // ถูกต้อง
    }
    else
    {
        throw new Exception("ข้อมูลทรัพยากรโลกไม่ถูกต้อง, ข้อมูลทรัพยากรแรกควรเป็น Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [รูปแบบ AI] แก้ไขปัญหาการแสดงเส้นโค้งสั้นในไฟล์ AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
