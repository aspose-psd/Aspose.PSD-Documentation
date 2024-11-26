---
title: การใช้ชั้นปรับแต่งสำหรับการปรับปรุง PSD
weight: 100
type: docs
description: ตัวอย่างการใช้ชั้นปรับแต่งผ่าน Aspose.PSD สำหรับ Java
keywords: [ชั้นปรับแต่ง, การปรับปรุงรูปภาพ, การปรับค่าเส้นโค้ง, การเพิ่มระดับ, การสลับ, ตัวกรองรูปภาพ,  ส่วน API สำหรับ PSD, จาวา, ตัวอย่างโค้ด]
url: th/java/adjustment-layer-enhancement/
---

## **ภาพรวม**

บทความนี้สำรวจวิธีการแก้ไขชั้นปรับแต่งใน Aspose.PSD สำหรับ Java ชั้นปรับแต่งเป็นคุณลักษณะที่มีประสิทธิภาพในการแก้ไขรูปภาพซึ่งช่วยให้คุณสามารถทำการเปลี่ยนแปลงโดยไม่ทำลายรูปภาพของคุณ Aspose.PSD มีชุดคลาสชั้นปรับแต่งที่ครอบคลุมที่คุณสามารถใช้เพื่อปรับเปลี่ยนด้านต่าง ๆ ของรูปภาพ

เพื่อสาธิตการแก้ไขชั้นการปรับแต่ง เราจะให้โค้ดตัวอย่างที่ปรากฏที่ส่วนท้ายของหน้านี้ ทำการโหลดภาพ PSD และปรับแต่งโค้ดอย่างต่างกันบนชั้น

ในโค้ดตัวอย่างต่อไปนี้ เราจะเริ่มด้วยการโหลดภาพ PSD โดยใช้วิธี PsdImage.load() จากนั้นเราตั้งค่าตัวเลือกสำหรับการบันทึกไฟล์ PNG ผลลัพธ์ คลาส PngOptions ช่วยให้เราระบุประเภทสีสำหรับรูปภาพผลลัพธ์

ต่อมาเราวนภูมิภาพสำหรับแต่ละชั้นในภาพ PSD และตรวจสอบประเภทของมันโดยใช้วิธี isAssignable() หากชั้นเป็นประเภทที่กำหนด  เราจะแปลงมันเป็นประเภทนั้นโดยใช้วิธี cast() และปรับการปรับแต่งตามที่ต้องการ เช่น ปรับความสว่างและความคมชัดของ BrightnessContrastLayer ปรับระดับของ LevelsLayer, เพิ่มจุด Curve ใน CurvesLayer และอื่น ๆ

คุณสามารถเพิ่มโค้ดเพื่อปรับเปลี่ยนการปรับแต่งอื่น  ๆ  ให้สอดคล้องกับชั้นต่าง ๆ  Aspose.PSD มีชุดคลาสชั้นปรับแต่งที่หลากหลาย เช่น [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), และอื่น ๆ

สุดท้ายเราบันทึกภาพที่ปรับแต่งแล้วโดยใช้วิธี save() ของคลาส PsdImage

นี้เป็นภาพรวมพื้นฐานของวิธีการแก้ไขชั้นปรับแต่งใน Aspose.PSD สำหรับ Java คุณสามารถปรับแต่งการปรับแต่งตามความต้องการของคุณ และสำรวจตัวเลือกที่หลากหลายที่มีในเอกสาร API

กรุณาตรวจสอบตัวอย่างทั้งหมดด้านล่าง

## **ตัวอย่าง**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
