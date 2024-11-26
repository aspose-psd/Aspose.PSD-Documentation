---
title: การทำงานกับเลเยอร์ข้อความ
type: งกฤษ
weight: 170
url: /th/net/working-with-text-layers/
---

## **เพิ่มเลเยอร์ข้อความ**
Aspose.PSD สำหรับ .NET ช่วยให้คุณเพิ่มเลเยอร์ข้อความในไฟล์ PSD ได้ ขั้นตอนในการเพิ่มเลเยอร์ข้อความในไฟล์ PSD คือดังนี้:

- โหลดไฟล์ PSD เป็นภาพโดยใช้เมทอดโรงงาน [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) ที่เปิดเผยโดย [Image class](https://reference.aspose.com/psd/net/aspose.psd/image)
- เรียกใช้เมทอด [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) ซึ่งยอมรับข้อความและอินสแตนซ์ของคลาส [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- บันทึกผลลัพธ์

โค้ดตัวอย่างด้านล่างแสดงวิธีการเพิ่มเลเยอร์ข้อความในไฟล์ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **ตั้งตำแหน่งเลเยอร์ข้อความ**
Aspose.PSD สำหรับ .NET ช่วยให้คุณตั้งตำแหน่งเลเยอร์ข้อความในไฟล์ PSD ได้ ขั้นตอนในการตั้งตำแหน่งเลเยอร์ข้อความในไฟล์ PSD คือดังนี้:

- โหลดไฟล์ PSD เป็นภาพโดยใช้เมทอดโรงงาน Load ที่เปิดเผยโดย Image class
- เรียกใช้เมทอด AddTextLayer พร้อมกำหนดตำแหน่งซ้ายและบนของเลเยอร์ข้อความ
- บันทึกผลลัพธ์

โค้ดตัวอย่างด้านล่างแสดงวิธีการตั้งตำแหน่งเลเยอร์ข้อความในไฟล์ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **รับคุณสมบัติข้อความจากเลเยอร์ข้อความ**
โดยใช้ Aspose.PSD สำหรับ .NET คุณสามารถรับและอัปเดตคุณสมบัติข้อความของส่วนต่าง ๆ ของข้อความที่ใช้งานได้ในเลเยอร์ข้อความ PSD บทความนี้สาธิตวิธีการรับวาจารณญะ, สไตล์, และคุณสมบัติข้อความของเลเยอร์ข้อความและอัปเดตข้อมูลดังกล่าว

โค้ดตัวอย่างด้านล่างแสดงวิธีการทำงานนี้

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


นี่คือตัวอย่างอื่น ๆ ที่สาธิตวิธีการของนักพัฒนาสามารถเรียกใช้การจัดรูปแบบข้อความของส่วนต่าง ๆ จาก [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) โดยใช้ [Aspose.PSD สำหรับ .NET](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **อัปเดตเลเยอร์ข้อความในไฟล์ PSD**
Aspose.PSD สำหรับ .NET ช่วยให้คุณจัดการข้อความในเลเยอร์ข้อความของไฟล์ PSD โปรดใช้คลาส Aspose.PSD.FileFormats.Psd.Layers.TextLayer เพื่ออัปเดตข้อความในเลเยอร์ PSD โค้ดตัวอย่างด้านล่างโหลดไฟล์ PSD, เข้าถึงเลเยอร์ข้อความ, อัปเดตข้อความและบันทึกไฟล์ PSD ด้วยชื่อใหม่โดยใช้เมทอด [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer/methods/updatetext/index)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **รองรับเลเยอร์ข้อความในเวลาที่ดำเนินการ**
บทความนี้แสดงวิธีการเพิ่มเลเยอร์ข้อความในเวลาที่ดำเนินการสำหรับภาพ PSD โค้ดตัวอย่างมีอยู่ด้านล่าง


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
