---
title: Aspose.PSD for .NET 22.3 - บันทึกการเผยแพร่
type: docs
weight: 100
url: /th/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการเผยแพร่สำหรับ [Aspose.PSD for .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**สำคัญ**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-210|เพิ่มโครงสร้าง IsOpen สำหรับ Layer Group|คุณลักษณะ|
|PSDNET-643|รูป PSD ที่มีแมสค์เรทเทอร์จะละทิ้งแมสค์เมื่อบันทึกเป็นรูป PSD 16 บิต|ข้อผิดพลาด|
|PSDNET-899|โหมดผสม Dissolve ไม่ถูกใช้ในโฟลเดอร์ที่มีแมสค์|ข้อผิดพลาด|
|PSDNET-1047|ไฟล์ที่เฉพาะเจาะจงไม่สามารถเปิดโดย Photoshop หลังจากบันทึกใน Aspose.PSD 21.11|ข้อผิดพลาด|
|PSDNET-1068|เรนเดอร์ไม่ถูกต้องของเลเยอร์ที่โหมดผสม Linear Dodge (Add)|ข้อผิดพลาด|
|PSDNET-1069|เลเยอ์ Pattern Fill ทำให้เกิดข้อยกเว้นเมื่ออัปเดตหลังจากโหลด|ข้อผิดพลาด|


## **การเปลี่ยนแปลงใน API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **API ที่ถูกลบ:**
- ไม่มี


## **ตัวอย่างการใช้:**

**PSDNET-210. เพิ่มโครงสร้าง IsOpen สำหรับ Layer Group**

{{< highlight csharp >}}
// ตัวอย่างการอ่านและเขียนคุณสมบัติ IsOpen ในระหว่างการทำงาน
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. รูป PSD ที่มีแมสค์เรทเทอร์จะละทิ้งแมสค์เมื่อบันทึกเป็นรูป PSD 16 บิต**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. โหมดผสม Dissolve ไม่ถูกใช้ในโฟลเดอร์ที่มีแมสค์**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. ไฟล์ที่เฉพาะเจาะจงไม่สามารถเปิดโดย Photoshop หลังจากบันทึกใน Aspose.PSD 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // ต้องเปิดไฟล์ PSD ผลลัพธ์ด้วย Photoshop ด้วยตนเอง

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // ไม่มีข้อยกเว้น
            }
{{< /highlight >}}

**PSDNET-1068. เรนเดอร์ไม่ถูกต้องของเลเยอร์ที่โหมดผสม Linear Dodge (Add)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. เลเยอร์ Pattern Fill ทำให้เกิดข้อยกเว้นเมื่ออัปเดตหลังจากโหลด**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}
