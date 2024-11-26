---
title: ป้องกันการชะลอความเร็วเมื่อวาดภาพบนภาพที่ถูกบีบอัด
type: docs
weight: 40
url: /th/java/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **ป้องกันการชะลอความเร็วเมื่อวาดภาพบนภาพที่ถูกบีบอัด**
มักมีเวลาที่คุณต้องการดำเนินการกราฟิกอย่างเหนือจากภาพที่ถูกบีบอัดอย่างมาก ขณะที่ Aspose.PSD ต้องบีบอัดและถอดรหัสภาพในขณะเดียวกัน การชะลอความเร็วอาจเกิดขึ้น การวาดบนภาพที่ถูกบีบอัดอาจมีความมีผลกระทบต่อความเร็วด้วย
### **วิธีการแก้ปัญหา**
เพื่อป้องกันการชะลอความเร็ว เราขอแนะนำให้คุณแปลงภาพเป็นรูปแบบที่ไม่ถูกบีบอัดหรือแบบ raw ก่อนทำการกราฟิกอย่างเป็นพิเศษ
### **ใช้เส้นทางไฟล์**
ในตัวอย่างที่ตามมานี้ ภาพ PSD ถูกแปลงเป็นรูปแบบ raw (ไม่บีบอัด) และบันทึกลงบนดิสก์ ภาพที่ไม่ถูกบีบอัดจากนั้นถูกโหลดกลับมาก่อนที่จะดำเนินการกราฟิกบนมัน วิธีเดียวกันใช้สำหรับไฟล์ BMP และ GIF

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **ใช้วัตถุสตรีม**
โค้ดตัวอย่างต่อไปนี้แสดงวิธีการแปลงภาพ PSD เป็นรูปแบบ raw (ไม่บีบอัด) และบันทึกลงบนดิสก์ โดยใช้วัตถุสตรีม

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
