---
title: ครอบ, หมุน และปรับขนาดภาพ
type: docs
weight: 40
url: /th/net/crop-rotate-and-resize-images/
---

## **การครอบภาพ**
การครอบภาพมักหมายถึงการตัดส่วนของภาพด้านนอกเพื่อช่วยปรับปรุงเฟรม การครอบยังสามารถใช้เพื่อตัดส่วนของภาพเพื่อเน้นบริเวณๆ ใดบนภาพได้อีกด้วย  API จาก Aspose.PSD รองรับวิธีการครอบภาพ 2 วิธีคือ โดยการเลื่อนและด้วยกรอบ
### **การครอบโดยเลื่อน**
คลาส [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) มีเวอร์ชันของเมทอด Crop ที่มีการโองเหลืออย่างอย่างยิ่ง 4 ค่าจำนวนเต็มซึ่งแสดงถึง ซ้าย, ขวา, บน และ ล่าง โดยโครงสร้างเมตอด Crop จะย้ายขอบภาพไปสู่ศูนย์ของภาพ โครงสร้างคำสั่งด้านล่างแสดงว่าจะครอบภาพโดยใช้เลื่อน



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **การครอบโดยกรอบสี่เหลี่ยม**
คลาส [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) มีเวอร์ชันของเมทอด Crop อีกตัวซึ่งรองรับการรับอินสแตนซ์ของคลาส Rectangle คุณสามารถตัดออกส่วนใดส่วนหนึ่งของภาพได้โดยการกำหนดขอบเขตที่ต้องการให้กับออบเจกต์ Rectangle โค้ดด้านล่างแสดงผลการครอบภาพด้วยกรอบสี่เหลี่ยม



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **หมุนและพลิกภาพ**
Aspose.PSD สำหรับ .NET เป็นไลบรารีที่ใช้งานง่ายเนื่องจากมีเมทอดที่ง่ายๆ ในการดำเนินการที่ซับซ้อน ตัวอย่างเช่น, Aspose.PSD สำหรับ .NET ได้ให้เมทอด RotateFlip สำหรับคลาสฐานของมัน Image หากแอปพลิเคชั่นต้องการหมุนภาพ โดยไม่ว่าจะเป็นรูปแบบของภาพ เวอร์ชัน Aspose สามารถใช้ Rotate & Flip ตามรูปแบบเฉพาะบนภาพได้
### **การหมุนภาพ**
เมทอด Image.RotateFlip สามารถใช้เพื่อหมุนภาพไปทางเขตหน้ารวมทั้ง 90/180/270 องศา และพลิกภาพแนวนอนหรือแนวตั้
