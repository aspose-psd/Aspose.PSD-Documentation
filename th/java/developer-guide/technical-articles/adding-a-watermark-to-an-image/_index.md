---
title: การเพิ่มลายน้ำลงในรูปภาพ
type: docs
weight: 20
url: /th/java/adding-a-watermark-to-an-image/
---

## **การเพิ่มลายน้ำลงในรูปภาพ**
เอกสารนี้อธิบายถึงวิธีการเพิ่มลายน้ำลงในรูปภาพโดยใช้ Aspose.PSD การเพิ่มลายน้ำลงในรูปภาพเป็นความต้องการที่พบบ่อยสำหรับแอปพลิเคชันประมวลผลภาพ ตัวอย่างนี้ใช้คลาส Graphics เพื่อวาดสตริงบนพื้นผิวรูปภาพ

### **การเพิ่มลายน้ำ**
เพื่อสาธิตการดำเนินการ เราจะโหลดรูปภาพ BMP จากดิสก์และวาดสตริงเป็นลายน้ำบนพื้นผิวรูปภาพโดยใช้วิธี DrawString ของคลาส Graphics เราจะบันทึกรูปภาพเป็นรูปแบบ PNG โดยใช้คลาส PngOptions ด้านล่างเป็นตัวอย่างโค้ดที่แสดงวิธีการเพิ่มลายน้ำลงในรูปภาพ โค้ดตัวอย่างถูกแบ่งเป็นส่วนเพื่อทำให้ง่ายต่อการติดตาม ขั้นตอนต่อขั้น ตัวอย่างแสดงวิธีการ:

1. โหลดรูปภาพ
1. สร้างและกำหนดค่าวัตถุ Graphics
1. สร้างและกำหนดค่า Font และ SolidBrush
1. วาดสตริงเป็นลายน้ำโดยใช้วิธี DrawString ของคลาส Graphics
1. บันทึกรูปภาพเป็น PNG

ส่วนโค้ดต่อไปนี้แสดงให้เห็นวิธีการเพิ่มลายน้ำในรูปภาพ.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}

### **การเพิ่มลายน้ำแนวเฉียง**
การเพิ่มลายน้ำแนวเฉียงในรูปภาพคล้ายกับการเพิ่มลายน้ำแนวนอนที่อธิบายไว้ข้างต้น โดยมีความแตกต่างเล็กน้อย เพื่อสาธิตการดำเนินการ เราจะโหลดรูปภาพ JPG จากดิสก์ เพิ่มการแปลงใช้วัตถุของคลาส Matrix และวาดสตริงเป็นลายน้ำบนพื้นผิวรูปภาพโดยใช้วิธี DrawString ของคลาส Graphics ตัวอย่างโค้ดถูกแบ่งเป็นส่วนเพื่อทำให้ง่ายต่อการติดตาม ขั้นตอนต่อขั้น ตัวอย่างแสดงวิธีการ:

1. โหลดรูปภาพ
1. สร้างและกำหนดค่าวัตถุ Graphics
1. สร้างและกำหนดค่า Font และ SolidBrush
1. รับขนาดของรูปภาพในวัตถุ SizeF
1. สร้างอินสแตนซ์ของคลาส Matrix และดำเนินการแปลงทวนสถานะ
1. กำหนดการแปลงให้กับวัตถุ Graphics
1. สร้างและกำหนดค่าวัตถุ StringFormat
1. วาดสตริงเป็นลายน้ำโดยใช้วิธี DrawString ของคลาส Graphics
1. บันทึกรูปภาพที่ได้

ส่วนโค้ดต่อไปนี้แสดงให้เห็นวิธีการเพิ่มลายน้ำแนวเฉียง.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
