---
title: การปรับแต่งเลเยอร์การปรับสีขาวดำ
type: docs
weight: 30
url: /th/java/layer-types/adjustment-layer/levels/
---

## การทำงานกับเลเยอร์การปรับ Photoshop Levels ใน Java

ในบทความนี้เราจะเรียนรู้วิธีการปรับช่วงโทนและสมดุลของสีในรูปถ่ายในรูปแบบไฟล์ [PSD](/th/psd/java/psd-format/) โปรแกรมเมอร์ตามต้องการใน Java โดยไม่ใช้ตัวแก้ไขรูปภาพของ Adobe® Photoshop® เอง แต่ใช้ไลบรารี Aspose.PSD สำหรับ Java ทำงานอย่างเองเพื่อจัดการเอกสาร Photoshop

แม้ว่า Aspose.PSD สำหรับ Java สนับสนุน [เครื่องมือในการแก้ไขรูปภาพ](/th/psd/java/manipulating-images/) มากพอสำหรับที่เราต้องการ ในบทความนี้เราจะ **เลือกใช้ API เลเยอร์การปรับระดับ Levels** ซึ่งเป็นหนึ่งในวิธีที่ง่ายและรวดเร็วที่สุดในการทำงาน

## ภาพรวมของ API

การใช้งานปัจจุบัน (20.6 ในขณะที่เขียน) ของ Levels adjustment layer API **สนับสนุนคุณสมบัติหลักของ Photoshop Levels ทั้งหมด** นั่นคือการปรับระดับ input และ output สำหรับช่องโคมโพรง (RGB) และสำหรับแต่ละช่องสีหลัก (ช่องสีแดง เขียว และน้ำเงิน)

API ของ Levels adjustment layer เป็นเรื่องง่ายตรงไปตรงมา คลาส [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) เป็นจุดเข้าทาง Levels adjustment มีเมธอดหลายตัวสำหรับเข้าถึงช่องสี: getMasterChannel และ getChannel(int) ทั้งสองเมธอดส่งคืน [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) ที่มีคุณสมบัติที่สอดคล้องกันสำหรับการจัดการ input และ output Levels ความแตกต่างกันคือ getMasterChannel ใช้ในการปรับช่องสีรวม (RGB) ในขณะที่ getChannel เข้าถึงช่องสีเฉพาะ (แดง เขียว หรือน้ำเงิน) โดยดัชนีของมัน

## ความเข้ากันได้กับโหมดสี

ควรทราบว่า Layers adjustment layer **เข้ากันได้กับส่วนใหญ่ของโหมดสี** ตาม Photoshop Levels ดังนั้นสามารถปรับระดับ Levels สำหรับภาพในโหมด Grayscale (ช่องสีเทา) RGB (RGB แดง เขียว และน้ำเงิน) CMYK (CMYK ไซยาน แม็จทา ชมพ์ และดำ) Duotone (ช่องสีเที่ยงคืน) และ LAB (ความสว่าง a และ b)

## ปรับช่องโทน

เพื่อง่าย การปรับการตั้งค่าโทนเกิดจาการนำภาพมาตีเตอร์ร่างของเงาและไฮไลท์เพื่อกระจายมิดโทนได้ดีขึ้น โดยทั่วไป **มันทำให้ภาพดูสีเข้มขึ้น** ถ้าทำถูกต้อง ตัวอย่างเช่น เราจะนำรูปภาพของสุนัข (b) และปรับช่องโทนของมัน (a - ภาพหน้าจอถูกจับจากหน้าต่าง Photoshop Levels เพื่อความชัดเจน) เพื่อให้ภาพดูเข้มสีขึ้น (c)

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![ภาพของเลเยอร์ช่องโทน 1](levels-adjustment-figure-1.png)|

เพื่อ **ปรับช่องโทนโดยรวมของภาพ** จำเป็นต้องตั้งค่า input Levels ของช่องมาสเตอร์:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

จำเป็นต้องจำใสไว้ว่า input Levels ควรอยู่ในช่วง 0 ถึง 253 สำหรับเงา 9.99 ถึง 0.01 สำหรับมิดโทนและ 2 ถึง 255 สำหรับไฮไลท์ ช่วงของ output Levels ต้องอยู่ระหว่าง 0 ถึง 255

ต้องการตัวอย่างเพิ่มเติมไหม? คุณสามารถหาออกมาได้ที่ [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) และใน [ฐานความรู้](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers)

## สรุป

สรุปว่า Aspose.PSD สำหรับ Java มี API ที่สะดวกและง่ายสำหรับการเปลี่ยนแปลงช่วงโทนและสมดุลของสีในภาพที่เข้ากันได้กับโหมดสีมากที่สุด เลเยอร์การปรับระดับ Levels ของไลบรารีมีลักษณะเหมือนกับ Photoshop Levels ดังนั้นง่ายต่อการเริ่มต้นแม้ว่าคุณไม่เคยใช้ไลบรารีก่อนหน้านี้
