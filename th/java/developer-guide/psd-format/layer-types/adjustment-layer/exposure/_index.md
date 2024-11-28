---
title: การปรับข้อมูลชั้น Exposure
type: หนังสือ
weight: 30
url: /th/java/layer-types/adjustment-layer/exposure/
---

# การทำงานกับชั้นการปรับข้อมูล Exposure ใน Photoshop ด้วย Java

ในบทความนี้เราจะเสริมชั้นการปรับข้อมูล Exposure เข้ากับเอกสาร Adobe® Photoshop® โดยใช้ Aspose.PSD สำหรับ Java - ไลบรารีการปรับแต่งรูปแบบไฟล์ PSD ด้วยตัวเอง ไลบรารีทำงานได้โดยไม่ต้องติดตั้งโปรแกรมแก้ไข Photoshop เพราะใช้ขั้นตอนประมวลผลรูปภาพของตัวเอง นอกจากนี้เรายังเรียนรู้รายละเอียดที่เกี่ยวข้องกับ API การปรับข้อมูล Exposure ของไลบรารี

## ภาพรวมของ API

ชั้นการปรับข้อมูล Exposure กำหนดผ่านคลาส [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) ซึ่งประกอบด้วยคุณสมบัติต่อไปนี้เพื่อทำงานกับการปรับข้อมูล Exposure:

- กำหนดว่ารูปภาพมีแสงมากเท่าใดโดยการบีบอัดหรือขยายฮิสโตแกรมทั้งหมดเทียบกับสีดำ ดังนั้น มันมีผลต่อส่วนสูงสุด
- ความแตกต่างกันแล้วการปรับแกนที่มีผลต่อแสง
- การปรับแกมมา ช่วยแก้ไขความสว่างของรูปภาพ

## ปรับแต่ง Exposure อย่างถูกต้อง

การปรับ Exposure และคุณสมบัติที่เกี่ยวข้องง่ายเพียงการเปลี่ยนคุณสมบัติของคลาสเท่านั้น ให้เราใช้การปรับข้อมูล Exposure (a) บนภาพที่ถ่ายกลุ่มห้องสมุดที่กำลังเล็กและไม่สามารถมองเห็นได้ใส่ใจสูง (c)

![ตัวอย่างชั้นการปรับข้อมูล Exposure](exposure-adjustment-layer-figure-1.png)

การปรับข้อมูลทั้งหมดด้วยการใช้การปรับแกมมา อย่างไรก็ตาม การปรับ Exposure และ Offset จะได้รับการปรับเพียงน้อย ทุกที่ที่คุณต้องทำคือตั้งค่าค่าที่เหมาะสมให้แก่คุณสมบค่าที่กล่าวถึงแล้ว:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

สังเกตว่า Exposure จะต้องอยู่ในช่วงระหว่าง -20.0 ถึง 20.0, ค่า Offset จะต้องอยู่ในช่วงระหว่าง -0.5 ถึง 0.5 และระยะค่าของการปรับแกมมาจะต้องอยู่ระหว่าง 9.99 และ 0.01

อ้างอิงที่[API ของ ชั้นการปรับข้อมูล Exposure](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) สำหรับรายละเอียดเพิ่มเติม

## สรุป

ในบทความนี้เราได้เรียนรู้วิธีการเพิ่มชั้นการปรับข้อมูล Exposure เข้ากับไฟล์ PSD เพื่อเพิ่มความสว่างของภาพและพิจารณาบางรายละเอียดของ API
