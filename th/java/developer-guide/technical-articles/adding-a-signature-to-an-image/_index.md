---
title: เพิ่มลาย เซ็นเซอร์ลงในรูปภาพ
type: docs
weight: 10
url: /th/java/adding-a-signature-to-an-image/
---

## **เพิ่มลาย เซ็นเซอร์**

การเพิ่มลาย เซ็นเซอร์ลงในรูปภาพ บางครั้งจำเป็นต้องลงลาย เซ็นเซอร์ที่ใช้สำหรับลายเซ็นดิจิทัลลงในภาพเพื่อป้องกันการทำของโกง ความคิดอื่น ๆ อาจเป็นการปรับปรุงรูปภาพให้อยู่ในรูปแบบที่คล้ายกับการนำไปแสดงในแกลเลอรี ไม่ว่าเหตุผลจะเป็นอย่างไร  APIs ของ Aspose.PSD จะมอบความสามารถในการเพิ่มลาย เซ็นเซอร์ลงในรูปภาพโดยใช้กลไกที่ง่ายที่สุดตามที่อธิบายด้านล่างนี้ โปรดทราบว่าตัวอย่างนี้ใช้ตัวอย่างหรือ API เฉพาะเพื่อวาดภาพอื่นขึ้นบนพื้นผิวภาพดั้งเดิม ในการสื่อผลการดำเนินการ เราจะโหลดภาพ PSD จากดิสก์และวาดภาพอื่นๆต่อแล้วยกลางภาพด้วยการใช้ตัวอย่างที่ใช้เมธอดวาดของคลาส Graphics ในการแสดงผล เราจะบันทึผลลัพธ์เป็นรูปภาพในรูปแบบ PNG โดยใช้ PngOptions ที่คลาส ด้านล่างคือตัวอย่างการเพิ่มลาย เซ็นเซอร์ลงในรูปภาพ โค้ดตัวอย่างได้ถูกแบ่งเป็นส่วน เพื่อทำให้ง่ายต่อการติดตาม ขั้นตอนต่อไปนี้แสดงวิธีทำเบื้องต้น:


- โหลดภาพหลักและภาพรอง (ภาพลายเซ็นเซอร์)
- สร้างและกำหนดค่าวัตถุกราฟริกส์
- วาดภาพโดยใช้เมธอดวาดของคลาสกราฟิกส
- บันทึผลลัพธ์ในรูปแบบ PNG

### **ตัวอย่างโปรแกรม**

#### **โหลดภาพ**
ก่อนอื่น สร้างอินสแตนช์ของคลาสภาพเพื่อโหลดภาพตัวอย่างจากดิสก์

#### **สร้างและกำหนดค่าวัตถุกราฟิกส**
หลังจากโหลดภาพ สร้างและกำหนดค่าวัตถุกราฟิกสอ็อบเจกต์ขณะใช้วัตถุของภาพหลัก

#### **วาดภาพภาพรองบนภาพหลัก**
จากนั้น โดยใช้เมธอดวาดของคลาสกราฟีกส เพิ่มภาพในตำแหน่งในภาพหลัก มีตัวนับเวอร์วู้드ของเมธอดวาดทั้งหมดที่ยอมรับวัตถุของภาพเป็นพารามิเตอร์แรกในขณะที่พารามิเตอร์ทุกตัวอื่นๆสัมพันธ์กับตำแหน่งที่ภาพต้องถูกวาด ในที่นี้เพื่อการสื่อการแสดงตัวินโค้ดต่อไปนี้ใช้ภเวอร์ชันของดรอว์อิเมจแรชซึ่งยอมรับวัตถุของพอยนโดวะว่าของ บังเกอร์ยูซเอ็ดอ่านดรอว์อิเมจซี่เดอดว้อดพารามิเตอร์ที่สองพารามิเตอร์แรกแล้วลองที่จะวาดลาย เซ็็นเซอร์บนมุมล่างขวาของภาพหลัก

#### **บันทึภาพ**
สุดท้ายบันทึภาพกลับไปยังดิสก์โดยใช้ไฟล์ PNG โดยใ้ PngOptions คลาส

#### **รหัสสมบูรณ์**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}
