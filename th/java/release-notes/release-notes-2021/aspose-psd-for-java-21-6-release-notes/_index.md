---
title: ออสโพส.PSD สำหรับ Java 21.6 - บันทึกการอัปเดต
type: งานเอกสาร
weight: 40
url: /th/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [ออสโพส.PSD สำหรับ Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDJAVA-351|เมาส์คลิปปิ้งสำหรับกลุ่มไม่แสดงอย่างถูกต้อง|ข้อผิดพลาด|
|PSDJAVA-352|การใช้เมาส์ปกติหรือเมาส์เวกเตอร์สำหรับกลุ่มเลเยอร์ถูกละเลยในขณะที่ทำการแสดงผล|ข้อผิดพลาด|
|PSDJAVA-353|ภาพ PSD ที่มีการปิดใช้งานเวกเตอร์เลเยอร์มาส์เมื่อบันทึกไฟล์จะเป็นการเปิดใช้งานเดี๋ยวนี้|ข้อผิดพลาด|
|PSDJAVA-354|มีข้อยกเว้นเมื่อสร้างเลเยอร์ข้อความที่มีข้อความมากกว่า 255 ตัวอักษร|ข้อผิดพลาด|

# **การเปลี่ยนแปลงของ API สาธารณะ**
# **API ที่เพิ่มเติม:**
- ไม่มี

# **API ที่ถูกลบ:**
- ไม่มี

# **ตัวอย่างการใช้งาน:**

**PSDJAVA-351. เมาส์คลิปปิ้งสำหรับกลุ่มไม่แสดงอย่างถูกต้อง**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. การใช้เมาส์ปกติหรือเมาส์เวกเตอร์สำหรับกลุ่มเลเยอร์ถูกละเลยในขณะที่ทำการแสดงผล**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. ภาพ PSD ที่มีการปิดใช้งานเวกเตอร์เลเยอร์มาส์เมื่อบันทึกไฟล์จะเป็นการเปิดใช้งานเดี๋ยวนี้**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. มีข้อยกเว้นเมื่อสร้างเลเยอร์ข้อความที่มีข้อความมากกว่า 255 ตัวอักษร**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
