---
title: การใส่ Vector Mask ในเลเยอร์
type: docs
weight: 10
url: /th/net/layer-vector-mask/
---

## **ภาพรวมของ Vector Mask ในเลเยอร์**
Vector mask เป็นเส้นทางที่ไม่ขึ้นอยู่กับความละเอียดที่ตัดข้อความของเลเยอร์ออกไป การใส่ vector mask มักจะแม่นยำกว่าการสร้างด้วยเครื่องมือที่ใช้ pixel คุณสร้าง vector mask ด้วยเครื่องมือด้ามหรือรูปร่าง

Aspose.PSD รองรับการเรนเดอร์และการใช้ vector mask คุณสามารถแก้ไข vector mask โดยการแก้ไขของ Vector Paths

## **เส้นทาง Vector ใน Aspose.PSD**
การเข้าถึงเส้นทาง vector ใน Aspose.PSD ได้ผ่าน [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) และ [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) ที่เป็นคลาสลูกของ [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource)

![todo:image_alt_text](layer-vector-mask_0.png)

## **วิธีแก้ไขเส้นทาง vector?**
### **โครงสร้างเส้นทาง vector**
โครงสร้างหลักในการจัดการเส้นทางคือ [VectorPathRecord.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord) แต่เพื่อความสะดวกของคุณ โครงสร้างต่อไปนี้ถูกแนะนำ

สำหรับการแก้ไขเส้นทาง vector อย่างสะดวก คุณควรใช้คลาส [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) ซึ่งมีเมทอดสำหรับการแก้ไขข้อมูล vector ในทรัพยากรที่ได้มาจาก VectorPathDataResource

เริ่มต้นด้วยการสร้างออบเจ็กต์ของประเภท VectorPath

สำหรับความสะดวก คุณสามารถใช้เมทอดแบบสแตติก [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) มันจะค้นหาทรัพยากร vector ในเลเยอร์นำเข้าและสร้างออบเจ็กต์ VectorPath จากนั้น

หลังจากการแก้ไขทั้งหมด คุณสามารถปรับใช้ออบเจ็กต์ VectorPath กับการเปลี่ยนแปลงกลับไปยังเลเยอร์โดยใช้เมทอดแบบสแตติก [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

ประเภท VectorPath มีรายการของ [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) องค์ประกอบและระบุภาพเวกเตอร์ทั้งหมดที่สามารถประกอบด้วยรูปร่างหรือหลายรูปร่าง

![todo:image_alt_text](layer-vector-mask_1.png)

แต่ละ PathShape เป็นรูปร่างเวกเตอร์ที่ประกอบด้วยเซ็ตอิสระของจุดเบเซียร์

จุดเบเซียร์คือวัตถุของประเภท [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) ซึ่งพื้นฐานของรูปตัวลูกปัจจุบัน

![todo:image_alt_text](layer-vector-mask_2.png)

ตัวอย่างโค้ดต่อไปนี้แสดงถึงวิธีเข้าถึงเรขาภิคตาและจุด

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **วิธีสร้างรูปร่าง?**
เพื่อแก้ไขรูปร่าง ต้องเรียกมาร์กเจ็ตที่มีอยู่จาก [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) ลิสต์ หรือเพิ่มรูปร่างใหม่โดยการสร้างอินสแตนซ์ [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) และเพิ่มลงใน [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) ลิสต์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **วิธีเพิ่มจุด (ข้อความ)?**
คุณสามารถจัดการจุดของรูปร่างเป็นสมาชิกของรายการปกติโดยใช้คุณสมบัติ PathShape.Points เช่น คุณสามารถเพิ่มจุดรูปร่าง:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}

BezierKnot ประกอบด้วยจุด Anchor และจุด Control สองประการ

![todo:image_alt_text](layer-vector-mask_3.png)

ถ้าจุด Anchor และจุด Control มีค่าเดียวกัน แล้วโหนดนั้นจะมีมุมแห้ง

เพื่อเปลี่ยนตำแหน่งจุด Anchor พร้อมกับจุดควบคุม (คล้ายกับวิธีที่เกิดขึ้นใน Photoshop) BezierKnot มีเมทอด Shift

ตัวอย่างโค้ดต่อไปนี้แสดงการเลื่อนเบเซียร์น็อตทั้งหมดขึ้นตามแนวตั้งโดยพิกยอด Y

คุณสามารถจัดการจุดของรูปร่างเป็นสมาชิกของรายการปกติโดยใช้คุณสมบัติ PathShape.Points เช่น คุณสามารถเพิ่มจุดรูปร่าง:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}

## **คุณสมบัติของ PathShape**
การแก้ไข PathShape ไม่จำกัดในการแก้ไขหลัก ประเภทนี้ยังมีคุณสมบัติอื่น ๆ อีก

### **PathOperations (การปฏิบัติ Boolean)**
คุณสมบัติ [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) เป็นการปฏิบัติบูลีเลียน การเปลี่ยนค่าในการกำหนดว่ารูปร่างหลาย ๆ ชิ้นถูกผสมเข้าด้วยกันอย่างไร

มีค่าผลเลือกต่อไปนี้:

- 0 = ไม่รวมรูปร่างทับกัน (การปฏิบัติ XOR)
- 1 = รวมรูปร่าง (การปฏิบัติ OR)
- 2 = ลบรูปร่างด้านหน้า (การปฏิบัติ NOT)
- 3 = ตัดพื้นที่รูปร่าง (การปฏิบัติ AND)

![todo:image_alt_text](layer-vector-mask_4.png)

### **คุณสมบัติ IsClosed**
นอกจากนี้ ใช้อินสแตนซ์ของคุณสมบัติ PathShape.IsClosed เราสามารถกำหนดว่าจุดเริ่มและจุดสุดท้ายของรูปร่างเชื่อมกันหรือไม่

| **รูปร่างที่ปิด** | **รูปร่างที่เปิด** |
| :- | :- |
| ![todo:image_alt_text](layer-vector-mask_5.png) | ![todo:image_alt_text](layer-vector-mask_6. png) |

### **FillColor Property**
รูปร่างใดก็สามารถมีสีของตัวเอง ดังนั้นคุณสามารถเปลี่ยนสีสตรีมทั้งหมดของเส้นทางเวกเตอร์ด้วยคุณสมบัติ VectorPath.FillColor

คุณสามารถจัดการจุดของรูปร่างเป็นสมาชิกของรายการปกติโดยใช้คุณสมบัติ PathShape.Points เช่น คุณสามารถเพิ่มจุดรูปร่าง:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}

## **ที่นี่คุณจะพบรหัสต้นฉบับของ VectorDataProvider และคลาสที่เกี่ยวข้อง:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
