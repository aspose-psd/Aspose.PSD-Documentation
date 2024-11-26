---
title: การใช้เลเยอร์การปรับปรุงสำหรับ PSD Enhancement
weight: 100
type: docs
description: ตัวอย่างการใช้เลเยอร์การปรับปรุงผ่าน Aspose.PSD สำหรับ Python
keywords: [เลเยอร์การปรับปรุง, ปรับปรุงรูปภาพ, การปรับความโทน, การปรับระดับ, การกลับ, ฟิลเตอร์รูปภาพ,  PSD API, Python, ตัวอย่างโค้ด]
url: th/python-net/adjustment-layer-enhancement/
---

## **ภาพรวม**

ในบทความนี้ เราจะสำรวจการแก้ไขเลเยอร์การปรับปรุงใน Aspose.PSD สำหรับ Python  เลเยอร์การปรับปรุงเป็นคุณสมบัติที่มีความสามารถในการแก้ไขรูปภาพโดยที่ไม่ทำลายรูปภาพของคุณ Aspose.PSD จะให้ชุดคลาสเลเยอร์การปรับปรุงที่ครอบคลุมที่คุณสามารถใช้เพื่อปรับเปลี่ยนด้านต่าง ๆ ของรูปภาพของคุณ

เพื่อสื่อแสดงการแก้ไขเลเยอร์การปรับปรุง เราจะใช้โค้ดตัวอย่างที่สุดท้ายของหน้าที่โหลดภาพ PSD และใช้การปรับปรงต่าง ๆ ใส่เลเยอร์

ในโค้ดตัวอย่างด้านล่าง เราเริ่มต้นโดยการโหลดภาพ PSD โดยใช้เมทอด PsdImage.load() เราจากนั้นสร้างตัวเลือกสำหรับการบันทึกไฟล์ PNG ผลลัพธ์ คลาส PngOptions ช่วยให้เราระบุประเภทสีสำหรับภาพผลลัพธ์

ต่อมา เราวนทีละเลเลอร์ในภาพ PSD และตรวจสอบประเภทของเลเลอร์โดยใช้เมทอด is_assignable() หากเลเลอร์เป็นประเภทหนึ่งเราจะแปลงมันเป็นประเภทนั้นโดยใช้เมทอด cast() และปรับการปรุงเพื่อให้เอาชนะ ตัวอย่างเช่น เราจะปรับความสว่างและความคมดวงของ BrightnessContrastLayer ปรับระดับของ LevelsLayer เพิ่มจุดการโค้งใน CurvesLayer และอื่น ๆ

คุณสามารถเพิ่มโค้ดเพื่อปรับปรุงอื่น ๆ สำหรับเลเลอร์ที่เกี่ยวข้องของพวกระบดีเลเยอร์การปรับปรุงมีให้มากมาย เช่น [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) และอื่น ๆ

สุดท้าย เราบันทึกภาพที่ปรับแก้ด้วยเมทอด save() ของคลาส PsdImage

โค้ดนี้ให้ภาพรวมพื้นฐานเกี่ยวกับวิธีการแก้ไขเลเลอร์การปรับปรงใน Aspose.PSD สำหรับ Python คุณสามารถปรับปรุงการปรับปรงตามความต้องการของคุณ และสำรวจตัวเลือกที่มีอยู่ในเอกสาร API

กรุณาตรวจสอบตัวอย่างเต็ม

## **ตัวอย่าง**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
