---
title: การสนับสนุนของชั้นการเติม
type: สารบัญ
weight: 90
url: /th/net/support-of-fill-layers/
---

## **ชั้นการเติมด้วยการเติมแบบรูปแบบ**
บทความนี้สาธิตวิธีการเติมชั้น [PSD](https://wiki.fileformat.com/image/psd/) ด้วยการเติมแบบรูปแบบ รูปแบบ* * เป็นภาพ สี เงา หรือเส้นที่ใช้เติมพื้นที่ของภาพ โปรดใช้ Aspose.PSD.FileFormats.Psd.Layers.FillLayer เพื่อเพิ่มรูปแบบในชั้น PSD โค้ดตัวอย่างต่อไปนี้โหลดไฟล์ PSD เข้าถึงคลาส [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) และตั้งค่ารูปแบบโดยใช้สมบัติ [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) 

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}

นี่คือตัวอย่างอีกตัวที่สาธิตว่า [Aspose.PSD](https://products.aspose.com/psd/net) เติมรูปแบบโดยใช้ [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) และ [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings) 

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}

## **ชั้นการเติมด้วยการเติมไล่สี**
บทความนี้สาธิตถึงการใช้การเติมไล่สีเพื่อเติมชั้น PSD Aspose.PSD APIs ได้เปิดเผยวิธีการที่มีประสิทธิภาพและง่ายต่อการใช้เพื่อบรรลุวัตถุประสงค์นี้ Aspose.PSD ได้เปิดเผยคลาส [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) และ [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) เพื่อเพิ่มอิสระมาในชั้น

ขั้นตอนการเติม [the PSD](https://wiki.fileformat.com/image/psd/) ชั้นด้วยการเติมไล่สีมีความง่ายดังนี้:

- โหลดไฟล์ PSD เป็นภาพโดยใช้วิธีการของโรงงาน [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) ที่เปิดเผยโดยคลาส [Image](https://reference.aspose.com/net/psd/aspose.psd/image)
- ตั้งค่าสมบัติของวัตถุ [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)
- สร้างรายการ [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) ด้วยสีที่ต้องการและตำแหน่งของสี
- สร้างรายการของจุดโปร่งใสที่ต้องการโปร่งใสและตำแหน่งของจุดโปร่งใส
- เรียกใช้วิธีการ [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update)
- บันทึกผลลัพธ์

โค้ดตัวอย่างต่อไปนี้แสดงวิธีการเติมไล่สีเข้ากับชั้น PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}

**นี่คือตัวอย่างอีกอันที่ใช้คุณสมบัติ [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** เพื่อเติมชั้น PSD ด้วยการเติมไล่ **Aspose.PSD** สนับสนุนประเภทการไล่สีต่อไปนี้ผ่านการเปรียบเทียบประเภทการไล่สี:

- **ประเภทการไล่เส้นตรง:** ในการไล่สีเส้นตรง สีมีการเปลี่ยนแปลงจากจุดเริ่มต้นไปยังสิ้นสุดอย่างตรงไป
- **ประเภทการไล่รัศมี:** ในการไล่สีรัศมี สีกระจายออกจากจุดเริ่มต้นในรูปแบบวงกลม
- **ประเภทการไล่มุม:** การไล่สีมุมหมุนตามเข็มนาฬิการอบจุดเริมต้น
- **ประเภทการไล่กระจกทราย:** ในการไล่สีกระจกทราย สีถูกสะท้อนทางด้านทั้วสองของจุดเริมต้น
- **ประเภทการไล่รูปห้าเหลี่ยม:** การไล่เสีรูปห้าเหลี่ยมสร้างรูปรูปห้าเหลี่ยมจากจุดเริมต้น

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

## **การสนับสนุนคุณสมบัติการยืดสำหรับชั้นเติมสีสายไล่**
บทความนี้สาธิตวิธีการยืด FillLayer ด้วยการเติมสีสายไล่โดยใช้ Aspose.PSD for .NET สำหรับวัตถ์นี้ เพิ่มคุณสมบัติใหม่ [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) ใน [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings)

ด้านล่างเป็นการสาธิตโค้ดที่แสดงวิธีการใช้คุณสมบัติ **Scale**

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}

## **ชั้นการเติมด้วยการเติมสี**
บทความนี้สาธิตวิธีการเติมชั้น [PSD](https://wiki.fileformat.com/image/psd/) ด้วยสี โปรดใช้คลาส [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) เพื่อเติมสีในชั้น PSD โค้ดตัวอย่างต่อไปนี้โหลดไฟล์ PSD และเข้าถึงชั้น Fill และตั้งค่าสีโดยใช้รูปแบบ [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}
