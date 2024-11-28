---
title: การใช้ไฟล์ PSD เป็นเทมเพลตสำหรับออโตเมชัน - กรณีนามบัตรธุรกิจ
type: docs
weight: 10
url: /th/net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **ภาพรวม**
บทความนี้อธิบายกรณีที่ใช้บ่อยเมื่อคุณต้องการอัปเดตเลเยอร์บางส่วนใน [ไฟล์ PSD](https://wiki.fileformat.com/image/psd/) โดยโปรแกรมอย่างสร้างเชิงลักษณะเทมเพลตที่ทราบ ซึ่งสามารถใช้สร้างนามบัตรขนาดใหญ่สำหรับผู้คนต่างๆ (กรณีนามบัตรธุรกิจ) หรือคุณอาจต้องการแปลงไฟล์ PSD เป็นภาษาต่างๆ พร้อมทำการแทนที่วัสดุกราฟิกบางส่วนในนั้น

หลังจากที่อ่านบทความนี้คุณจะทราบได้ว่าคุณสามารถทำดังนี้:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **กรณีง่ายๆ**
ตัวอย่างเช่น คุณมีเทมเพลต PSD บางชิ้นที่มีชื่อเลเยอร์ทราบเลย ดังนั้นคุณจำเป็นต้องเปลี่ยน อัปเดต หรือแทนที่เลเยอร์ PSD ผ่าน C# ก่อนอื่นคุณต้องเปิดไฟล์เทมเพลตด้วย Aspose.PSD

วิธีเปิดไฟล์ PSD ผ่าน C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)



จากนั้นเราจำเป็นต้องค้นหาเลเยอร์ที่ต้องการแทนที่โดยชื่อของมัน นี่คือการดำเนินการอย่างง่ายสำหรับนี้

วิธีค้นหาเลเยอร์ในไฟล์ PSD โดยชื่อของมัน

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



เมื่อค้นพบเลเยอร์เราสามารถอัปเดตมันได้ในวิธีการทั่วไป โดยใช้ [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

วิธีวาดบนเลเยอร์ PSD Graphics

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

ในกรณีนี้เราวาดรูปภาพแบบใหม่ที่โหลดมา [ไฟล์ PNG](https://wiki.fileformat.com/image/png/) บนเลเยอร์ PSD ที่มีอยู่ เพื่อที่ข้อมูลเก่าจะหายไปในไฟล์ใหม่

แต่ถ้าเราต้องการอัปเดตข้อความอีกด้วย? กระบวนการจะคล้ายกัน ค้นหา [Text Layer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) โดยชื่อของมันแล้วเราก็อัปเดตเลเยอร์ข้อความของไฟล์ Photoshop โดยโปรแกรมมาตามนี้

วิธีอัปเดตเลเยอร์ข้อความใน Photoshop โดยใช้ C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



สุดท้ายเราต้องบันทึกการเปลี่ยนแปลงของเรา:

วิธีบันทึกไฟล์ PSD ที่เปลี่ยนแปลงโดยใช้ [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



ภาพผลลัพธ์:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **กรณีที่ซับซ้อนพร้อมลักษณะเพิ่มเติม**
ข้างต้นเราแสดงวิธีที่ง่ายที่สุดในการแทนที่ภาพในเลเยอร์ของไฟล์ PSD

แต่ Aspose.PSD สามารถมอบคุณสมบัติเพิ่มเติมที่ซับซ้อนมากขึ้น เช่น เพิ่มเลเยอร์ใหม่, ลบเลเยอร์เก่า และอัปเดตเลเยอร์ข้อความโดยใช้อัตราต่างๆในข้อความหลายบรรทัด

เราสามารถค้นหา [Layer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) ที่ต้องการแทนที่ จากนั้นเราค้นพบดัชนีของมันในรายการเลเยอร์ ลบลง และแทนที่ด้วยเลเยอร์ใหม่หลังจากสร้างมันจาก [ไฟล์ Jpeg](https://wiki.fileformat.com/image/jpeg/) ไปยังสถานที่เดียวกัน

สร้างเลเยอร์ใหม่จากไฟล์และแทรกไปยังภาพ PSD โดยใช้ [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



ที่สุดของตัวอย่างโค้ดในไฟล์นี้ เราสร้างรายการเลเยอร์ใหม่และบันทึกไฟล์เลเยอร์ใหม่ไปยังภาพ PSD

วิธีคัดลอกคุณสมบัติเลเยอร์ของ [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



และสุดท้ายเราจำเป็นที่จะอัปเดตเลเยอร์ข้อความในภาพ PSD ที่มีโดย C# Aspose.PSD รองรับการอัปเดตของ TextLayer โดยต่อเนื่อง

การกำหนด Properties ของ [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage) Layer

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



เป็นผลลัพธ์เราได้เปลี่ยนแปลงเทมเพลต PSD ผ่านโค้ดด้วยเลเยอร์ใหม่จากไฟล์ Jpeg, Png, J2k, Bmp, Gif, หรือไฟล์ Tiff และข้อความหลายบรรทัด [ซึ่งมีสไตล์ต่างๆ](https://gist.github.com/aspose-com-gists/8a4d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) ในแต่ละแถว

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
