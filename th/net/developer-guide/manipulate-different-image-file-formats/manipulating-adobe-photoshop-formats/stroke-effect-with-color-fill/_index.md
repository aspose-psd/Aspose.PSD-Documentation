---
title: การใช้ Stroke Effect พร้อมกับการเติมสี
type: คู่มือ
weight: 60
url: /th/net/stroke-effect-with-color-fill/
---

## **การใช้ Stroke Effect พร้อมกับการเติมสี**
บทความนี้สาธิตวิธีการเรนเดอร์ Stroke effect พร้อมกับการเติมสี การใช้ Stroke effect เป็นวิธีในการเพิ่มเส้น Stroke และเส้นขอบสำหรับเลเยอร์และรูปร่าง สามารถใช้สร้างเส้นสีทึบ สีไล่ระดับ และเส้นขอบลายละเอียดได้

ขั้นตอนสำหรับการเรนเดอร์ Stroke effect พร้อมกับการเติมสีมีดังนี้:

- ตั้งค่าโครงสร้าง [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource)
- โหลดไฟล์ PSD เป็นรูปภาพโดยใช้เมทอด Load ที่เปิดเผยโดยคลาส Image และกำหนด [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions)
- ตั้งค่าคุณสมบัติของการตั้งค่าสี [**ColorFillSetting**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)
- บันทึกผลลัพธ์

โค้ดย่อยต่อไปนี้แสดงวิธีการเรนเดอร์ Stroke effect พร้อมกับการเติมสี

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
