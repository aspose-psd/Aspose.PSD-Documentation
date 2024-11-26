---
title: ชั้นการปรับเส้นโค้ง
type: docs
weight: 30
url: /th/java/layer-types/adjustment-layer/curves/
---

# การทำงานกับชั้นการปรับเส้นโค้งของ Photoshop ใน Java

จุดมุ่งหมายของบทความนี้คือการสาธิตความสามารถของไลบรารี Aspose.PSD สำหรับ Java ขณะ **ทำงานกับชั้นการปรับเส้นโค้ง** ในเอกสารของ Adobe® Photoshop® The library is fully autonomous. ดังนั้น มันทำงานโดยไม่ต้องติดตั้งโปรแกรมแก้ไขภาพ Photoshop ซึ่งสามารถ [ดูรายการความสามารถทั้งหมด](https://docs.aspose.com/psd/java/features/) ได้ในฐานความรู้ของเรา ขอบคุณ สิ่งที่เหลือ กลับมาที่เรื่องเส้นโค้ง

## ภาพรวมของ API

เครื่องมือเส้นโค้งสามารถแสดงในรูปของเส้นทแทงซ้ายขึ้นเหนือมุมขวาของขอบบนและเงาในมุมขวาล่าง

ไลบรารีมี API เพื่อทำงานกับเส้นโค้ง นั้นก็คือ [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer) อย่างไรก็ตาม คลาสนี้มี **วิธีการทำงานสองวิธีที่แตกต่างกันต่างจากกันโดยสิ้นเชิง** เพื่อทำงานกับเส้นโค้ง ดังนั้น สามารถแก้ไขได้ในหนึ่งในสองโหมดได้เท่านั้น:

- ต่อเนื่อง (เส้นโค้งแทนด้วยเส้นทแงด้วยจุด ในสถานที่ค้นงอย)
- ไม่ต่อเนื่อง (เส้นโค้งแทนด้วยเส้นปะปน)

ดังนั้น ไลบรารีมีวิธีการสองวิธีในการแก้ไขเส้นโค้งโดยใช้ [continuous](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) และ [discrete manager](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) ติดต่อในลงไป พวกเราจะอธิบายวิธีการใช้แต่ละอย่างบนตัวอย่างเฉพาะ

## ปรับสีและโทนด้วยระบบจัดการเส้นโค้งต่อเนื่อง

[Curves Continuous Manager](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **กำหนดจุดกำหนดของเส้นโค้งต่อเนื่อง** สำหรับช่องคอมโพสิต (RGB) รวมทั้งสำหรับแต่ละช่องสีที่เฉพาะเจาะจง ในการสาธิต การปรับแต่งของเส้นโค้งบางส่วน (a) จะถูกใช้บนภาพภายในมิถีของวงอัล และจะได้ภาพที่สว่างขึ้นกับสีอบอุ่นมากขึ้น (c):

![Curves Adjustment Layer Figure 1](curves-psd-adjustment-layer-figure-1.png)

เนื่องจากมีผู้จัดการสองคน จำเป็นต้องเลือกเป็นแบบหนึ่งโดยชัดเจน (ผู้จัดการต่อเนื่องในกรณีนี้) ก่อนที่จะเข้าถึง จากนั้น เราสามารถเพิ่มจุดเส้นโค้งโดยตรงที่พิกัดบางตำแหน่งสำหรับช่องสีที่ต้องการ (ช่อง RGB รวมถึงสีแดงและฟ้า ตามลำดับ) เพื่อสร้างรูปร่างของเส้นโค้ง:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

ที่ต้นกันทีคุณละ ค่าพิกัดสูงสุดของจุดจำกัดไว้ที่ประเภทข้อมูล (byte) และมีค่าเท่ากับ 255 (127 สำหรับประเภทที่มีเครื่องหมาย) นอกจากนี้ยังมี[มีวิธีอื่น ๆ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager)ที่คุณสามารถใช้

## ปรับโทนด้วย Curves Discrete Manager

Curves Discrete Manager ยังเป็นทางเลือกอีกเพื่อวางจุดของเส้นโค้ง (เปลี่ยนสีและโทน) แต่ความแตกต่างคือว่าพวกเขาทำในทางที่แตกต่างกัน ต่อซึ่ง **เส้นโค้งประกอบด้วยจุด** หรือจุด (ไม่ใช่เส้นต่อ) สอง ผู้จัดการ **ไม่วางจุดไหน** บนกราฟ แทนที่ **เลื่อนจุดขึ้นหรือลง** ด้วยช่วงค่าระหว่าง 255 และ 0 ตามลำดับ โดยค่าเริ่มต้นของจุดของเส้นโค้งเพิ่มขึ้นตามลำดับเพื่อสร้างสีที่ได้สวมเป็นเส้นโค้งอย่างมีมุมกับ 45 องศา

ดังนั้น โดยควาภิจแล้วง่ายต่อให้รูปสี [Negative (RBG)] ตั้งต้นของ Photoshop (a) และนำมาใช้กับภาพสีเทาของหุบเขา (b) เพื่อเอามาเป็นตัวแทนของภาพแสงที่ตัวเคร่งของหุบเขาปิด (c)

![Curves Adjustment Layer Figure 2](curves-psd-adjustment-layer-figure-2.png)

ก่อนอื่น อย่าลืมเลือกผู้จัดการสอดให้ถูกต้องเพื่อสามารถใช้และจากนั้นตั้งค่าค่าจุดของเส้นโค้งลงมาตามลำดับเริ่มจาก 255 ลงไปจนถึง 0 สำหรับแต่ละจุดของเส้นโค้ง (รวมทั้ง 255 ค่า):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

ผู้จัดการยังมี[มีวิธีการอื่น ๆ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager)เพื่อการจัดการกับเส้นโค้ง

## สรุป

ในบทความนี้เราได้เรียนรู้วิธีการทำงานกับชั้นการปรับเส้นโค้งในเอกสารของ Photoshop โดยใช้ Aspose.PSD สำหรับ Java ในวิธีการทำงานสองวิธีที่แตกต่างกันอย่าง สมบูรณ์แบบและต่อเนื่อง
