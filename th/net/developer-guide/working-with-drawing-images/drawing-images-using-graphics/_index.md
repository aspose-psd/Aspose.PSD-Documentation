---
title: การวาดรูปภาพโดยใช้กราฟิก
type: docs
weight: 20
url: /th/net/drawing-images-using-graphics/
---

## **การวาดรูปภาพโดยใช้กราฟิก**
ด้วยไลบรารี Aspose.PSD คุณสามารถวาดรูปร่างพื้นฐาน เช่น เส้น, สี่เหลี่ยม และวงกลม รวมถึงรูปร่างที่ซับซ้อน เช่น รูปหลายเหลี่ยม, เส้นโค้ง, ภาพรูปวงกลมและรูปร่างเบเซียร์ ไลบรารี Aspose.PSD สร้างรูปร่างเหล่านี้โดยใช้คลาส [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ซึ่งตั้งอยู่ในเนมสเปซ Aspose.PSD ออบเจ็กต์ Graphics รับผิดชอบในการดำเนินการวาดต่าง ๆ บนภาพ, ซึ่งจะเปลี่ยนแปลงพื้นผิวของภาพ คลาส [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ใช้อ็อบเจกต์ช่วยเหลือหลายอย่างเพื่อเสริมสร้างรูปร่าง:

·         Pens, ใช้สำหรับวาดเส้น, ขอบรูปร่าง หรือเรนเดอร์ภาพเรขาคณิ.

·         Brushes, ใช้สำหรับกำหนดว่าพื้นที่จะถูกเติม.

·         Fonts, ใช้สำหรับกำหนดรูปร่างของตัวอักษรข้อความ.
### **การวาดด้วยคลาส Graphics**
ด้านล่างนี้เป็นตัวอย่างโค้ดที่แสดงการใช้คลาส [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ตัวอย่างโค้ดมีการแบ่งเป็นส่วนต่าง ๆ เพื่อให้ง่ายต่อการติดตาม ขั้นตอนต่อไป เป็นตัวอย่างโชว์ว่าจะทำอย่างไร:

1. สร้างภาพ.
1. สร้างและกำหนดค่าให้กับอ็อบเจกต์ Graphics.
1. เคลียร์พื้นผิว.
1. วาดวงกลม.
1. วาดรูปหลายเหลี่ยมและบันทึกภาพ.
### **ตัวอย่างการเขียนโปรแกรม**
#### **การสร้างภาพ**
เริ่มต้นด้วยการสร้างภาพโดยใช้วิธีใดก็ได้ที่อธิบายไว้ในการสร้างไฟล์.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **สร้างและกำหนดค่าให้กับอ็อบเจกต์ Graphics**
จากนั้น สร้างและกำหนดค่าให้กับอ็อบเจกต์ Graphics โดยส่งอ็อบเจกต์ภาพไปยังคอนสตรักเตอร์ของมัน.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **เคลียร์พื้นผิว**
เคลียร์พื้นผิว Graphics โดยเรียก Clear ของคลาส [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) และส่งสีเป็นพารามิเตอร์ วิธีนี้จะเติมพื้นผิว Graphics ด้วยสีที่ถูกส่งไปเป็นอาร์กิวเมนท์.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **วาดวงกลม**
คุณอาจสังเกตว่า คลาส [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ได้เปิดเผยเมทอดหลายรูปแบบเพื่อวาดและเติมรูปร่าง คุณจะพบรายการเต็มของเมทอดทั้งหมดใน Aspose.PSD for .NET API Reference มีเวอร์ชันล่วงหน้าของเมทอด DrawEllipse ที่ถูกเปิดเผยโดยคลาส Graphics มีหลายเวอร์ชันที่ยืดหยุ่น ทุกเวอร์ชันต้องการอ็อบเจกต์ Pen เป็นอาร์กิวเมนต์แรก เมื่อส่งพารามิเตอร์ว่างงานคือสี่เหลี่ยมล้อมวงกลม ในตัวอย่างนี้ใช้เวอร์ชันที่ยอมรับอ็อบเจกต์ Rectangle เป็นพารามิเตอร์ที่สองเพื่อวาดวงกลมโดยใช้อ็อบเจกต์ Pen ในสีที่คุณต้องการ.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **วาดรูปหลายเหลี่ยม**
จากนั้น วาดรูปหลายเหลี่ยมโดยใช้ LinearGradientBrush และอาร์เรย์ของจุด คลาส Graphics ได้เผยแพร่เมทอด FillPolygon หลายเวอร์ชัน ทั้งหมดรับอ็อบเจกต์ Brush เป็นอาร์กิวเมนต์แรก กำหนดลักษณะของการเติม อาร์เรย์จุดเป็นอาร์กิวเมนต์ที่สอง โปรดทราบว่าทุกสองจุดติดต่อกันในอาร์เรย์ระบุด้านของรูปหลายเหลี่ยม

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **การวาดรูปภาพโดยใช้กราฟิก: โค้ดเต็ม**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

อ็อบเจกต์ที่สมบูรณ์แบบทั้งหมดที่รวมอยู่ใน IDisposable และเข้าถึงทรัพยากรที่ไม่ได้จัดการอย่างถูกต้องจะถูกสร้างหรือสร้างขึ้นในคำสั่ง Using เพื่อให้แน่ใจว่ามันถูกเก็บอย่างถูกต้อง.
