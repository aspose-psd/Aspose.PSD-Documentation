---
title: การใช้งานฟิลเตอร์มีเดียนและวีเนอร์
type: docs
weight: 10
url: /th/net/applying-median-and-wiener-filters/
---

## **การใช้งานฟิลเตอร์มีเดียนและวีเนอร์**
ฟิลเตอร์มีเดียนเป็นเทคนิคการกรองดิจิตัลที่ไม่เช่นต่อกัน ที่ใช้บ่อยเพื่อล้างเสียง การลดรบกวนแบบนี้เป็นขั้นตอนการประมวลผลก่อนที่จะได้ผลลัพธ์การประมวลผลในภายหลังดีขึ้น ฟิลเตอร์วีเนอร์เป็นฟิลเตอร์เชิงเส้นที่ต่ำที่สุดใน MSE(mean squared error) สำหรับภาพที่ถูกทำลายด้วยเสียงส่วนเพิ่มและคล้ายๆกัน โดยใช้ Aspose.PSD สำหรับการพัฒนา API สำหรับ .NET นักพัฒนาสามารถใช้ฟิลเตอร์มีเดียนเพื่อขจัดเสียงรบกวนในภาพและสามารถใช้ฟิลเตอร์วีเนอร์กาวส์บนภาพ บทความนี้สาธิตวิธีที่ฟิลเตอร์มีเดียนและฟิลเตอร์วีเนอร์กาวส์สามารถใช้บนภาพได้

### **การใช้งานฟิลเตอร์มีเดียน**
Aspose.PSD มีคลาส [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) เพื่อใช้ฟิลเตอร์บน [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) ชิ้นส่วนโค้ดด้านล่างแสดงถึงวิธีการใช้ฟิลเตอร์มีเดียนกับภาพราสเตอร์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **การใช้งานฟิลเตอร์วีเนอร์กาวส์**
Aspose.PSD มีคลาส [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) เพื่อใช้ฟิลเตอร์บน [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) ชิ้นส่วนโค้ดด้านล่างแสดงถึงวิธีการใช้ฟิลเตอร์วีเนอร์กาวส์กับภาพราสเตอร์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **การใช้งานฟิลเตอร์วีเนอร์กาวส์สำหรับภาพสี**
Aspose.PSD มีคลาส [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)สำหรับภาพสีด้วย ชิ้นส่วนโค้ดด้านล่างแสดงถึงวิธีการใช้ฟิลเตอร์วีเนอร์กาวส์กับภาพสี

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **การใช้งานฟิลเตอร์วีเนอร์ของการเคลื่อนไหว**
Aspose.PSD มีคลาส [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd/imagefilters.filteroptions/motionwienerfilteroptions) เป็นการใช้ฟิลเตอร์บน [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) ชิ้นส่วนโค้ดด้านล่างแสดงถึงวิธีการใช้ฟิลเตอร์วีเนอร์ของการเคลื่อนไหวกับภาพราสเตอร์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **ใช้ฟิลเตอร์การแก้ไขบนภาพ**
บทความนี้สาธิตการใช้งาน Aspose.PSD สำหรับ .NET เพื่อประมวลผลภาพด้วยฟิลเตอร์การแก้ไข  API Aspose.PSD ได้เปิดเผยวิธีการใช้งานที่มีประสิทธิภาพและใช้งานง่ายเพื่อบรรลุจุดมุ่งนี้ Aspose.PSD สำหรับ .NET ได้เปิดเผยคลาส [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) และ [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) สำหรับกรอง คลาส BilateralSmoothingFilterOptions ต้องการจำนวนเต็มเป็นพารามิเตอร์ ขั้นตอนในการปฏิบัติการ  Resize  ง่ายๆ คือดังนี้:

1. โหลดภาพโดยใช้วิธีการโรงงาน Load ที่เปิดเผยโดยคลาส Image.
1. แปลงภาพเป็น RasterImage.
1. สร้างอินสแตนซ์ของคลาส BilateralSmoothingFilterOptions และ SharpenFilterOptions.
1. เรียกใช้วิธี [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) โดยระบุตารางเป็นขอบของภาพ และอินสแตนซ์คลาส BilateralSmoothingFilterOptions.
1. เรียกใช้ [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) โดยระบุตารางเป็นขอบของภาพ และอินสแตนซ์คลาส SharpenFilterOptions.
1. ปรับความคมชัด
1. ตั้งค่าความสว่าง
1. บันทึกผลลัพธ์


## **ใช้วิธีการคำนวณของบรัดลีย์**
การกำหนดค่าโค้งสะพรั่งใช้ในแอปพลิเคชันกราฟิก จุดมุ่งหลักของการกำหนดค่าโค้งในภาพคือการจำแนกพิกเซลเป็น "มืด" หรือ "สว่าง" Aspose.PSD API ช่วยให้คุณใช้วิธีการคำนวณบรัดลีย์ขณะที่แปลงภาพ ชิ้นส่วนโค้ดด้านล่างแสดงวิธีการกำหนดค่าค่าโค้งแล้วเรียกใช้วิธีการคำนวณบรัดลีย์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
