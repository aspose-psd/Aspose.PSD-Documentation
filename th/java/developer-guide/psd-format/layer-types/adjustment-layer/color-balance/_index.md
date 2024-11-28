---
title: การปรับความสมดุลของสีด้วยชั้นการปรับปริมาณสี
type: docs
weight: 30
url: /th/java/layer-types/adjustment-layer/color-balance/
---

# การทำงานกับชั้นการปรับปริมาณสี Color Balance ใน Photoshop ด้วย Java

ในบทความนี้เราจะ **ปรับความสมดุลของสีในรูปภาพ** ในรูปแบบไฟล์ PSD ด้วย Java  เราจะใช้ไลบรารีพิเศษที่เรียกว่า Aspose.PSD สำหรับ Java ซึ่งเป็นอุปกรณ์เครื่องมือสำหรับการจัดการเอกสารของ Photoshop

โดยเนื่องจากไลบรารีนี้ทำงานกับรูปแบบไฟล์ PSD มีเกือยไว้เกือบ [ทุกคุณสมบัติ](https://docs.aspose.com/psd/java/features/) ที่มีในตัวดูแก้ไขของ Photoshop และชั้นปรับปริมาณสี Color Balance ซึ่งเหมาะสำหรับงานนี้อย่างแท้จริง

ชั้นการปรับปริมาสี Color Balance ทำให้เป็นไปได้ในการเปลี่ยนสมดุลระหว่างสีหลัก (RGB) และสีถอย (CMY) สำหรับเงา กลางแสง และไฮไลต์อย่างง่ายและรวดเร็ว

## ปรับความสมดุลของสี

ตามที่กล่าวมาชั้นการปรับความสี Color Balance ใน Aspose.PSD สำหรับ Java ก็คือ **เครื่องชช่นระหว่างสีหลักและสีถอย** หมายควา่ามีสามสเกลสำหรับแต่ละคู่สี ( Cyan/Red, Magenta/Green, Yellow/Blue) ความเข้มของสีที่เฉพาะเจาลจะเพิ่มขึ้นถ้าค่าเคลื่อนที่ไปในทิศทางนั้น หรือทวีคลิกรบกัน  รองลัสได้วาย่สามคู่ถอยร้ะเกี่ยจ่างสุนความยืดหยุ่นของการปรับแบบนี้

ดังนั้น ให้เรานำความรู้นี้ไปใช้ในความปฏิบัติ เช่นเลือกภาพหนึ่งที่เป็นภาพหน้าผุ้หญิงสีแดง (b) ใบหน้าดูมีสีแดงเป็นอย่างมากและเราจะแก้ไขให้ **เพิ่มชั้นการปรับปริมาสี Color Balance** เพื่อลือสีแดงลดลงและเพิ่มซี่ยาน เบสิค (a) เพื่อให้ขจาหน้าดูสมเหตุ(c) อีกครั้ง, มีการทำงานเกพ่ามากในภาพนี้ แต่ภายในบทความนี้นั้น นังนี้ที่เราจะทำ

![ตัวอย่างชั้นการปรับปริมาสี Color Balance](color-balance-adjustment-layer-example-figure-1.png) API ของชั้นปรับปริมาสี Color Baalance มีการออกแบบเนียน ดังนั้น, [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) คือคลาสที่เราต้องการ ขั้นแรกคือ รักษาความสว่างเพราะมีการปิดทิต่างหจักค่า เมื่อนำไปใช้ และเพิ่มสีเขียวและขนาดสีเหลืองมากขึ้นให้เหลือสามโดยใช้เมทคอดที่เกี่ยมชื่อพิเชิลของพื้นที่ของชุลลของสีร่วาระและธูงต向น้รและบลูไปแล้วเสHHHHHHHHHasasmh中

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

ตอนนี้เราได้ภาพตามที่ต้องการแล้วค้าา ง่ายและสะดวก เขา่ใช่ไหม?

โปรดสังเกคว่า _ค่าของแต่ละคู่สีิตรกุหยงตรีร่สามจป้าแก้จิข่ยเวนรระหรี่จกวนัการปพริทิสัิบเม้จสาแกี่จเดิั่ีาีการ์แยร้เหส้รฟ่ะซีปดเีขยะิทิวกิทิ_

อ้างอิงตามโศรการของเราเพื่อเรียนรู้รายละเอียดทางเทคนิคเพิิ่มเติมเกี่ยวกับ [ชั้นปรับปริมาสี Color Balance](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## สรุป

ในบทความนี้ เราได้พิจารณาว่าการปรับความสมดุลของสีของภาพในลักษณะที่เป็นโปรแกรมใน Java โดยใช้ไลบรารี Aspose.PSD สำหรับ Java  ไลบรารีนี้มี API ที่มีความสมบูรณ์ถึงเพิ้มือในการทำงานกับชั้นปรับปริมาหีรได้อย่างประณีแบบในเอกสารของ Photoshop
