---
title: วิธีการใช้ Warp ใน Aspose.PSD
type: docs
weight: 40
url: /th/net/how-to-use-warp-in-aspose-psd/
---

## **ส่วนที่ 1 – การเล่นไฟล์ PSD ด้วยเอฟเฟกส์ Warp**

Photoshop บันทึกรูปภาพหลังจากการใส่เอฟเฟกส์ Warp ลงไป ห้องสมุดของเราสามารถทำซ้ำหรือเล่นภาพอีกครั้งด้วยเอฟเฟกส์ Warp โดยเราสามารถเปิดใช้ฟีเจอร์นี้โดยการตั้งค่า AllowWarpRepaint flag เมื่อเปิดไฟล์ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-1.cs" >}}

ผลลัพธ์:
![Aspose.PSD for .NET ผลลัพธ์ Warp ที่ 1](warp1.png)

นอกจากการเล่นเอฟเฟกส์ Warp สำหรับ SmartLayers ที่เรามีอยู่ ห้องสมุดของเรายังสนับสนุนเอฟเฟกส์ Warp สำหรับ TextLayers การซึ่งรหัสการสร้างยังคงเหมือนเดิม โดยความแตกต่างเพียงอยู่ในชื่อไฟล์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-2.cs" >}}

ผลลัพธ์:
![Aspose.PSD for .NET ผลลัพธ์ Warp ที่ 2](warp2.png)

**! โน้ต:** ในปัจจุบัน, ห้องสมุดของเราสนับสนุนการเล่นทั้ง Custom Warp (ที่ผู้ใช้ควบคุมจุดตะกร้า) และทุกประเภทของ Warp มาตรฐาน

## **ส่วนที่ 2 – การปรับเปลี่ยนเอฟเฟกส์ Warp**

ห้องสมุดของเราช่วยให้คุณไม่เพียงแค่ทำซ้ำแต่ยังสามารถปรับเปลี่ยน (เพิ่ม) เอฟเฟกส์ Warp ได้อีกด้วย<br>
การปรับเปลี่ยนนี้สะดวกผ่านคุณสมบัติของคลาส **WarpParams**

| **คุณสมบัติ**  | **รายละเอียด**                                                         | 
|:--------------|:---------------------------------------------------------------------------|
| Bounds        | คืนค่าของขอบของภาพที่ถูกเล่น                                 |
| MeshPoints    | อาร์เรย์ของจุด โดยทุกจุดแทนจุดสมองของตะกร้าเอฟเฟค                   |
| Value         | ค่าของเอฟเฟค Warp สำหรับเอฟเฟคที่ไม่ใช่ Custom                   |
| WarpRotates   | การแบ่งกลุ่มที่กำหนดทิศทางของเอฟเฟคที่ไม่ใช่ Custom               |
| WarpStyles    | การแบ่งกลุ่มที่กำหนดประเภทของเอฟเฟค Warp                          |

ตัวอย่างโค้ดด้านล่างแสดงวิธีการกำหนดประเภทของเอฟเฟค Warp สำหรับ Smart Layer และปรับประเภทและความเดือดเด็ดของการบิดเอฟเฟค

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-3.cs" >}}

ผลลัพธ์:
![Aspose.PSD for .NET ผลลัพธ์ Warp ที่ 3](warp3.png)

## **ส่วนที่ 3 – การเพิ่มเอฟเฟกส์ Warp**

ตัวอย่างโค้ดด้านล่างแสดงวิธีการเพิ่มเอฟเฟกส์ Warp มาตรฐานไปยัง Smart Layer

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-4.cs" >}}

ผลลัพธ์:
![Aspose.PSD for .NET ผลลัพธ์ Warp ที่ 4](warp4.png)

ตัวอย่างโค้ดด้านล่างแสดงวิธีการเพิ่มเอฟเฟกส์ Warp ที่กำหนดเองไปยัง Smart Layer
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

ผลลัพธ์:
![Aspose.PSD for .NET ผลลัพธ์ Warp ที่ 5](warp5.png)

ตัวอย่างโค้ดด้านล่างแสดงวิธีการเพิ่มเอฟเฟกส์ Warp ไปยัง Text Layer
**! โน้ต:** ตามมาตรฐานของ Photoshop, เอฟเฟกส์ Warp สำหรับ Text Layers มักจะถูกจำกัดไปยังประเภทมาตรฐาน เรายังสนับสนุนการใช้สองประเภทของเอฟเฟกส์ Warp โปรดทราบว่าไฟล์เหล่านี้อาจจะไม่สมบูรณ์แบบกับ Photoshop

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

ผลลัพธ์:
![Aspose.PSD for .NET ผลลัพธ์ Warp ที่ 6](warp6.png)

เราเรื่อยไปปรับปรุงและขยายความสามารถของเอฟเฟกส์ Warp ของเรา โฟกัสที่การเพิ่มความเร็ว คุณภาพ และฟังก์ชันที่รองรับ อยู่เสมอ อยู่รอคอยกับการอัพเดทรายเดือนของเราเพื่อสิ่งใหม่ล่าสุด<br>ทีม Aspose.PSD ของคุณ
