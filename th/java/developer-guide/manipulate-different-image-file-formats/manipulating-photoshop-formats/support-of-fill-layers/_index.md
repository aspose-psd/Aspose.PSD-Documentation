---
title: การสนับสนุน Fill Layers
type: docs
weight: 50
url: /th/java/support-of-fill-layers/
---


## **การสนับสนุน Fill Layers ด้วยการเติมสี**
บทความนี้สาธิตวิธีการเติมเลเยอร์ PSD ด้วยสี โปรดใช้ Aspose.PSD.FileFormats.Psd.Layers.FillLayer เพื่อเพิ่มสีในเลเยอร์ PSD ซึ่งโค้ดตัวอย่างด้านล่างโหลดไฟล์ PSD, เข้าถึงคลาส Filllayer และตั้งค่าสีโดยใช้คุณสมบัติ FillLayer.FillSettings

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **การสนับสนุน Fill Layers ด้วยการเติมแบบ Gradient**
บทความนี้สาธิตการใช้งานการเติมแบบ Gradient เพื่อเติม PSD layer  Aspose.PSD APIs ประกาศเมทอดที่มีประสิทธิภาพและใช้ง่ายเพื่อบรรลุวัตถุประสงค์นี้ Aspose.PSD ได้เปิดเผยคลาส GradientColorPoint และ GradientTransparencyPoint เพื่อเพิ่มเอฟเฟกต์ Gradient เข้าไปในเลเยอร์

ขั้นตอนในการเติม PSD layer ด้วยการเติมแบบ Gradient ง่ายมากดังต่อไปนี้:

- โหลดไฟล์ PSD เป็นภาพโดยใช้เมทอด Load ที่เปิดเผยโดย Image class
- กำหนดค่าคุณสมบัติของออบเจกต์ FillLayer
- สร้างรายการ ColorPoints พร้อมกับสีที่ต้องการและตำแหน่งของสี
- สร้างรายการ transparencyPoints พร้อมกับความทึกทึนที่ต้องการและตำแหน่งของจุดความทึกทึน
- เรียกเมทอด FillLayer.Update
- บันทึกผลลัพธ์

โค้ดตัวอย่างด้านล่างแสดงวิธีการเพิ่ม Gradient fill เข้าไปในเลเยอร์ PSD

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **เอฟเฟกต์ Stroke ด้วยการเติมสี**
บทความนี้สาธิตวิธีการสร้างเอฟเฟกต์ Stroke ด้วยการเติมสี การใช้เอฟเฟกต์ Stroke เพื่อเพิ่มเส้นและเส้นขอบเข้าไปในเลเยอร์และรูปทรง สามารถใช้สร้างเส้นสีทึบ, เฉดเทาสีสวยงาม, และขอบลวดลาม

ขั้นตอนในการสร้างเอฟเฟกต์ Stroke ด้วยการเติมสี ง่ายมากดังต่อไปนี้:

- กำหนดคุณสมบัติ LoadEffectsResource
- โหลดไฟล์ PSD เป็นภาพโดยใช้เมทอด Load ที่เปิดเผยโดย Image class และกำหนด PsdLoadOptions
- กำหนดค่าคุณสมบัติของ ColorFillSetting
- บันทึกผลลัพธ์

โค้ดตัวอย่างด้านล่างแสดงวิธีการสร้างเอฟเฟกต์ Stroke ด้วยการเติมสี

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}




