---
title: การเพิ่มลายน้ำลงในภาพ
type: docs
weight: 30
url: /th/net/adding-a-watermark-to-an-image/
---

## **การเพิ่มลายน้ำลงในภาพ**
เอกสารนี้อธิบายวิธีการเพิ่มลายน้ำลงในภาพโดยใช้ Aspose.PSD การเพิ่มลายน้ำลงในภาพเป็นความต้องการที่สามารถพบเห็นในแอปพลิเคชันประมวลผลภาพ ตัวอย่างนี้ใช้คลาส Graphics เพื่อวาดสตริงบนพื้นผิวภาพ

### **การเพิ่มลายน้ำ**
เพื่อสาธิตการดำเนินการ จะโหลดภาพ BMP จากดิสก์และวาดสตริงเป็นลายน้ำบนพื้นผิวภาพโดยใช้เมธอด DrawString ของคลาส Graphics เราจะบันทึกภาพเป็นรูปแบบ PNG โดยใช้คลาส PngOptions ด้านล่างเป็นตัวอย่างโค้ดที่สาธิตวิธีการเพิ่มลายน้ำลงในภาพ โค้ดตัวอย่างถูกแบ่งเป็นส่วนเพื่อทำให้ง่ายต่อการติดตาม ตามลำดับ ตัวอย่างแสดงวิธีการ:

1. [โหลด](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) ภาพ
1. สร้างและกำหนดค่าวัตถุ [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)
1. สร้างและกำหนดค่า Font และวัสดุ [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush)
1. วาดสตริงเป็นลายน้ำโดยใช้เมธอด DrawString ของคลาส Graphics
1. บันทึกภาพเป็น PNG

โค้ดชุดต่อไปนี้แสดงวิธีการเพิ่มลายน้ำในภาพ

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **การเพิ่มลายน้ำแนวเส้นทแยง**
การเพิ่มลายน้ำแนวเส้นทแยงในภาพคล้ายกับการเพิ่มลายน้ำแนวนอนที่พูดถึงข้างต้น โดยมีความแตกต่างบางที ในการสาธิตการดำเนินการ เราจะโหลดภาพ JPG จากดิสก์ เพิ่มการแปลงโดยใช้วัตถุคลาส [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) และวาดสตริงเป็นลายน้ำบนพื้นผิวภาพโดยใช้เมธอด DrawString ของคลาส Graphics ด้านล่างเป็นตัวอย่างโค้ดที่สาธิตวิธีการเพิ่มลายน้ำแนวเส้นทแยงในภาพ โค้ดตัวอย่างถูกแบ่งเป็นส่วนเพื่อทำให้ง่ายต่อการติดตาม ตามลำดับ ตัวอย่างแสดงวิธีการ:

1. โหลดภาพ
1. สร้างและกำหนดค่าวัตถุ Graphics
1. สร้างและกำหนดค่า Font และ SolidBrush 
1. รับขนาดของภาพในวัตถุ [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef)
1. สร้างอินสแตนซ์ของคลาส Matrix และดำเนินการแปลง
1. กำหนดการแปลงให้กับวัตถุ Graphics
1. สร้างและกำหนดค่าวัตถุ [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat)
1. วาดสตริงเป็นลายน้ำโดยใช้เมธอด DrawString ของคลาส Graphics
1. บันทึกรูปภาพที่ได้

โค้ดชุดต่อไปนี้แสดงวิธีการเพิ่มลายน้ำแนวเส้นทแยง

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}

