---
title: การใช้งานเลเยอร์การปรับปรุงสำหรับ PSD
weight: 100
type: docs
description: ตัวอย่างการใช้งานเลเยอร์การปรับปรุงผ่าน Aspose.PSD สำหรับ C#
keywords: [การปรับเลเยอร์, ปรับปรุงรูปถ่าย, การปรับเลเยอร์เว้นบรรทัด, การปรับระดับการเพิ่ม, การกลับ, ฟิลเตอร์รูปภาพ, สร้าง API, C#, ซีชาร์ป, ตัวอย่างโค้ด]
url: th/net/adjustment-layer-enhancement/
---

## ภาพรวม

ในบทความนี้ เราจะสำรวจการแก้ไขเลเยอร์การปรับปรุงใน Aspose.PSD สำหรับ C# เลเยอร์การปรับปรุงเป็นคุณสมบัติที่มีประสิทธิภาพในการแก้ไขภาพซึ่งช่วยให้คุณสามารถทำการเปลี่ยนแปลงรูปภาพของคุณโดยไม่ทำลาย  Aspose.PSD ให้ชุดคลาสเลเยอร์การปรับปรุงอย่างครบถ้วนที่คุณสามารถใช้เพื่อแก้ไขและปรับปรุงด้านต่าง ๆ ของรูปภาพของคุณ

เพื่อสาธิตการแก้ไขเลเยอร์การปรับปรุง เราจะใช้ตัวอย่างโค้ดที่อยู่ที่ด้านล่างของหน้าเพจเพื่อโหลดรูปภาพ PSD และใช้การปรับปรุงต่าง ๆ กับเลเยอร์ของมัน

ในตัวอย่างโค้ดด้านล่าง เราเริ่มหากดํหการโหลดไฟล์ PSD ด้วยวิธี `PsdImage.Load()` จากนั้นเราตั้งค่าสำหรับการบันทึกไฟล์ PNG ด้วยชั้น `PngOptions` ที่ช่วยให้เรากําหนดชนิดสีสำหรับรูปภาพผลลัพธ์

ต่อมาเราทำการวนซ้กเลเยอร์ในรูปภาพ PSD และตรวจสอบประเภทของเลเยอร์ด้วยวิธี `IsAssignable()` หากเลเยอร์เป็นประเภทพิเศษ เราจะแปลงมันให้กลายเป็นชนิดดังกล่าวด้วยวิธี `Cast()` และสมการปรับปรุงตามที่ต้องการ เช่น เราได้ปรับความสว่างและความคมชัดของ `BrightnessContrastLayer` ปรับระดับของ `LevelsLayer` เพิ่มจุดโค้งให้กับ `CurvesLayer` และอื่น ๆ

คุณสามารถเพิ่มโค้ดเพื่อปรับปรุงสิ่งที่ปรับให้กับเลเยอร์ของตนเอง Aspose.PSD มีชุดคลาสเลเยอร์การปรับปรุงที่หลากหลาย เช่น [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) และ อื่น ๆ

สุดท้ายเราบันทึกภาพที่ปรับแก้ไขไว้ด้วยวิธี `Save()` ของคลาส `PsdImage`

โค้ดนี้จะให้ภาพรวมพื้นฐานเกี่ยวกับวิธีแก้ไขเลเยอร์การปรับปรุงใน Aspose.PSD สำหรับ C# คุณสามารถปรับเปลี่ยนการปรับปรุงตามความต้องการของคุณและสำรวจตัวเลือกต่าง ๆ ที่มีอยู่ในเอกสาร API 

## ตัวอย่าง

นี่คือตัวอย่างโค้ดที่แสดงวิธีการใช้งานเลเยอร์การปรับปรุงใน Aspose.PSD สำหรับ C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

สำหรับข้อมูลและตัวอย่างอื่น ๆ โปรดเยี่ยมชม [เอกสาร Aspose.PSD สำหรับ C#](https://docs.aspose.com/psd/net/).
